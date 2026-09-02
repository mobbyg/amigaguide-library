# AmigaGuide Library

The document library for the [AmigaGuide on Linux](https://github.com/mobbyg/amigaguide-on-linux) project.

This repository serves two related purposes: preserving useful AmigaGuide material and providing a canonical collection of documents for testing the reader and future AmigaGuide tools.

## Goals

- Preserve original and historically useful AmigaGuide documents.
- Provide public-domain works in AmigaGuide format.
- Host modern material when redistribution is permitted.
- Maintain a small, deliberate test corpus for parser, renderer, formatting, macros, navigation, and malformed-input testing.
- Give documents stable `ag://` identifiers that remain useful when files are moved or mirrored.

## Repository layout

```text
original/                 Historical and original AmigaGuide material
public-domain/            Public-domain and cleared works
modern/                   Modern material with appropriate redistribution rights
test-corpus/
  navigation/             Navigation and cross-document link tests
  formatting/             Formatting and rendering tests
  macros/                 Macro and command tests
  malformed/              Invalid or deliberately broken guides
docs/
  IDENTIFIERS.md          Stable ag:// identifier rules
  METADATA.md             Document metadata and provenance rules
```

## Stable identifiers

A library document may have an identifier such as:

```text
ag://gov.us.constitution
ag://gov.us.declaration-of-independence
ag://us.scotus.marbury-v-madison
```

The identifier belongs to the document, not to a filename, repository path, mirror, or download location. This allows the same work to be referenced consistently across local copies and future library services.

See `docs/IDENTIFIERS.md` for the current rules.

## Metadata and preservation

Every document should retain useful information about its title, authorship, source, date, licensing status, provenance, format, and known locations when that information is available. See `docs/METADATA.md`.

Future conversion tools may convert PDF, HTML, or plain text sources into `.guide` documents while preserving source metadata and creating AmigaGuide structure such as nodes, tables of contents, indexes, and cross-links where the source supports it.

## Architecture

The library is intentionally separate from the reader and from the future crawler/indexer:

```text
                         +----------------------+
                         |   AmigaGuide Reader  |
                         +----------+-----------+
                                    |
                   local file / HTTP / ag://GUID
                                    |
                                    v
                         +----------------------+
                         |   AmigaGuide Library |
                         +----------+-----------+
                                    ^
                                    |
                         +----------+-----------+
                         |  Crawler / Indexer   |
                         |      (future)        |
                         +----------------------+
```

The reader must remain useful with ordinary local `.guide` files and must not require the crawler, catalog, or an online service merely to open a document.

## Contributing

Before adding a document, verify its copyright and redistribution status. Preserve attribution and provenance whenever possible. See `CONTRIBUTING.md` for the basic contribution rules.

## Status

This repository is being established alongside the AmigaGuide reader. The initial priority is a clean, durable library structure and metadata model before building a large collection.
