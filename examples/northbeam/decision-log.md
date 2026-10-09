# DESIGN DECISION LOG — Northbeam

## Index

| id | date | category | screen | status | summary |
|---|---|---|---|---|---|
| DL-001 | 2026-09-12 | interaction | Settings (all) | settled | Show the scope next to every control it affects |

---

id: DL-001
date: 2026-09-12
category: interaction
screen: Settings (all pages with an Agency / client scope)
status: settled

**Context**
An ops coordinator changed a field at agency level while thinking they were editing one client. Every client inherited the change. The scope selector was visible at the top of the page, but far from the control being changed.

**Decision**
Every control whose change depends on the scope shows the scope next to it ("Agency · all clients" or the client's name). The Undo toast names the scope too.

**Why**
Agency-level changes are rare but reach every client at once, and the person making them is usually setting up one client.

**Rejected alternatives**
- Bigger scope selector at the top — rejected because the incident happened with the selector visible, just not near the control
- A confirmation dialog on every agency-level change — rejected because setup means many changes in a row; a dialog per switch gets clicked through without being read

**Agent instruction**
→ When a settings change can apply at agency level, check the scope is visible next to the control, not only at the top of the page.
→ Treat a scope-dependent control without its scope in view as a blocker, not a suggestion.
→ When comparing options, treat this as a condition every option must meet, not one score among others.

**Related**
guidelines.md › Patterns / briefs/settings-fields.md
