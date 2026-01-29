---
name: umbraco-mcp-content-ops
description: Guide Claude to perform Umbraco content operations via MCP tools safely.
---

# Umbraco MCP Content Ops

## Purpose

Guide Claude to perform Umbraco content operations efficiently and safely using the MCP tool collections.

## Scope

- Included: content CRUD, publishing, content audits, media management, localization, redirects, content webhooks, content version/history queries.
- Excluded by default: schema changes (document/data types), infrastructure ops, cross-environment diffs.

## When to Use

- Automating or assisting with content and media tasks in Umbraco.
- Running content audits or reporting tasks against the content tree.

## When Not to Use

- Document Type/Data Type changes or developer tooling.
- Server health, logs, and indexing tasks.

## Tool Collection Strategy

- Always request the smallest set of tool collections needed for the task.
- See `references/tool-collections.md` for task-to-collection mapping.

## Execution Policy

- Read before write: fetch existing items and configuration first.
- Validate before mutate: use validation endpoints where available.
- Prefer search and by-id-array endpoints to reduce calls.
- Paginate for large lists; batch writes with clear progress.

## Safety Rules

- Require confirmation for destructive actions: delete, recycle-bin empty, and large moves.
- Require confirmation for bulk publish/unpublish or actions affecting more than 25 items.
- If permissions are unclear, fetch current user permissions and report limits.

## Response Format

- Summarize actions taken, list affected items, and note any skipped items.
- For read-only tasks, return concise findings with counts and key examples.
- Include next steps only when useful (e.g., publish, review, or verify).

## Examples

- Bulk create blog posts from CSV under `/blog`.
- Audit published pages missing meta descriptions.
- Publish all pages tagged `release-notes`.
- Upload images from a local folder into a Media folder and link them.
- Add a new language and create variants for a section.
- Create a redirect from `/old-path` to `/new-path`.
