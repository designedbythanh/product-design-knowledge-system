# [Product] — Design Guidelines

> **Role: `guidelines`.** The rules a design is judged against: values, patterns, states, copy, and the review checklist. Product facts (users, roles, vocabulary) live in `PRODUCT.md`. The design system (tokens, components) lives where it already is (Figma, Storybook, a tokens file); point to it from `PRODUCT.md` › Sources instead of copying it here.
>
> **Keep the headings as they are.** Skills find a section by its heading and read only the ones they need. Add `###` subsections freely.
>
> Write rules only you or your team know. A rule any designer would follow anyway ("buttons should look clickable") costs reading time and teaches a skill nothing.
>
> **When this file passes ~800 lines**, move a section to its own file and add a row to Sources, e.g. `guidelines.review-checklist` → `docs/review-checklist.md`.

---

## Values

> **Used by:** `decision-rationale` (as criteria), `design-scope-negotiator` (what to protect when cutting).
> **If missing:** both pick generic criteria.
>
> Product values: the "why" behind product decisions, specific to your domain. Each one gets a name, a one-paragraph definition, and 2–3 places in the product that prove it.
>
> Design values: phrased as testable conditions, not beliefs. Not "we believe in simplicity" but:

### Clarity

A screen is clear when:
- [ ] It answers a single dominant question
- [ ] The primary action is discoverable without reading instructions
- [ ] Labels and units are explicit; never relative time ("this week") without dates

---

## Patterns

> **Used by:** `design-critique-facilitator`, `edge-case-finder`, `acceptance-criteria`.
> **If missing:** they judge against common practice, not your product's conventions.
>
> Reusable interaction behavior, not components. Each pattern: name, trigger (when it applies), numbered rules, edge cases, what not to do.
>
> Common ones: empty states, errors (recoverable vs. not), loading (skeleton vs. spinner), drill-down and back navigation, confirmation dialogs (when required), filters and scope (does it persist across sessions?), saving (immediate vs. explicit).

---

## States

> **Used by:** `edge-case-finder`, `acceptance-criteria`, `design-critique-facilitator`.
> **If missing:** they list the states a screen *could* have, not the ones your product defines.
>
> Every state a major screen can be in: empty (first time vs. configured but no data), loading, partial, error (recoverable vs. fatal), limited (permission-gated), success. One feature's states go in its brief; states shared across screens go here.

---

## AI features

> *Skip if the product has no AI features.*
>
> **Used by:** `edge-case-finder`, `prd-first-draft`, `design-critique-facilitator`.
> **If missing:** they can't tell what the AI is allowed to do, and may assume more than it can.
>
> One block per feature:

```
[Feature name]
- Can: [explicit list]
- Cannot: [explicit list]
- Requires human review before: [actions]
- When unsure, it: [says so / asks / does nothing]
```

---

## Microcopy

> **Used by:** `design-critique-facilitator`, `persona-pretest`, `acceptance-criteria`.
> **If missing:** copy is judged on general clarity, not your tone.
>
> Tone rules (3–5 adjectives, each with a definition and an example), copy templates (empty, error, partial data, status labels, confirmations, AI output), banned phrases, and a table of real examples:

| Context | ❌ Don't | ✅ Do | Why |
|---|---|---|---|
| Empty list | "No data found!" | "No reports yet. Create your first report." | Says what's missing and what to do |
| Error | "Something went wrong" | "Couldn't load campaigns. Check your connection and try again." | Specific and recoverable |

---

## Examples

> **Used by:** `design-critique-facilitator`.
> **If missing:** the critique has no picture of "good" in your product.
>
> Annotated good and bad examples from your product. Link the screen (Figma frame, screenshot in `evidence/`) and say in 2–3 sentences why it works or what's wrong.

---

## Review checklist

> **Used by:** `design-critique-facilitator`.
> **If missing:** the critique uses its five general lenses only, and can't catch what's specific to your product.
>
> What a design must pass before it ships. Only checks you'd actually fail a design on.

### Core
- [ ] Single dominant question per screen
- [ ] All numbers have units

### States
- [ ] Empty state designed (first time and no data)
- [ ] Error state includes a recovery action

### Copy
- [ ] No relative time without a date
- [ ] AI-generated text is editable and dismissible

### Accessibility
- [ ] Text contrast ≥ 4.5:1 (WCAG AA)
- [ ] Color is never the only signal
- [ ] Touch targets ≥ 44×44px

---

## Open questions

> Rules not settled yet, and what they wait on. Skills won't treat anything here as decided.
>
> - [ ] [Question] — blocking [section] — owner: [person]
