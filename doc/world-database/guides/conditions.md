# Conditions

[Database documentation](../README.md)

[conditions](../tables/conditions.md) attaches typed predicates to supported content sources. The source tuple identifies the gated content. The condition discriminator and operands describe the test. [Condition enums](../reference/conditions-enums.md) supplies this checkout's source values, target availability, and predicate operand comments.

## Source identity

SourceTypeOrReferenceId selects the source category for ordinary rows. SourceGroup, SourceEntry, and SourceId have different meanings for different source types. A gossip option, spell target, loot row, and SmartAI event do not share one universal key layout.

Read ConditionMgr's source attachment code as well as the source enum comments. SourceGroup or SourceId values that are valid for one type may be rejected or ignored for another.

## Boolean composition

Within the same source and ElseGroup, predicates are ANDed. Different ElseGroup alternatives are ORed. Thus an intended “A and B, or C” uses A/B in one group and C in another.

NegativeCondition negates an individual predicate. It is distinct from a negative ConditionTypeOrReference, which calls a reusable reference.

ConditionTarget selects a target slot supplied by the source. Do not assume every source exposes every target or that target 0 always means a player.

## Reusable references

A negative SourceTypeOrReferenceId defines a reference template identified by its absolute value. A negative ConditionTypeOrReference invokes a template. Reference definitions do not use ordinary source attachments. Avoid self-references, cycles, missing templates, and irrelevant operand values.

ConditionValue1–3 and ConditionStringValue1 are selected by predicate type. For example, string-ID conditions use the string operand; other predicates validate spell, item, quest, area, faction, level, or other values.

ErrorType/ErrorTextId are meaningful only where the source supports user-facing failure reporting. ScriptName may invoke a registered condition script.

## Inspection

```sql
SET @source_type = 0; -- replace with the current enum
SET @source_entry = 0; -- replace with the relevant content ID
SELECT *
FROM conditions
WHERE SourceTypeOrReferenceId = @source_type
  AND SourceEntry = @source_entry
ORDER BY SourceGroup, SourceId, ElseGroup, ConditionTypeOrReference;
```

Filter the complete source tuple for an edit; SourceEntry alone can collide across source categories.

## Label-view defect

vw_conditions_with_labels currently computes the predicate label using SourceTypeOrReferenceId, rather than ConditionTypeOrReference. It can therefore display a convincing but wrong predicate name. Use the numeric base table and current source enums; the view definition is preserved on its object page.

## Validation

Test both passing and failing cases, alternatives, negation, the correct target, and reusable references. Check load-time diagnostics for invalid source tuples and irrelevant operands. A condition that works in one interaction may fail in another if the source supplies a different target context.
