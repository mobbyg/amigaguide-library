# Contributing

Contributions to the AmigaGuide library are welcome.

## Adding documents

Before adding a document, verify its copyright and redistribution status. Preserve source attribution and provenance whenever possible.

Place documents in the collection that best describes them:

- `original/` — historical or original AmigaGuide material
- `public-domain/` — public-domain works and other material cleared for redistribution
- `modern/` — modern material for which redistribution permission or an appropriate license is available
- `test-corpus/` — small documents whose primary purpose is testing parser, renderer, formatting, macro, navigation, or error-handling behavior

## Stable identifiers

New library documents should receive a stable `ag://` identifier. See `docs/IDENTIFIERS.md` and `docs/METADATA.md`.

## Quality

For converted documents, keep the original source information and document any significant conversion decisions. Test guides should be intentionally small and focused on a specific behavior when practical.
