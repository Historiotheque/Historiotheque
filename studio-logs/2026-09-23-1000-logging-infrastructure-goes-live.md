---
date: 2026-09-23
time_start: "10:00"
time_end: "11:00"
timezone: America/Toronto
season: autumn-of-atonement
project: [historiotheque]
stream: [text]
session_type: admin
workspace: historiotheque
refcards: [RC-2026-0007, RC-2026-0008, RC-2026-0009, RC-2026-0010, RC-2026-0011, RC-2026-0012]
tags: [new-documentation, methodology, github, refcards, studio-logs, admin]
related:
  - studio-logs/2026-09-23-0830-art-ops-ecosystem-documentability.md
---

## What I did

Brought the operation's documentation infrastructure live on GitHub. Uploaded the 6
new refcards (RC-2026-0007–0012, canonical numbering following the repo's 0001–0006)
to `Historiotheque/Refcards/cards/RC-2026/` and added the 6 entry-point rows to the
repo's top-level `index.md`. Uploaded the studio-logs batch (README + 4 entries) to
`Historiotheque/Historiotheque/studio-logs/` and the studio log spec to
`docs/new-documentation/studio-log-spec_v1.0.md`, per the root README's repo map.
Diagnosed and fixed a dead spec link in the studio-logs README (uploaded copy
predated the path correction).

## Decisions

- **Decision:** Refcards live in the Refcards repo, not the Historiotheque repo and
  not inside studio logs; logs cite cards by ID. / **Reason:** Separate systems,
  linked by citation — the spec's design.
- **Decision:** One log stream for everything; session type + tags do the sorting
  (`research` + `methodology` for methods work, no separate "methodology log").
  / **Reason:** Fewer systems to maintain; the pilot entries are the template.
- **Decision:** Commit history + commit messages are the micro-tracking layer on
  GitHub; studio logs are the session layer; specs are the how-layer. / **Reason:**
  Three layers, one practice — the New Documentation documenting itself.
- **Decision:** Upload protocol going forward — every file I create or change gets
  flagged NEW or MODIFIED-replace, with its System Files path and repo destination.
  / **Reason:** He uploads everything himself, in batches he sequences.

## Problems and friction

The dead link came from an uploaded README that predated the spec-path correction —
diagnosed from screenshots by checking the link's resolved address. The Refcards
repo's `index.md` exists only on GitHub (no local copy), so new rows were drafted
from pasted contents. The seven workflow files (`wf-2026-001`–`007`) don't exist
anywhere — confirmed by search; they're TBD rows in the index by design, to be
written as needed.

## Ideas and sketches

- `seed`: The `workflow:` frontmatter field for studio logs (referenced in
  wf-index.md, not yet in spec v1.0) — propose it formally the first time a
  workflow run gets logged.
- `seed`: Write the workflows as they're actually run, starting with whichever comes
  next — no seeding the folder with empty files.

## Research and references

Repo-structure spec v1.0 (own); Workflows Folder Spec v1.0 (own); root README repo
map (own). No external sources.

## Artifacts produced

- 6 refcards live in `Historiotheque/Refcards`; `index.md` updated.
- `studio-logs/` (5 files) + `docs/new-documentation/studio-log-spec_v1.0.md` live
  in `Historiotheque/Historiotheque`.

## Next actions

- [ ] Write the seven workflows one at a time as they're needed; upload wf-index.md
  when seeding `workflows/`. (me)
- [ ] Keep logging per session: experimentation always; methodological/admin work
  when there's a real delta; sub-15-minute clerical bits batched or left to commit
  messages. (me)
