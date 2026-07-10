# Docs Style Guide

- Write in plain, direct English. Prefer "a health worker verifies the
  record" over passive voice.
- One doc, one topic. If a section grows past a page, it likely belongs in
  its own file — link it from [docs/README.md](README.md).
- Every doc that references a field, schema, or contract shared with another
  repo should link to [data-model.md](data-model.md) rather than
  re-describing it.
- Architecture decisions (the *why*, not the *what*) go in
  [docs/adr/](adr/README.md), not scattered inline — link to the ADR instead
  of re-arguing it.
- Mark anything not yet implemented explicitly as "planned," "sketch," or
  "forward-looking" — see [api-surface-sketch.md](api-surface-sketch.md) for
  the convention.
- Markdown must pass `markdownlint` (see `.markdownlint.yml`); CI enforces
  this on every PR.
- Don't invent URLs, contact details, or people. If a fact isn't confirmed,
  leave a clearly marked placeholder instead of a fabricated one.
