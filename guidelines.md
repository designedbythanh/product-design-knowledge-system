*If something is not clearly covered here, say: "Not specified in guidelines.md."*

# [Product] — Design Guidelines

> **Layer 1 — Master Guidelines.** Single source of truth. Every other layer references this. If something is not in guidelines.md, it doesn't exist as a system rule.
>
> Markdown. Machine-readable. 15–20 sections. ~1500–2500 lines for a mature product.
>
> The guidance blocks (`> ...`) under each section tell you what to write. Replace them with your product's truth.

---

## §1 — What [Product] Is

> *2–3 paragraphs. The product in plain language. What it replaces, what it enables.*
>
> **Write**:
> - One-sentence product definition
> - The core workflow it supports (weekly? ad-hoc? mission-critical?)
> - Primary entry points / sections (table format: Section | What it does)
>
> **Do not write**: Marketing copy. "Empowers teams to..." is not useful to an agent.

| Section | What it does |
|---|---|
| | |

---

## §2 — What [Product] Is NOT

> *The explicit scope boundary. This section prevents agents from hallucinating features that don't exist.*
>
> **Write**:
> - A bulleted list of what the product does not do
> - For AI features: explicit capability limits (no memory? no forecast? no real-time?)
>
> **Tip**: Read your support tickets. The most common misunderstandings are your §2.

---

## §3 — Product Core Values

> *The "why" behind product decisions. Not generic (no "we value quality"). Specific to your domain.*
>
> **Each value should have**:
> - A name
> - A one-paragraph definition
> - 2–3 concrete product examples that prove it

### 3.1 [Value Name]

[Definition paragraph]

- [Feature A] demonstrates this by [specific behavior]
- [Feature B] demonstrates this by [specific behavior]

---

## §4 — Design Core Values

> *How design decisions get made. Not "we believe in simplicity" — but "a screen is clear when [checkboxes]".*
>
> **Each value should have**:
> - A name
> - A checklist definition (3–5 items, phrased as testable conditions)

### 4.1 Clarity

A screen is "clear" when:
- [ ] There is a single dominant question it answers
- [ ] The primary action (if any) is discoverable without reading instructions
- [ ] Labels and units are always explicit — never relative ("this week") without dates

---

## §5 — Design System Reference

> *The component/token layer. What exists. Not what should exist.*

### §5.1 Color system
> Palette structure.

### §5.2 Typography
> Type scale, weight rules, line-height system.

### §5.3 Spacing
> Base unit, spacing scale, density variants.

### §5.4 Components
> Key components with states, variants, when to use / when not to use.

#### [Component Name]
**When to use**: [condition]
**When NOT to use**: [condition]
**States**: [default | hover | active | disabled | loading | error | empty]
**Variants**: [list]
**Key constraints**: [max items, layout rules, size limits]

### §5.5 Compositions
> Complex multi-component patterns (cards, empty states, drill-downs, forms).

---

## §6 — User Context

> *Who uses this, when, and in what state of mind. This shapes every copy and layout decision.*
>
> **Include**:
> - 2–4 user types (role, goal, technical fluency)
> - Usage moments (daily? weekly? emergency?)
> - What they see before they arrive on each screen
> - What they need to do next
>
> ⚠️ **Mark unvalidated assumptions with a warning**: *"The following scenarios are hypothetical — not validated user research."* Agents should not treat assumptions as facts.

---

## §7 — Core UX Patterns

