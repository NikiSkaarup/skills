# Content Ops Guardrails

## Confirmations

- Require confirmation for delete, recycle-bin empty, or move-to-recycle-bin.
- Require confirmation for bulk publish/unpublish or actions affecting more than 25 items.

## Validation

- Use `validate-document` and `validate-media` before write operations.
- If validation fails, summarize missing or invalid fields.

## Permissions

- If write fails or scope is unclear, check current user permissions.
- Report permission gaps and stop further mutations.

## Error Handling

- Aggregate errors for bulk operations and continue when safe.
- Report skipped items with reasons.

## Idempotency

- Search by unique fields before creating to avoid duplicates.
