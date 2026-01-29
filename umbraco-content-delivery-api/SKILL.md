---
name: umbraco-content-delivery-api
description: Guide Claude to use the Umbraco Content Delivery API effectively and safely.
---

# Umbraco Content Delivery API

## Purpose

Guide Claude to use the Umbraco Content Delivery API endpoints correctly and efficiently.

## Scope

- Included: endpoint selection, path vs id usage, query parameters, headers, preview, localization.
- Excluded: backoffice mutations, schema changes, or MCP administrative operations.

## When to Use

- You need to read content via the Delivery API.
- You need to craft requests with filters, expansion, or paging.

## When Not to Use

- You need to create or update content.
- You need to manage content types or media in the backoffice.

## Endpoint Strategy

- Choose the smallest endpoint that returns the needed data.
- Prefer single-item endpoints for known content items.
- Use list and query endpoints for discovery and pagination.
- See `references/request-recipes.md` for common request shapes.

## Request Policy

- Use `Start-Item` for multi-site or root-scoped queries.
- Use `Accept-Language` only when requesting by id.
- Use `Preview: true` with `Api-Key` for draft content.
- Limit payloads with `fields` and use `expand` only when needed.

## Response Format

- Provide a canonical request shape with headers and query parameters.
- Explain the minimum required inputs and expected response types.

## Examples

- Get a content item by id.
- Get a content item by path.
- Fetch children of a node with paging.
- Filter by content type and sort by update date.
- Fetch a draft item with preview and API key.
