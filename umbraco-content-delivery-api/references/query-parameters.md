# Content Delivery API Query Parameters

The following parameters apply to the `/content` and item endpoints as documented.

## expand

Expand related properties from picked content or media.

- `?expand=properties[$all]`
- `?expand=properties[alias1,alias2]`
- `?expand=properties[alias1[properties[nested1,nested2]]]`

## fields

Limit the properties returned.

- `?fields=properties[$all]`
- `?fields=properties[alias1,alias2]`
- `?fields=properties[alias1[properties[nested1,nested2]]]`

## fetch

Structural selector for `/content` only. Only one selector at a time.

- `?fetch=ancestors:{idOrPath}`
- `?fetch=children:{idOrPath}`
- `?fetch=descendants:{idOrPath}`

## filter

Filter options for `/content`.

- `?filter=contentType:alias`
- `?filter=name:nodeName`
- `?filter=createDate>:2023-01-01`
- `?filter=updateDate<:2024-01-01`

Notes:

- `contentType` and `name` support negation: `contentType:!article`.
- Date filters support `>`, `>:`, `<`, `<:` operators.

## sort

Sort options for `/content`.

- `?sort=createDate:asc`
- `?sort=updateDate:desc`
- `?sort=name:asc&sort=sortOrder:asc`

## skip / take

Pagination for `/content`.

- `?skip=0&take=20`
