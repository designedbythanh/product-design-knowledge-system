# Layer 3 — Deep-Dive Modules

When a feature or domain is too complex for a guidelines section, it gets its own module. These are merged back into guidelines when stable.

A module exists as a standalone file only while it's being actively written. Once stable, it merges into the relevant guidelines section and the standalone file is deprecated.

## When to create a module

Create a module when:
- A single feature needs more than 200 lines to document properly
- A domain (data model, integration spec) requires its own reference structure
- You're writing something exploratory that might change before it's settled policy

Start from [`_TEMPLATE.md`](_TEMPLATE.md).

## Common module types

**Feature module** — One product feature in depth
- Compositions (which components, in what order, at what density)
- States (every state, every variant)
- Edge cases (no data, partial data, permission limits)
- Interaction flows (step by step)

**Data model module** — The technical truth about your data
- Entity definitions (what is a metric vs. a dimension?)
- Rules (what can and cannot be combined)
- Formulas (how calculated metrics are defined)
- Connector availability (which data source has which fields)

**Microcopy module** — Extended copy examples for a complex feature
- Full copy library for one feature
- Rationale per string
- Banned alternatives
