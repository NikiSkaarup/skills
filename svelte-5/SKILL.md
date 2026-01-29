---
name: svelte-5
description: Guide Svelte 5 development with runes and migration-aware practices.
---

# Svelte 5

## Purpose
Guide responses for Svelte 5 component authoring, reactivity, and migration from Svelte 4 based on official docs.

## Scope
- Included: Svelte 5 runes, component APIs, props, events, snippets, reactivity, effects, and TypeScript usage.
- Excluded: SvelteKit topics unless required by user context, and unrelated tooling.

## When to Use
- You are building or migrating Svelte components to Svelte 5.
- You need guidance on runes, reactivity, props, events, snippets, or Svelte 5 API changes.

## Response Guidance
- Prefer runes ($state, $derived, $effect) over legacy $: and implicit reactivity.
- Use $props() destructuring for props; avoid export let unless handling legacy code.
- Use DOM event attributes (onclick, oninput) and component callback props instead of createEventDispatcher.
- Favor snippets (children + {@render ...}) over slots.
- Call out bindable props with $bindable and warn against mutating non-owned state.

## Key Changes: Svelte 4 -> 5
- Reactivity: runes replace implicit reactivity and most $: usage.
- Props: $props() replaces export let; bindable props require $bindable.
- Events: DOM event attributes replace on:; component events become callback props.
- Slots: snippets replace slot and let: patterns.
- Components: function-based mount/hydrate replace class instance APIs ($on/$set/$destroy).
- Modules: <script module> replaces <script context="module">.
- New file types: .svelte.js and .svelte.ts support runes.
- Migration helper: npx sv migrate svelte-5.

## TypeScript Guidance
- Prefer explicit prop interfaces with $props() destructuring:

```ts
interface Props {
  class?: ClassValue;
  text: string;
}

let { class: className, text }: Props = $props();
```

- If using snippet props, type them with Snippet:

```ts
import type { Snippet } from 'svelte';

interface Props {
  children?: Snippet;
}
```

- Use .svelte.ts and .svelte.js for shared reactive logic; do not export reassigned $state directly.
- For wrapper component typing, use DOM types from svelte/elements when needed.
- Recommend the Svelte VS Code extension and the TypeScript plugin for best editor support.

## References
- https://svelte.dev/docs/svelte/llms.txt
