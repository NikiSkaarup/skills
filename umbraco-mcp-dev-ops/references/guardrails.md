# Dev Ops Guardrails

## Confirmations

- Require confirmation for delete operations and folder removals.
- Require confirmation for broad schema changes affecting multiple types.

## Validation

- Use `validate-document-type` and `validate-document-type-post` before writes.
- If validation fails, summarize missing or invalid configuration.

## Permissions

- If write fails or scope is unclear, check current user permissions.
- Report permission gaps and stop further mutations.

## Error Handling

- Aggregate errors for bulk operations and continue when safe.
- Report skipped items with reasons and suggested fixes.

## Idempotency

- Search for existing types or assets before create to avoid duplicates.
