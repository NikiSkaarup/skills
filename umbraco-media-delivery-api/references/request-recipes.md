# Common Request Recipes

## Get by id with minimal fields

`GET /umbraco/delivery/api/v2/media/item/{id}?fields=properties[altText,caption]`

## Get by path with expanded property

`GET /umbraco/delivery/api/v2/media/item/{path}?expand=properties[author]`

## Fetch children of root with type filter

`GET /umbraco/delivery/api/v2/media?fetch=children:/&filter=mediaType:Image&skip=0&take=10`

## Fetch children inside a folder path

`GET /umbraco/delivery/api/v2/media?fetch=children:/root/child/&skip=0&take=20`

## Multi-id fetch

`GET /umbraco/delivery/api/v2/media/items?id={id1}&id={id2}`
