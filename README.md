# Product & Design Knowledge System

A layered documentation architecture for product designers and teams who want their design knowledge to be usable by both humans and AI agents (Claude, Cursor, Figma Make, etc.).

This framework comes from building a real design knowledge system (15+ sections, 8+ decision logs, and 4 in-depth modules). Adapted into a template you can make your own, whatever product you're working on.

**Who it's for:** product designers, design leads, and design-forward PMs working on B2B SaaS products.

**What you get:** a template structure — not content. You fill in your product's truth. The system tells you *where* and *how*.

by [Thanh Nguyen](https://www.linkedin.com/in/thanh2-nguyen/) · Product Designer, AI-native workflows · [Notion version](https://www.notion.com/@thanh-nguyen) · [Substack](https://designedbythanh.substack.com)

## Why this exists

Most product design documentation fails in one of two ways:

1. **Too abstract**: values and principles that don't tell anyone what to actually do
2. **Too scattered**: decisions buried in Slack threads, Figma comments, and individual memory

This framework solves both. It gives **every decision a home**, a format, and an instruction that an AI agent can follow without interpretation.

The output is a **living knowledge system** — not a one-time doc — that gets more useful the longer you maintain it.

## Get started

Click **Use this template** at the top of this page to copy the structure into your own repo, then point your AI tool at these files.

```
guidelines.md                        Layer 1 — Master Guidelines
decision-log.md                      Layer 2 — Decision Log
modules/                             Layer 3 — Deep-Dive Modules
  _TEMPLATE.md
agents/                              Layer 4 — Agent Interface
  agent-roles.md
  routing-logic.md
  output-schema.example.json
evidence/                            Layer 5 — Evidence
  figma-component-inventory.md
  annotated-screens.md
```

## The Five-Layer Architecture

| Layer | What it holds | Role | Principle |
|---|---|---|---|
| **1 — [Master Guidelines](guidelines.md)** | Product · Design system · Patterns · Microcopy | Single source of truth. Every other layer references this. If something is not in guidelines.md, it doesn't exist as a system rule. | Markdown. Machine-readable. 15–20 sections. ~1500–2500 lines for a mature product. |
| **2 — [Decision Log](decision-log.md)** | Judgment calls · Rejected alternatives · Rules | Append-only journal of non-obvious judgment calls. The "why" behind the decisions that guidelines compress into rules. | This file is never edited — only appended. Old entries are settled; new entries can supersede them but never replace them. |
| **3 — [Deep-Dive Modules](modules/)** | Feature docs · Data models · Composition specs | When a feature or domain is too complex for a guidelines section, it gets its own module. These are merged back into guidelines when stable. | A module exists as a standalone file only while it's being actively written. Once stable, it merges into the relevant guidelines section and the standalone file is deprecated. |
| **4 — [Agent Interface](agents/)** | Agent roles · Routing logic · Output schemas | Makes your knowledge system usable by AI agents without extra explanation. Tells agents what they are, what they see, what they produce. | **Build this after** your Layer 1 and Layer 2 are stable. Building Layer 4 too early creates specs for a system that doesn't exist yet. |
| **5 — [Evidence](evidence/)** | Figma inventory · Annotated screens · Screenshots | The grounding layer. What agents consult when they need to recognize a component or verify a pattern is real. | **Build this incrementally.** Don't try to document all screens at once — start with the 5 most frequently designed screens. |

**Reading order for agents**: Layer 1 → Layer 2 → Layer 3 → Layer 4 → Layer 5
**Writing order for humans**: Start at Layer 1, add Layer 2 entries as you work, pull modules into Layer 3 when things get long.

## Starter checklist

**Layer 1 — Guidelines**
- [ ] §1 Product definition written
- [ ] §2 Explicit scope boundaries written
- [ ] §3 Product values with concrete examples
- [ ] §4 Design values as testable checklists
- [ ] §5 Design system: color + typography + spacing + key components
- [ ] §6 User context: user types + usage moments
- [ ] §7 Core UX patterns: empty, error, loading, drill-down
- [ ] §9 Microcopy: tone rules + golden examples table
- [ ] §12 Design review checklist (at least 15 items)

**Layer 2 — Decision Log**
- [ ] File created with header + entry template
- [ ] At least 5 real entries logged
- [ ] Entry index table maintained
- [ ] Each entry has an agent instruction

**Layer 3 — Deep-Dive Modules**
- [ ] Identified which features need a module
- [ ] At least 1 module written for your most complex feature
- [ ] Module status marked (Draft / Stable / Merged)

**Layer 4 — Agent Interface**
- [ ] Agent roles defined (even if just 2–3 agents)
- [ ] Routing logic drafted
- [ ] At least 1 output schema defined

**Layer 5 — Evidence**
- [ ] 3–5 key screens annotated
- [ ] Figma component inventory started (even if partial)

## What to build first

If you're starting from zero:

- **Week 1**: Write §1, §2, §3, §4 of guidelines.md. These are the foundation. Everything else depends on them being clear.
- **Week 2**: Write §5 (design system) and §12 (review checklist). Now you have something an agent can use immediately.
- **Week 3 onward**: Write §7 (patterns), §9 (microcopy), and start logging decision-log entries as you do real work.
- **When stable**: Write Layer 4 (agent interface) to make the whole system orchestratable.

## Maintenance rules

These rules keep the system alive and useful. Without them, it becomes stale documentation.

- **The append rule** — Decision log entries are **never edited** — only new entries are added. If a decision changes, add a new entry that references and supersedes the old one. Never delete the old entry.
- **The merge rule** — Deep-dive modules (Layer 3) are merged into guidelines.md (Layer 1) when stable. The standalone file is marked deprecated. The canonical version lives in one place.
- **The single source rule** — One file is primary. Everything else is supporting. When they conflict, the primary file wins. Make the primary file explicit in your system header.
- **The warning rule** — Unvalidated assumptions are marked `⚠️ Not validated — written from inferred context`. Agents must not treat assumptions as settled facts.
- **The 5-minute rule** — Decision log entries don't need to be polished. A rough entry written in 5 minutes is 10× more valuable than a perfect entry never written. Quantity beats polish.

## Related

- [AI Skills Library for Product & Design Teams](https://github.com/designedbythanh/ai-skills-library-product-design): 15 structured AI skills, Discovery → Shipping

## License

[CC BY 4.0](LICENSE). Use, adapt, and share freely, including commercially, with attribution.
