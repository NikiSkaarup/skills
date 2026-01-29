# llm skills

---

## btca

Use `btca` to look up Umbraco documentation or Umbraco CMS source code.

**Quick usage:**

```bash
btca ask -r <resource> -q "<question>"
```

**Available resources:**

- `umbraco` - Umbraco CMS source code
- `umbracoDocs` - Umbraco documentation

**When to use btca:**

- You need Umbraco-specific APIs, configuration, or behavior details
- You need official documentation references or source-level answers

**When not to use btca:**

- General C#/.NET questions that are not Umbraco-specific
- Project-specific code browsing (use repo search/read tools)

**Examples:**

```bash
btca ask -r umbraco -q "How does Umbraco handle content publishing events?"
btca ask -r umbracoDocs -q "How to create custom data types?"
btca ask -r umbracoDocs -q "How to configure the Content Delivery API?"
```

---
