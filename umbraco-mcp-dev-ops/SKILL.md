---
name: umbraco-mcp-dev-ops
description: Guide Claude to perform Umbraco developer and ops tasks via MCP tools safely.
---

# Umbraco MCP Dev Ops

## Purpose
Guide Claude to perform Umbraco developer and operational tasks efficiently and safely using the MCP tool collections.

## Scope
- Included: document/data type management, templates and partials, scripts/stylesheets, models builder, health/logs, indexing/search, server diagnostics.
- Excluded by default: content authoring and bulk publishing workflows.

## When to Use
- Automating schema changes, developer assets, or operational diagnostics.
- Running health checks, log analysis, or index maintenance.

## When Not to Use
- Content creation or editorial operations.
- Media uploads or localization tasks.

## Tool Collection Strategy
- Always request the smallest set of tool collections needed for the task.
- See `references/tool-collections.md` for task-to-collection mapping.

## Execution Policy
- Read before write: fetch configuration or scaffolds first.
- Validate before mutate: use validation endpoints when available.
- Prefer search and by-id-array endpoints to reduce calls.
- Paginate large lists and batch changes with clear progress.

## Safety Rules
- Require confirmation for destructive actions (delete, remove folders).
- Require confirmation for broad schema changes affecting many types.
- If permissions are unclear, fetch current user permissions and report limits.

## Response Format
- Summarize actions taken and list affected assets.
- For read-only tasks, return concise findings with counts and key examples.
- Include next steps only when useful (e.g., rebuild models, run checks).

## Examples
- Create a new Document Type with required properties.
- Update a Data Type configuration across the project.
- Rebuild the external search index and report status.
- Run all health checks and summarize warnings.
- Generate Models Builder outputs after schema changes.
- Create a stylesheet or partial view scaffold.
