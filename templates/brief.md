# [Feature]

> **Role: `feature`.** Copy this file to `briefs/<feature-slug>.md`, one per feature. This is the most important file for the skills: it holds your **intent**, which no skill can infer from a spec or a screen. `product-context` writes it from what you tell it; later skills add to its Log.
>
> Keep the core short: facts in bullets. Write `Not provided` for what you don't know yet.

Spec: [link to the PRD or ticket, or "None"]

> The spec lives where the team keeps it. Link it, don't copy it: a copy goes stale. When brief and spec disagree, the brief wins on intent and the spec wins on what was committed to the team, and skills report the gap.

## Goal

> What the feature is for, in one or two lines. The user's problem, not the solution.

## Stage

> Spec only / prototype / staging / production. `edge-case-finder` ranks its findings against it: a prototype shortcut isn't a launch blocker.

## Decided

> One line per decision. Skills won't reopen these.
>
> - [decision] · [date] · [who]
> - Rejected: [suggestion] · [why] · [date]
>
> A decision that applies beyond this feature belongs in `decision-log.md`. Move it there and keep a pointer: `[decision] · see DL-012`.

## Open

> Questions still being decided. Skills also add here any disagreement they find between your sources.

## Worries

> What made you ask for a review. `design-critique-facilitator` answers these first.

## Log

> Skills append a dated entry here: what they found or decided. Never rewrite or delete entries; the next skill or session starts from them.

<!--
Optional sections, below the Log, when the feature needs more than the core:

## Compositions   which components, in what order
## States         every state the feature can be in
## Edge cases     what was found and how it's handled
## Flows          step by step
## Spec           only if the spec has no other home

When a rule here would apply to other features (a new empty-state pattern, a copy rule), move it into guidelines.md and leave a pointer.
-->
