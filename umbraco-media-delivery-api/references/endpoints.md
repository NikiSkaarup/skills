# Media Delivery API Endpoints

All endpoints are prefixed with `/umbraco/delivery/api/v2`.

## Get a media item by id

`GET /media/item/{id}`

- Use when you have the media key (GUID).
- Returns a single media item.
- `id` refers to the media item's key, not its integer id.

## Get a media item by path

`GET /media/item/{path}`

- Use when you have a full folder path to the item.
- Returns a single media item.

## Get media items by id list

`GET /media/items?id={id}&id={id}`

- Use to fetch multiple items by key.
- Returns a list of media items.

## Query media items

`GET /media`

- Use for discovery, filtered lists, or structural queries.
- Supports `fetch`, `filter`, `sort`, `skip`, `take`.
