# Localization

[Database documentation](../README.md)

Tables ending in _locale translate parent content. Their complete key includes parent identity components and locale. A quest-objective locale identifies an objective, not merely its quest. Gossip options, creature text, and player-choice responses can require multiple parent components.

Typical locale strings include deDE, esES, esMX, frFR, itIT, koKR, ptBR, ruRU, zhCN, and zhTW where supported by the current LocaleConstant/client. Do not infer support from a varchar width alone.

## Text sources

Local text fields can coexist with BroadcastTextID, sound, language, and other client-facing references. Broadcast text originates in client/hotfix data; translating a world fallback field may not change the active broadcast-text path.

trinity_string stores server messages and locale variants in one table. Its format placeholders must remain compatible with the call site. page_text chains use NextPageID and a separate locale table.

NULL, empty strings, missing locale rows, and fallback behavior are determined by the loader and consumer. Avoid bulk conversions between NULL and empty text.

## Workflow

Identify the actual parent record and active text source. Preserve placeholders, inline tokens, line breaks, and formatting accepted by that consumer. Insert/update the translation using every parent key component and an accepted locale. Verify with a client using that locale, including fallback behavior when a translation is absent.

Translation changes should not alter gameplay identities, flags, rewards, or prerequisites. Keep provenance in VerifiedBuild consistent with the source of the translation.
