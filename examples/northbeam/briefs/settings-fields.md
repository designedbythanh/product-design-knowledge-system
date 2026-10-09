# Settings › Fields

Spec: None

## Goal
- Creating a field and choosing where it shows should take one trip, not two (today: create it in "Lists", switch it on in "Pipeline columns")

## Stage
- Prototype

## Decided
- Fee models are not rows of the fields table; they open from the Fee row, in their own drawer · 2026-09-27 · designer
- Rejected: fee models as a flagged row of the fields table · they're pricing rules, not a field · 2026-09-27
- The scope shows next to every control it affects · see DL-001

## Open
- Two pages with links (A), or one merged page (B)? Taken to the team: it changes the product, not only the design
- Whether the "New field" form should take values and stages at creation

## Worries
- People who maintain lists (Sam, ops coordinator) stop finding them once they don't have their own page
- Rows don't say what kind of field they are; the list icon isn't explained

## Log

### 2026-09-26 · five-whys-root-cause
- Root need: one trip from creating a field to seeing where it shows
- From reading the code, not the whys: a new field is already on in Screening and Interview; the second trip exists because nothing says so
- Cheaper options than merging: ask where the field shows when creating it, show it in the field's drawer, link the two pages

### 2026-09-26 · decision-rationale
- B (one page) 39, A (two pages with links) 33, five criteria weighted equally
- Scope safety was one criterion among five: 8 against 7
- Leaning B, not decided: taken to the team

### 2026-09-27 · cross-industry-steal
- Best steal: fee models as a flagged row, like a control account in a ledger
- Rejected by the designer, see Decided

### 2026-09-27 · persona-pretest
- Tested findability, as asked: Sam finds the lists on the merged page
- Bug on the existing page: a new fee model gets a default unit nobody chose, and saves wrong. Logged in NB
