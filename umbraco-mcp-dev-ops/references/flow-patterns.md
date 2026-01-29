# Dev Ops Flow Patterns

## Document Type Update

1. Fetch configuration and blueprint.
2. Apply changes to allowed compositions and properties.
3. Validate update before saving.

## Data Type Update

1. Fetch existing configuration.
2. Update configuration values.
3. Verify references when changing editor type.

## Template/Partial Update

1. Fetch current content by path or id.
2. Update contents.
3. Confirm dependencies if referenced widely.

## Models Builder Generation

1. Check Models Builder status.
2. Trigger build.
3. Report completion and any errors.

## Health and Logs

1. Run health checks by group.
2. Summarize warnings and errors.
3. Pull relevant logs when needed.

## Index Maintenance

1. List available indexes.
2. Rebuild selected index.
3. Report status or failures.
