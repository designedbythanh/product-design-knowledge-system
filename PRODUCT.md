# [Product]

> **Role: `product`.** Read first by every skill. The fastest way to fill this file is to run `product-context`: it asks what's missing, finds the docs you already have, and writes this file. Filling it by hand works too.
>
> The guidance blocks (`> ...`) tell you what to write. Delete them as you go. Write `Not provided` for anything you don't know yet, never a guess.

## Sources

> The index. One row per role that already has a home somewhere: your own design system file, an ADR folder, a design note per feature. Skills go there instead of asking you. A role with no row uses this template's default file.
>
> - **Status**: `primary` (the source of truth for that role, one per role) or `supporting`.
> - **Verified**: the date you last confirmed the path is current. A skill that sees in git that the file changed since then will ask whether it still holds (not for briefs: they change by design).
>
> **If missing:** skills only know this file and the default ones, and ask for everything else.

| Role | Path | Status | Verified |
|---|---|---|---|
| guidelines | guidelines.md | primary | YYYY-MM-DD |
| decisions | decision-log.md | primary | YYYY-MM-DD |
| feature | briefs/<slug>.md | primary | YYYY-MM-DD |
| evidence | [Figma library, Storybook or tokens file link] | primary | YYYY-MM-DD |

## Product and users

> **Write**, in bullets:
> - What it is, in one sentence. What it replaces.
> - What it is **not**: features people assume exist, limits of any AI feature (no memory? no real-time?). Your support tickets are the best source.
> - Who uses it (2–4 user types: role, goal, technical fluency) and in what situation: device, frequency, interruptions.
> - Mark anything not backed by research `⚠️ Not validated`.
>
> **Don't write** marketing copy. "Empowers teams to…" tells a skill nothing.
>
> **If missing:** `persona-pretest` and `design-critique-facilitator` ask you to describe the user every time.

## Roles and permissions

> Who can see and change what. Include the gaps you know about.
>
> **If missing:** `edge-case-finder` checks permissions against generic cases (unauthorized users, role conflicts) instead of your real roles.

## Vocabulary

> The words the product uses for its key concepts, and the words to avoid.
>
> **If missing:** skills use whatever words came up in the conversation, which may not be the product's.

## Domain

> *Optional.* Data definitions, business rules, integrations, metric definitions: what an agent needs so it doesn't invent them. Link out instead if they're documented elsewhere.

## Known issues live in

> Where the team tracks known issues: a tracker project, a dev review doc. A link.
>
> **If missing:** skills can't tell a known issue from a new one, and present old problems as discoveries.
