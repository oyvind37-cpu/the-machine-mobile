# Project Finch — Cold Case AI (prototype specification)

## Purpose
Research public historical sources, compare events and construct auditable timelines. The tool is a research assistant, **not** a police investigation or identity-tracing system.

## First case: Jørn Berntzen
Scope: Oslo 2000–2005, with focus on 18–20 August 2004. Do not imply any other case is connected without documented evidence.

### Initial verified leads
- VG chapter 1: https://www.vg.no/spesial/2018/pappaen-som-forsvant/kap1/
- VG chapter 2: https://www.vg.no/spesial/2018/pappaen-som-forsvant/kap2/
- AMK call: 19 August 2004 at 22:24, reported by VG from archive. Separate reported location, caller identification and physical eyewitness observations.
- Oslo Police Trend Report 2012 (historic robberies): https://fido.nrk.no/f444d6eb4fbde1991769d878089801958e7718a3115f87d1d9d19693b57ae7b4/Vedlegg_1549.pdf
- Government 2004 crime context: https://www.regjeringen.no/no/dokumenter/stprp-nr-1-2004-2005--2/id297184/?ch=2
- Kripos homicide data: https://www.politiet.no/om-politiet/tall-og-fakta/drapsoversikt

## Data schema
Each event: id, date_start, date_end, location_text, event_type, description, source_url, source_title, source_date, evidence_type (primary/secondary), confidence (confirmed/reported/unverified), notes, case_id.
Each proposed connection: event_ids, basis (shared time/place/documented association), supporting_source_urls, status (hypothesis/verified/rejected). **Temporal or geographic overlap alone is not a link.**

## Modules
1. Source register: URLs, dates, quotes limited to short extracts, archived references, provenance.
2. Timeline: precise timestamps, uncertain intervals, conflicting accounts.
3. Historical context: homicides, missing persons, robberies, theft, policing 2000–2005.
4. Comparison engine: document-level similarities only; no guilt scores, suspect rankings, or face matching.
5. Review queue: human confirmation before publishing claims.
6. Export: source-linked CSV/JSON and a printable research memo.

## Safeguards
Use public and lawfully obtained sources only. Do not scrape private accounts, track living people, perform face recognition, infer identities from photos, or publish sensitive private information. Treat unverified reports as unverified. Preserve corrections and an audit trail. Any credible new evidence should go to police, not public accusation.

## Next implementation
Build mobile-friendly case dashboard with source table, event timeline, filters (year, type, evidence level), and context panel. Seed only documented records; keep unanswered questions explicitly open.
