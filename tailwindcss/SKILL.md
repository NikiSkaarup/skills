---
name: tailwindcss
description: Guide Tailwind CSS v4 usage with best-practice utility patterns and theme variable guidance.
---

# Tailwind CSS v4

## Purpose

Provide guidance for using Tailwind CSS v4 effectively in projects that are already configured, with an emphasis on utility-first patterns, maintainability, and theme variables.

## Scope

- Included: utility composition, variants, responsive and container query patterns, theme variables, and custom CSS hooks.
- Excluded: installation, build tooling, and migration guidance.

## When to Use

- You are authoring or refactoring UI in a Tailwind CSS v4 codebase.
- You need best-practice guidance for composing utility classes and managing reuse.
- You are defining or extending design tokens using theme variables.
- You need patterns for variants, responsive behavior, or container queries.

## Response Guidance

- Prefer composing utility classes directly in markup; use variants for state, media, and feature conditions.
- Manage duplication with components or template partials; for localized repetition, edit class lists directly rather than inventing abstractions.
- Use `@layer base` for default element styles and `@layer components` for reusable classes that can still be overridden by utilities.
- Use `@apply` only when writing custom CSS or styling third-party markup; avoid turning utilities into permanent abstractions.
- Avoid conflicting utilities on the same element; choose one source of truth or expose explicit props.

## Theme Variables

Theme variables are defined with `@theme` and generate both utilities and CSS variables.

```css
@import "tailwindcss";

@theme {
  --color-mint-500: oklch(0.72 0.11 178);
  --font-poppins: Poppins, sans-serif;
  --breakpoint-3xl: 120rem;
}
```

- Use `@theme` for design tokens that should map to utilities; use `:root` for plain CSS variables that should not generate utilities.
- Common namespaces include `--color-*`, `--font-*`, `--text-*`, `--spacing-*`, `--radius-*`, `--shadow-*`, `--breakpoint-*`, `--container-*`, and `--animate-*`.
- Extend defaults by adding new variables, override by redefining, and reset a namespace with `--color-*: initial` or the entire theme with `--*: initial`.
- Prefer CSS variables for custom CSS and inline styles, for example `var(--color-sky-500)` or `bg-(--my-color)`.
- Use `@theme inline` when a theme variable references other variables to avoid unexpected resolution; use `@theme static` when you want all theme variables emitted regardless of usage.
- `theme()` is deprecated in v4; use CSS variables instead and only reach for `theme(--breakpoint-*)` in edge cases like media queries.

## Common Patterns

- Stack variants to express state and media logic in place, for example `dark:md:hover:bg-sky-700`.
- Use `group`, `peer`, and named group/peer variants for parent or sibling state, and `in-*` for implicit parent state when scoping is not required.
- Use arbitrary values and variants sparingly for one-offs, for example `bg-[#316ff6]`, `[&.is-dragging]:cursor-grabbing`, and `text-(length:--size)` when ambiguous.
- Build responsive layouts with `sm:` and `max-*` ranges; use `@container` with `@md` or `@max-md` for container-query components.
- For dynamic values, set CSS variables inline and consume them with utilities:

## Pitfalls

- Conflicting utilities target the same property; avoid combining them or use explicit conditional class selection.
- `peer` only affects following siblings; it cannot style elements that appear before the peer.
- Parent child selectors like `*:` and `**:` cannot be overridden by child utilities due to generation order and equal specificity.
- Overusing `@apply` leads to rigid abstractions; prefer components or utility composition unless you need custom CSS.
- If theme variables reference other variables, prefer `@theme inline` to avoid unexpected fallback behavior.
