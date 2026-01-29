# Headers and Auth

## Api-Key

- Required when public access is disabled.
- Required to access draft content with preview.

## Preview

- `Preview: true` requests draft content.
- Requires `Api-Key` when previewing.

## Accept-Language

- Use when querying by id to request a specific culture.
- When querying by path, the culture is usually implied by the path.

## Start-Item

- Use to scope requests to a root node in multi-site setups.
- Accepts a root node id (GUID) or path segment.
