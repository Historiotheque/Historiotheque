# Historiotheque Studio Log — Format Specification v1.0

*Derived from The New Documentation (April–May 2024). Drafted 2026-09-20.*
*The theory: the Open Source Artist documents in the light — continuously, publicly, reproducibly.*

---

## 1. Purpose

A studio log entry is an atomic, timestamped record of one work session in the Art Operation.
It exists so that any experiment in the practice can be **reproduced** — by the artist later,
or by anyone with a web browser. Logs are the ground truth; Declarations, Releases,
PROSPECTIVEs and RETROSPECTIVEs are built on top of them.

The logs are **separate from but linked to** the Refcards project. Refcards are physical
index cards (atomic knowledge units); log entries cite them by ID. Neither replaces the other.

## 2. File conventions

- **Location:** one `studio-logs/` directory per GitHub project repository, plus a master
  `studio-logs/` in the operation's root repo for cross-project sessions.
- **One file per session:** `studio-logs/YYYY-MM-DD-HHMM-<slug>.md`
  (24h time, local timezone; slug in kebab-case, e.g. `2026-09-20-1430-chronotopium-no12.md`).
- **Plain Markdown**, GitHub-flavored. YAML frontmatter at the top, fixed section order below.
  Omit any section that doesn't apply — but never omit *Decisions* and *Next actions*;
  a session with no decisions recorded is a session not yet understood.

## 3. Frontmatter

```yaml
---
date: 2026-09-20
time_start: "14:30"
time_end: "16:10"
timezone: America/Toronto
season: autumn-of-atonement         # <calendar-season>-of-<quality>, season first
project: [chronotopium-series]     # project slug(s), kebab-case
stream: [image]                    # image | sound | text | mixed
session_type: studio               # studio | field | research | admin | discourse
workspace: historiotheque          # where the work happened
refcards: [RC-2026-0142, RC-2026-0143]
tags: [assemblage, cardboard, first-pass]
related:
  - releases/5.1.0                 # links to declarations, releases, other logs
  - studio-logs/2026-09-18-1000-chronotopium-no11.md
---
```

**Controlled vocabularies** (extend as needed, but never ad hoc — propose additions in the log):

- `season`: the calendar season (spring | summer | autumn | winter, by solstice/equinox
  date) qualified by the moral temperature reading, in kebab-case, season first:
  `autumn-of-atonement`, `summer-cool`. Canonical defaults: `springtime-of-life`,
  `summer-of-the-heart`, `autumn-of-atonement`, `winter-of-the-soul`. (The `-of-joyful-being`
  variants are reserved for Seasons of the Heart project sessions.) One qualifier; further
  shades go in `tags` or the log body. Always set from the session date when the log
  is written — never carried over unexamined.
- `stream`: image, sound, text, mixed.
- `session_type`: studio, field, research, admin, discourse (a video discourse counts as a session).
- `project`: the project's kebab-case slug, matching its repo/directory name.

## 4. Body — fixed section order

### What I did
Plain account of the session, in the order it happened. Concrete verbs, concrete materials.
What was touched, cut, recorded, written, coded, moved, deleted.

### Decisions
Every decision taken, with the reason. Format: **Decision:** … / **Reason:** …
Decisions are the most valuable data in the log — this section is mandatory.

### Problems and friction
What resisted, what failed, what was confusing — and what was tried about it.
Unresolved problems stay open and are carried into *Next actions*.

### Ideas and sketches
New ideas that surfaced mid-session. Mark their status: `seed` (untested),
`sketch` (partially formed), `proposal` (ready to become a project or Refcard).

### Research and references
What was read, watched, listened to, consulted. Cite from the repository's BIBLIOGRAPHY.md
(see §8) by citation ID wherever the source is already logged; give a full Chicago-style
citation inline only for sources not yet in the bibliography, and flag them for entry.

### Feedback and collaboration
Who said what, where (platform, in person), and what changed because of it.

### Reproducibility notes
*Required for experimental sessions.* Materials, tools, settings, parameters, and the
step sequence — enough that the session could be re-run. Software versions, file paths,
instrument settings, paint mixtures, microphone placement: whatever the experiment
depended on goes here.

### Artifacts produced
One metadata block per artifact, typed by stream. Fields follow The New Documentation's
per-medium standards:

**Image:**
`title` · `description` · `dimensions` · `materials` · `techniques` · `date` · `file`

**Sound:**
`title` · `description` · `duration` · `instruments/tools` · `techniques` · `date` · `file`

**Text:**
`title` · `abstract` (1–3 sentences) · `keywords` · `citations` · `date` · `file`

### Next actions
Concrete, checkable. Each with an owner (usually: me) and, where known, a when.

## 5. Cross-referencing conventions

- **Refcards:** cite as `RC-YYYY-NNNN` (e.g. `RC-2026-0142`). The number is the card's own
  number in the Refcards project; the log never renumbers cards.
- **Other logs:** relative path links (`../2026-09-18-1000-chronotopium-no11.md`).
- **Official documents:** cite by type and identifier
  (`Declaration 2028–2029`, `Release 5.1.0`, `PROSPECTIVE 2026-10`).
- **Tags:** kebab-case, shared across logs and Refcards so both systems stay searchable
  as one index.

## 6. Session skeleton (copy-paste)

```markdown
---
date: YYYY-MM-DD
time_start: "HH:MM"
time_end: "HH:MM"
timezone: America/Toronto
season:
project: []
stream: []
session_type:
workspace: historiotheque
refcards: []
tags: []
related: []
---

## What I did

## Decisions

## Problems and friction

## Ideas and sketches

## Research and references

## Feedback and collaboration

## Reproducibility notes

## Artifacts produced

## Next actions
```

## 7. How to add a log (the working protocol)

Tell Oracle: **"add a studio log"** (or "log this session") and describe the session —
what you did, decided, hit, and made. Oracle drafts the entry in this format, files it,
and reads it back for correction before it's final. The trigger phrase is the whole interface.

## 8. Citations and the running bibliography

**Standard: Chicago Manual of Style, 17th edition.** It is the standard in art history,
history, and philosophy; it handles books, archival sources, artworks, and digital/online
sources — the full range of an interdisciplinary art-research practice.

- In **studio logs and Refcards**: Chicago **author-date** (compact inline citations).
- In **official documents** (Declarations, Releases, PROSPECTIVEs, RETROSPECTIVEs):
  Chicago **notes-bibliography**.

Each repository keeps a running `BIBLIOGRAPHY.md` — one entry per source, each with a
stable citation ID (`BIB-2026-001`, …). The bibliography is built **slowly and cumulatively**:
every book read, every paper consulted, gets logged as it comes up. Log entries cite
sources by ID; the full Chicago entry lives in one place.

**To add a citation:** tell Oracle **"add a citation"** and name the source (author, title,
and whatever else you remember — Oracle fills in the rest and asks before guessing).
Oracle formats it in Chicago style, assigns the next ID, appends it to the repository's
BIBLIOGRAPHY.md, and reads it back for correction.
