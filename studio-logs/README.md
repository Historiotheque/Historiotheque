# Studio Logs

Master log location for the Historiotheque operation. Cross-project research,
discourse, and admin sessions live here. Sessions belonging to a single project
live in that project's own `studio-logs/` (e.g. `WhatIsCubism/studio-logs/`).

## Spec

Format follows [studio-log-spec_v1.3.md](../docs/new-documentation/studio-log-spec_v1.3.md): one file per
session, named `YYYY-MM-DD-HHMM-<slug>.md` (24h local time), YAML frontmatter,
fixed section order. `Decisions` and `Next actions` are mandatory — a session with
no decisions recorded is a session not yet understood.

## Session types

- `studio` — Images / Sounds / Texts work (the artwork itself)
- `research` — labnotes: research-oriented processes and practices
- `field` — fieldwork and field recordings
- `admin` — operational/administrative sessions
- `discourse` — video discourses and other public-facing sessions

## How to add a log

Say **"log this session"** (or "add a studio log") and describe what you did,
decided, hit, and made. Backfilled entries are marked `reconstructed: true` with
a provenance note and approximate timestamps.

## Index (newest first)

| File | Date | Session |
|---|---|---|
| `2026-09-23-2315-atmospherics-theory-scaffold.md` | 2026-09-23 | AtmosphericsTheory repo scaffold: bibliography filed, Work-Schema-framed structure, zip built (empty-folder and hidden-dotfile upload fixes), commit text, project-list entries, naming decision |
| `2026-09-23-1747-cubism-art-operation-video-discourse.md` | 2026-09-23 | 26-min video discourse: Cubism as an Art Operation — what the records show and don't; Picasso/Braque procedures undocumented; software-dev logging best practices imported; the independent-researcher's publication paradox |
| `2026-09-23-1400-video-discourses-treasure-open-source-artist.md` | 2026-09-23 | Two walk-and-talk video discourses (Picasso/Braque procedures undocumented; the "Treasure" archive analogy; Open Source Artist coinage); first published to Instagram as a Reel |
| `2026-09-23-1000-logging-infrastructure-goes-live.md` | 2026-09-23 | Logging infrastructure goes live on GitHub: 6 refcards uploaded, index.md rows added, studio-logs batch uploaded, spec placed, dead link fixed, upload protocol established |
| `2026-09-23-0830-art-ops-ecosystem-documentability.md` | 2026-09-23 | RQ-2026-014→017, ArtOps Ecosystem doc, Picasso/Warhol documentation comparison, non-monotonic documentability thesis, 12-folder Research registry snapshot |
| `2026-09-23-0130-cubism-studies-pdf-readthrough.md` | 2026-09-23 | Cubism Studies PDF (2002–2003 notes) read-through; structure mapped; gleanables cataloged per instrument; 2002–2003 "Metaphysic of Art Movements" provenance finding |
| `2026-09-23-0000-whatiscubism-scaffold.md` | 2026-09-23 | WhatIsCubism repo scaffold build (README, schema, 13 audit cards, positions map, timelines, bibliography) |
| `2026-09-22-2000-art-operation-schema-audit-apparatus.md` | 2026-09-22 | Art Operation Schema v0.1, evidence-audit + positions-map instrument, RQ-2026-013 |
