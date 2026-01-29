# Media Delivery API Query Parameters

The following parameters apply to the `/media` and item endpoints as documented.

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

Structural selector for `/media` only.

- `?fetch=children:{idOrPath}`

Note: the default Media Delivery API implementation supports only `children`.

## filter

Filter options for `/media`.

- `?filter=mediaType:Image`
- `?filter=name:size`

## sort

Sort options for `/media`.

- `?sort=createDate:asc`
- `?sort=updateDate:desc`
- `?sort=name:asc&sort=sortOrder:asc`

## skip / take

Pagination for `/media`.

- `?skip=0&take=10`

Notes:

- `take` defaults to 10 and accepts 0.
