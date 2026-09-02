# Document Metadata

Each library document should carry enough metadata to establish what it is, where it came from, what may be done with it, and how it relates to the stable library identifier.

## Recommended metadata

- **id** — stable `ag://` identifier
- **title** — human-readable document title
- **authors** — author or organization, when known
- **date** — publication or source date, when known
- **source** — original source, archive, or publication
- **provenance** — how the library copy was obtained or converted
- **license** — copyright/public-domain/license status
- **format** — source format and library format
- **locations** — known local, repository, mirror, or remote locations
- **notes** — preservation or conversion notes

## Sidecar metadata

Metadata may be stored in a sidecar file alongside a guide when embedding metadata in the AmigaGuide document would reduce compatibility. The sidecar format will be standardized as the library develops.

## Preservation principle

Conversion should not discard useful source information. When a PDF, HTML, or text source is converted into `.guide`, retain source attribution, licensing information, provenance, and other relevant metadata.
