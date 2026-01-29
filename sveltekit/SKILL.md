---
name: sveltekit
description: Guide SvelteKit development using official SvelteKit documentation.
---

# SvelteKit

## Purpose
Guide responses for SvelteKit app architecture, routing, data loading, and deployment based on official docs.

## Scope

- Included: project structure, file-based routing, `+page/+layout/+server`, `load` functions, form actions, hooks, adapters, config, env, SSR/CSR/prerendering.
- Excluded: non-SvelteKit frameworks, Svelte-only topics unless required, and unrelated tooling.

## When to Use

- You need help with SvelteKit routing, data loading, endpoints, adapters, or configuration.
- You are building or debugging a SvelteKit app.

## Response Guidance

- Prefer SvelteKit-native patterns (`load`, form actions, `+server` handlers).
- Call out server-only vs universal code and serialization constraints.
- Point to the correct locations (`src/routes`, `src/lib`, `static`).
- Mention where settings live (`svelte.config.js`, `vite.config.js`, `src/app.html`).

## Key Concepts to Emphasize

- File-based routing with `src/routes` and `+page/+layout/+server` files.
- `load` functions, `+page.server` for server-only logic, and `prerender/ssr/csr` options.
- Adapters for deployment (`adapter-auto`, `adapter-node`, `adapter-static`, etc.).
- Server hooks (`hooks.server.js`) and client hooks (`hooks.client.js`).

## References

- https://svelte.dev/docs/kit/llms.txt
