# Content Ops Tool Collections

Use the minimal set of collections needed for the task.

## Common Tasks

- Content CRUD and publish flows -> `document`
- Content audits and versions -> `document`, `document-version`
- Content relationships and impact -> `document`, `relation`, `relation-type`
- Media uploads and management -> `media`, `temporary-file`
- Localization and dictionary items -> `language`, `dictionary`
- Tags and content categorization -> `tag`, `document`
- Redirects -> `redirect`
- Content webhooks -> `webhook`
- Permission checks -> `user`

## Example Pairings

- Create pages from CSV -> `document`, `document-type`
- Publish tagged pages -> `document`, `tag`
- Find broken media references -> `document`, `media`
- Add German variants -> `document`, `language`
- Replace a media asset -> `media`, `document`
