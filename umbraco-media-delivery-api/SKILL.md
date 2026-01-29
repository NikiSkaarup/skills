---
name: umbraco-media-delivery-api
description: Guide to use the Umbraco Media Delivery API effectively and safely.
---

# Umbraco Media Delivery API

## Purpose

Guide to use the Umbraco Media Delivery API endpoints correctly and efficiently.

## Scope

- Included: endpoint selection, path vs id usage, query parameters, headers, media JSON structure.
- Excluded: media mutations, backoffice management, or MCP admin operations.

## When to Use

- You need to read media items via the Media Delivery API.
- You need to craft requests with filters, expansion, or paging.

## When Not to Use

- You need to create or update media.
- You need to manage media types or folders in the backoffice.

## Endpoint Strategy

- Choose the smallest endpoint that returns the needed data.
- Prefer single-item endpoints for known media items.
- Use list and query endpoints for discovery and pagination.

## Request Policy

- Use `Api-Key` when public access is disabled.
- Limit payloads with `fields` and use `expand` only when needed.
- Use `fetch=children` for structural queries (default implementation supports children only).

## Response Format

- Provide a canonical request shape with headers and query parameters.
- Explain the minimum required inputs and expected response types.

## Examples

- Get a media item by id.
- Get a media item by path.
- Fetch media items by id list.
- Fetch children of a folder with paging and filters.
