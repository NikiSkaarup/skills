# Content Ops Flow Patterns

## Bulk Content Creation

1. Load source data (CSV/JSON) via filesystem MCP.
2. Resolve target parent and document type.
3. Create documents in batches.
4. Optionally validate and publish if requested.

## Content Audit

1. Search for target content (by type, tag, or path).
2. Fetch required properties and metadata.
3. Report issues with counts and examples.

## Bulk Publish/Unpublish

1. Search for target items.
2. Confirm impact if large.
3. Publish/unpublish in batches.

## Media Upload

1. Create temporary files from local paths or URLs.
2. Create media items with correct parent folder and metadata.
3. Update references in documents if needed.

## Localization

1. Verify languages and fallbacks.
2. Create or update culture variants per document.
3. Report any missing mandatory properties.
