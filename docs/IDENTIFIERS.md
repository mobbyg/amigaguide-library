# Stable Document Identifiers

The library uses stable `ag://` identifiers for documents.

## Purpose

An identifier names the document itself, rather than a particular filename, directory, mirror, or download location. This lets the same document be referenced consistently when it is copied, mirrored, converted, or moved.

## Examples

```text
ag://gov.us.constitution
ag://gov.us.declaration-of-independence
ag://us.scotus.marbury-v-madison
```

## Rules

- Identifiers should be stable over time.
- Identifiers should be lowercase and URL-safe.
- An identifier should describe the document's logical identity, not its current storage path.
- Filenames and repository paths may change without changing the identifier.
- A new revision of the same work should normally retain its identifier unless it represents a materially different document.
- The identifier scheme should remain usable by the reader without requiring the crawler or online library service.

The exact namespace and collision-handling rules will be refined as the catalog grows.
