# Common Request Recipes

## Get by id with minimal fields

`GET /umbraco/delivery/api/v2/content/item/{id}?fields=properties[title,summary]`

## Get by path with expanded hero block

`GET /umbraco/delivery/api/v2/content/item/{path}?expand=properties[hero]`

## Fetch children with paging

`GET /umbraco/delivery/api/v2/content?fetch=children:{idOrPath}&skip=0&take=20`

## Filter by content type and sort by update date

`GET /umbraco/delivery/api/v2/content?filter=contentType:article&sort=updateDate:desc&skip=0&take=10`

## Fetch draft content with preview

`GET /umbraco/delivery/api/v2/content/item/{id}`

Headers:

- `Preview: true`
- `Api-Key: {apiKey}`