> *Reusable interaction logic. Not components (that's §5) — behaviors.*
>
> **Each pattern should have**:
> - Pattern name
> - Trigger (when does this pattern apply?)
> - Rules (numbered, unambiguous)
> - Edge cases
> - What NOT to do
>
> **Common patterns to document**:
> - Empty states (template: "[What's missing]. [One action sentence].")
> - Error states (recoverable vs. unrecoverable; copy tone)
> - Loading states (skeleton vs. spinner rules)
> - Drill-down / progressive disclosure (max depth, back navigation)
> - Confirmation dialogs (when required vs. not)
> - Filters and scoping (how state persists across sessions)

---

## §8 — AI Feature Guidelines *(skip if no AI features)*

> *For products with AI: the hardest section to keep honest.*
>
> **Include**:
> - Map of every AI feature (table: Feature | What it does | What it cannot do)
> - Role clarity: where does AI make decisions vs. where does human decide?
> - Explainability requirements: does every AI output need an explanation?
> - Uncertainty handling: what happens when the AI doesn't know?
> - Tone rules for AI-generated copy

| Feature | What it does | What it cannot do |
|---|---|---|
| | | |

**Mandatory statements per AI feature**:

```
[Feature name]
- Can: [explicit list]
- Cannot: [explicit list]
- Requires human review before: [list of actions]
```

---

## §9 — Microcopy

> *The smallest words. The hardest to get right. The easiest to get wrong.*

### §9.1 Tone rules
> 3–5 adjectives with definitions and examples.

### §9.2 Patterns
> Copy templates for: empty states, errors, partial data, loading, status labels, confirmations, AI output.

### §9.3 Golden examples
> Table of real copy: Bad | Good | Why.

| Context | ❌ Don't | ✅ Do | Why |
|---|---|---|---|
| Empty dashboard | "No data found!" | "No reports yet. Create your first report." | Actionable, not alarming |
| Error state | "Something went wrong" | "Couldn't load campaigns. Check your connection and try again." | Specific, recoverable |

### §9.4 Things to never write
> Banned phrases and patterns.

---

## §10 — Examples & Non-Examples *(optional but high-value)*

> *Real annotated screens or annotated descriptions. The most useful section for AI agents doing design review.*

### [Feature or Pattern]

**✅ Good example**
[Screenshot reference or description]
Why it works: [2–3 sentences]

**❌ Bad example**
[Screenshot reference or description]
What's wrong: [2–3 sentences]
What to do instead: [1 sentence]

---

## §11 — States Reference

> *Every UI state for every major screen. Agents need this to know what to design when things go wrong.*
>
> **States to document per major screen**:
> - Empty (first time vs. configured but no data)
> - Loading (skeleton structure)
> - Partial (some data, some missing)
> - Error (recoverable vs. fatal)
> - Limited (permission-gated)
> - Success / complete

---

## §12 — Design Review Checklist

> *Run this before shipping. Agents use this to evaluate designs. You use this in critique.*

### Core
- [ ] Single dominant question per screen
- [ ] No orphaned elements without labels
- [ ] All numbers have units

### States
- [ ] Empty state designed (first time AND no-data)
- [ ] Loading state uses skeleton, not spinner, for data-heavy views
- [ ] Error state includes recovery action

### Copy
- [ ] No exclamation marks in status labels
- [ ] No relative time without a date ("this week" → "May 1–7")
- [ ] AI-generated text is editable and dismissible

### Accessibility
- [ ] Text contrast ≥ 4.5:1 (WCAG AA)
- [ ] Color is never the sole signal — always paired with label or icon
- [ ] Touch targets ≥ 44×44px
- [ ] Font size ≥ 12px for any text users must read

---

## §13 — TODOs & Open Questions *(maintenance section)*

> *Screenshots needed, decisions unconfirmed, things waiting for data.*

### Screenshots needed
- [ ] [Screen name] — needed for §[section] — waiting on [person/milestone]

### Decisions unconfirmed
- [ ] [Decision] — written from inference — needs [person] to verify

### Open questions
- [ ] [Question] — blocking [section] — owner: [person]

---

## §14 — Domain Reference *(product-specific)*

> *The technical/domain knowledge agents need to not invent things. Data models, integrations, metric definitions.*
>
> **Examples by product type**:
> - **Analytics tool**: Metric definitions, dimension taxonomy, connector list, data freshness rules
> - **E-commerce**: Product taxonomy, pricing rules, inventory states
> - **Fintech**: Account types, transaction states, regulatory constraints
> - **Healthcare**: Term definitions, data sensitivity rules, workflow constraints
