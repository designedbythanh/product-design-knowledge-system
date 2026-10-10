# Product & Design Knowledge System

Templates for the context AI tools need to give useful product design feedback: what your product is, who uses it, the rules a design is judged against, and what you intend for each feature. Written so a person can read them and an AI skill can follow them without guessing.

by [Thanh Nguyen](https://www.linkedin.com/in/thanh2-nguyen/) · Product Designer, AI-native workflows · [Substack](https://designedbythanh.substack.com)

Implements context contract 1.0 of the [AI Skills Library for Product & Design Teams](https://github.com/designedbythanh/ai-skills-library-product-design/blob/main/CONTEXT-CONTRACT.md).

## The one rule

**Write down what only you know. Point to what already has a home.**

Your intent for a feature, the decisions you made and why, the words your product uses, the rules you'd fail a design on: nobody can infer these, so they go here. Your design system, your PRD, your tickets already live in Figma, Notion or a tracker. Copying them here makes a second version that goes stale, and an AI tool reading the stale one gives confident, wrong feedback. Link them instead.

## Get started

1. **Run `product-context`** from the [skills library](https://github.com/designedbythanh/ai-skills-library-product-design) in your project. It asks what's missing, finds the docs you already have, asks you to confirm each one, and writes `PRODUCT.md` and a first brief using these templates. Without the skills, copy the templates and fill them by hand.
2. **Look at the [Northbeam example](examples/northbeam/)** to see what "filled in" looks like.
3. **Fill the minimum**: `PRODUCT.md` (product, roles, vocabulary), one brief, and the review checklist in `guidelines.md`. Everything else can wait until a skill asks for it.

Write `Not provided` for what you don't know yet, and `⚠️ Not validated` for what you're assuming. A blank tells a skill to ask; a guess sends it the wrong way.

## What's here

| File | Role | Holds | Read by |
|---|---|---|---|
| [`PRODUCT.md`](PRODUCT.md) | `product` | What the product is and isn't, users, roles, vocabulary, and **Sources**, the index of where everything else lives | every skill |
| [`templates/brief.md`](templates/brief.md) → `briefs/<feature>.md` | `feature` | Your intent for one feature: goal, stage, decided, rejected, open, worries, and a Log the skills add to | every skill |
| [`guidelines.md`](guidelines.md) | `guidelines` | Values, patterns, states, AI features, microcopy, review checklist. Each section says which skills use it | critique, edge cases, acceptance criteria, … |
| [`decision-log.md`](decision-log.md) | `decisions` | Decisions that apply across features, with why and what was rejected | every skill (as decided) |
| [`evidence/`](evidence/) | `evidence` | Annotated screens, component inventory, or just links to them | critique, persona pretest |

## Already have your own docs?

Keep them where they are. A `DESIGN.md`, an ADR folder, a design note per feature, a tokens file: list each one in `PRODUCT.md` › Sources, with the role it plays. Skills read your files through that index and only fall back to these templates for roles you haven't listed. `product-context` builds the index for you and asks before adding anything.

## How the skills use it

- They read `PRODUCT.md` first, then only the sources and `guidelines.md` sections the task needs.
- They start their answer with `Context used:`, so you see which files they relied on.
- When two sources disagree, the more specific one wins (what you say now, then the brief, then decisions, then guidelines, then product), and the skill tells you about the disagreement instead of picking silently.
- They write only to a brief: a dated entry in its Log, and a line under Open when two sources disagree. Product-level files change only when you change them.

The full rules are in the [context contract](https://github.com/designedbythanh/ai-skills-library-product-design/blob/main/CONTEXT-CONTRACT.md).

## Keeping it alive

- **Append, don't edit, decisions.** A changed decision is a new entry that supersedes the old one.
- **Promote, don't duplicate.** A feature decision that turns out to apply elsewhere moves to `decision-log.md`; a feature rule that applies elsewhere moves to `guidelines.md`. The brief keeps a pointer.
- **One primary source per role.** Mark it `primary` in Sources. When files disagree, the primary one wins.
- **Re-verify what moved.** When a source changes, update its Verified date once you've checked it still holds.
- **5 minutes beats perfect.** A rough entry today is worth more than a polished one never written.

## Upgrading from v1

v1 had five layers. In v2:
- **Layer 1, guidelines**: product facts (what it is and isn't, users, domain) moved to `PRODUCT.md`. The design system section is gone: link your design system in Sources. Sections now have fixed headings instead of numbers.
- **Layer 2, decision log**: unchanged. Feature-only decisions now go in the brief.
- **Layer 3, modules**: replaced by briefs. A brief has a short core and optional sections (compositions, states, edge cases, flows) for features that need more.
- **Layer 4, agent interface**: removed. The skills library is the agent layer: each skill defines its inputs and output, and names the skill that usually comes next.
- **Layer 5, evidence**: unchanged.

## License

[CC BY 4.0](LICENSE). Use, adapt, and share freely, including commercially, with attribution.
