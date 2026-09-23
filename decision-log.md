# DESIGN DECISION LOG

> **What this is**: A personal log of non-obvious design decisions — judgment calls that guidelines can't fully capture.
> **Who reads it**: Design agents use this as few-shot context when guidelines are ambiguous.
> **How to use it**: Append a new entry every time you make a decision that isn't obvious from guidelines alone. 5 minutes per entry is enough.
>
> **Format rule**: Each entry must have at minimum — context, decision, why, agent instruction.

<!--
Layer 2 — Decision Log. Append-only journal of non-obvious judgment calls:
the "why" behind the decisions that guidelines compress into rules.

This file is never edited — only appended. Old entries are settled; new entries
can supersede them but never replace them.

Add a decision log when you:
- Make a call that isn't covered by guidelines
- Choose option A over B when both seemed reasonable
- Override a common convention for a product-specific reason
- Settle a disagreement between team members

Don't add a decision log for:
- Decisions fully covered by guidelines (just follow the guideline)
- Visual taste (unless taste is hiding a systematic rule)
- Temporary workarounds you plan to fix

Categories:
- layout       Grid, density, placement, hierarchy decisions
- copy         Any word-level decision: labels, CTAs, status text, empty states
- pattern      Interaction flow, progressive disclosure, navigation
- component    How an existing component is used in a new context
- color        Semantic color assignments, exceptions to the color system
- data-viz     Chart type selection, axis decisions, color encoding in charts
- interaction  Trigger conditions, frequency, threshold-based behavior
- a11y         Accessibility exceptions or additions beyond WCAG defaults
-->

## Index

| id | date | category | screen | status | summary |
|---|---|---|---|---|---|
| | | | | | |

---

## Entry template

```
id: DL-[three digit number, sequential]
date: YYYY-MM-DD
category: layout | copy | pattern | component | color | data-viz | interaction | a11y
screen: [name of the screen or feature]
status: settled | provisional

**Context**
[1–3 sentences: what design problem were you solving? what made it non-obvious?]

**Decision**
[1–2 sentences: what did you decide?]

**Why**
[The actual reasoning. Be specific. "Because it looks better" is not useful.
"Because users see this weekly and alarm UI damages the relationship" is useful.]

**Rejected alternatives**
- [Alternative A] — rejected because [reason]
- [Alternative B] — rejected because [reason]

**Agent instruction**
→ [Written as a direct rule. Start with "Apply", "Never", "Prefer", or "When X, do Y".]
→ [Add a second rule if needed. Each rule is one line.]

**Related**
guidelines.md §[section] / DL-[other entry id]
```

---

<!-- Append new entries below this line. -->
