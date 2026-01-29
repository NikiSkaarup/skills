# Headless Dev Ops Flow Patterns

## Schema Change for API Clients

1. Fetch Document Type configuration and blueprint.
2. Apply additive changes when possible.
3. Validate updates before saving.
4. Trigger Models Builder and notify downstream consumers.

## Data Type Update

1. Fetch existing configuration.
2. Update settings with backward compatibility in mind.
3. Check references when changing editor type.

## Index Maintenance

1. List available indexes.
2. Rebuild selected index used by delivery APIs.
3. Report status or failures.

## Webhook Setup

1. Inspect available webhook events.
2. Create or update webhook for publish/unpublish.
3. Verify logs after first execution.

## Health and Logs

1. Run health checks by group.
2. Summarize warnings and errors.
3. Pull relevant logs when needed.
