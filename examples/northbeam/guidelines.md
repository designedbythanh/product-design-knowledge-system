# Northbeam — Design Guidelines

## Values

### Scope is never a surprise
Every setting exists at agency level and per client. A designer must be able to answer, for any control: which level does this change, and who else does it reach?
- Pipeline columns show ↺ on a cell a client overrides, to go back to the agency value
- The scope shows next to every control it affects (DL-001)

### Settings for people who live in Excel
Ops coordinators set up a client once a month. A settings page should read like the table they already keep, not like a form.

## Patterns

### Saving settings
1. Switches save at once. No Save button.
2. The cell locks while it saves and shows an "Undo" toast after.
3. Changing the scope keeps the user on the page and reloads the table in place.
- Never: a switch that saves at once inside a form that has a Save button.

### Scope
1. The scope (Agency or a client) is visible next to any control it affects, not only at the top of the page.
2. The Undo toast names the scope: "Seniority hidden in Offer for all clients · Undo".

## States

- Settings tables: empty (agency with no custom fields), loading (skeleton rows), saving (cell locked), overridden (↺ on the cell), read-only (lists and fee models, for a recruiter)

## Microcopy

- Plain, short, recruiting words: "candidate", "client", "hire"
- Say the scope whenever a change depends on it

| Context | ❌ Don't | ✅ Do | Why |
|---|---|---|---|
| Undo toast, agency level | "Saved · Undo" | "Seniority hidden in Offer for all clients · Undo" | Names what changed and how far |

## Examples

Not provided

## Review checklist

- [ ] The scope is visible next to every control it affects
- [ ] The Undo toast names the scope
- [ ] A row that owns a list says so, and the list icon is explained
- [ ] Where a recruiter can't edit (lists, fee models), nothing looks clickable
- [ ] Text contrast ≥ 4.5:1

## Open questions

- [ ] One merged Settings › Fields page, or two linked pages — owner: product lead — blocking: briefs/settings-fields.md
