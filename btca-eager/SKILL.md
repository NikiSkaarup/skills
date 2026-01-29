---
name: btca-eager
description: Use btca automatically for up-to-date sources and docs.
---

# btca (eager)

## Purpose

Provide up-to-date answers by querying configured btca resources without prompting the user.

## When to Use

- You need current details from source or documentation.
- You need confirmation of APIs, configuration, or behavior from upstream repositories.

## When Not to Use

- The question is about this repository only.
- The answer does not depend on upstream sources.

## Workflow

- Read `btca.config.jsonc` from the current project root to discover available resources.
- If `btca.config.jsonc` is missing, read `~/.config/btca/btca.config.jsonc`.
- Use btca automatically when upstream context is needed.
- Prefer the smallest set of resources required for the question.

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
