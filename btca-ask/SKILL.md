---
name: btca-ask
description: Ask before using btca for up-to-date sources and docs.
---

# btca (ask)

## Purpose

Offer btca research and wait for user confirmation before querying external sources.

## When to Use

- You need current details from source or documentation and should ask first.
- The answer likely depends on upstream repositories.

## When Not to Use

- The user already provided authoritative sources.
- The question is limited to this repository.

## Workflow

- Read `btca.config.jsonc` from the current project root to discover available resources.
- If `btca.config.jsonc` is missing, read `~/.config/btca/btca.config.jsonc`.
- Ask the user for confirmation before running btca.
- Use btca only after approval.

## Usage

```bash
btca ask -r <resource> -q "<question>"
```

Use multiple resources when needed:

```bash
btca ask -r svelte -r sveltekit -q "How to lazy load a svelte component?"
```

## Available Resources

read `btca.config.jsonc` or if it is missing try reading `~/.config/btca/btca.config.jsonc` for the name field in the resources array.
