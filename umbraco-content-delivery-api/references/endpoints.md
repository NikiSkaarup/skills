# Content Delivery API Endpoints

All endpoints are prefixed with `/umbraco/delivery/api/v2`.

## Get a content item by id

`GET /content/item/{id}`

- Use when you have the content key (GUID).
- Returns a single content item.
- `id` refers to the content item's key, not its integer id.

## Get a content item by path

`GET /content/item/{path}`

- Use when you have a routed path.
- Returns a single content item.

## Get content items by id list

`GET /content/items?id={id}&id={id}`

- Use to fetch multiple items by key.
- Returns a list of content items.

## Query content items

`GET /content`

- Use for discovery, filtered lists, or structural queries.
- Supports `fetch`, `filter`, `sort`, `skip`, `take`.
