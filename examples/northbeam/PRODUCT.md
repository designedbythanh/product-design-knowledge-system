# Northbeam

## Sources

| Role | Path | Status | Verified |
|---|---|---|---|
| guidelines | guidelines.md | primary | 2026-10-02 |
| decisions | decision-log.md | primary | 2026-10-02 |
| feature | briefs/<slug>.md | primary | 2026-10-02 |
| evidence | Not provided | | |
| issues | Tracker, project NB | primary | 2026-10-02 |

## Product and users
- Hiring tool for recruiting agencies: candidates move through a pipeline (Sourcing, Screening, Interview, Offer) for each client the agency recruits for
- Replaces the spreadsheets agencies keep per client
- Not: an applicant tracking system for the client's own HR team; clients don't log in
- Not: invoicing. Northbeam stores fee models, the agency's billing tool calculates invoices from them
- Recruiters: daily, on a laptop, between calls. Move candidates, fill in fields
- Ops coordinators: set up a new client about once a month. Comfortable with Excel, not with settings pages; keep the agency's dropdown lists in an Excel tab
- ⚠️ Not validated: how often recruiters change settings themselves. Written from support tickets, not research

## Roles and permissions
- Admin: everything, including who has which role
- Ops coordinator: all settings, for the agency and any client, including lists and fee models
- Recruiter: switches fields on or off per stage, for the agency or a client; sees lists and fee models without changing them
- Whether a recruiter can create a field: Not provided

## Vocabulary
- **field**: a piece of information on a candidate or an application (Seniority, Notice period). Avoid "column", except in "Pipeline columns", the old page name
- **list**: the values a field can take (LinkedIn, Referral, Job board). Avoid "picklist", "options"
- **agency / client**: the agency is our customer; a client is a company the agency recruits for. Settings exist at both levels
- **fee model**: how the agency charges a client for a hire (Contingency %, Retained, Hourly). A pricing rule, not a field

## Domain
- Settings at agency level are the default every client inherits; a client can override a field's visibility, never its definition
- A new field is switched on in Screening and Interview by default

## Known issues live in
- Tracker, project NB
