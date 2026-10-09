# Documentation verification

Run from the repository root after generation. This checks captured object inventory, all column names/order/types, local Markdown and source-file links, source line bounds, Markdown heading anchors, and balanced code fences. It does not execute database writes or assert that every field meaning is known.

```powershell
python -c 'from pathlib import Path; p=Path("doc/world-database/verification.md"); fence=chr(96)*3; exec(p.read_text(encoding="utf-8").split(fence+"python"+chr(10),1)[1].split(chr(10)+fence,1)[0])'
```

```python
from pathlib import Path
import json, re, collections
root=Path.cwd()
out=root/'doc/world-database'
fence=chr(96)*3
snapshot=json.loads((out/'schema-snapshot.md').read_text(encoding='utf-8').split(fence+'json\n',1)[1].split('\n'+fence,1)[0])
errors=[]
pages=list(out.rglob('*.md'))
expected={t['TABLE_NAME'] for t in snapshot['tables']}
actual={p.stem for p in (out/'tables').glob('*.md')}
if expected!=actual: errors.append({'object_inventory':{'missing':sorted(expected-actual),'extra':sorted(actual-expected)}})
cols=collections.defaultdict(list)
for c in snapshot['columns']: cols[c['TABLE_NAME']].append(c)
for n,cs in cols.items():
    text=(out/'tables'/f'{n}.md').read_text(encoding='utf-8')
    section=text.split('## Schema',1)[1].split('## Keys and indexes',1)[0]
    found=re.findall(r'^\| \d+ \| '+chr(96)+r'([^'+chr(96)+r']+)'+chr(96)+r' \|',section,re.M)
    if found != [c['COLUMN_NAME'] for c in cs]: errors.append({'column_order':n})
    for c in cs:
        if chr(96)+c['COLUMN_TYPE']+chr(96) not in section: errors.append({'column_type':n+'.'+c['COLUMN_NAME']})
links=0
for p in pages+[root/'doc/README.md']:
    text=p.read_text(encoding='utf-8')
    plain=re.sub(r'^'+fence+r'.*?^'+fence+r'[^\n]*','',text,flags=re.M|re.S)
    for m in re.finditer(r'\[[^\]]+\]\(([^)]+)\)',plain):
        target=m.group(1)
        if target.startswith(('https://','http://')): continue
        links+=1
        path,_,anchor=target.partition('#')
        dest=(p.parent/path).resolve() if path else p
        if not dest.exists():
            errors.append({'broken_link':str(p.relative_to(root)),'target':target})
        elif anchor.startswith('L') and anchor[1:].isdigit() and not dest.suffix=='.md':
            line=int(anchor[1:])
            if line<1 or line>len(dest.read_text(encoding='utf-8',errors='replace').splitlines()):
                errors.append({'bad_source_line':target})
        elif anchor and dest.suffix=='.md':
            headings=re.findall(r'^#{1,6}\s+(.+)',dest.read_text(encoding='utf-8'),re.M)
            slugs={re.sub(r'[^a-z0-9_\- ]','',h.lower()).replace(' ','-') for h in headings}
            if anchor not in slugs: errors.append({'bad_anchor':target})
    if text.count(fence)%2: errors.append({'unbalanced_fence':str(p.relative_to(root))})
result={'markdown_files':len(pages)+1,'objects':len(actual),'columns':len(snapshot['columns']),'local_links_checked':links,'errors':errors}
print(json.dumps(result,indent=2))
if errors: raise SystemExit(1)

```
