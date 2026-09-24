# Historiotheque Studio Log — Format Specification v1.3

*Derived from The New Documentation (April–May 2024). Drafted 2026-09-20.*
*Amended 2026-09-23 (v1.1): split the old combined `season` field into a calendrical
`season` (automatic, never asked) and a qualitative `season_of_heart` (asked every
time, optional, may differ from the calendar season and change within a day).*
*Amended 2026-09-23 (v1.2): removed `season_of_heart` from the frontmatter entirely.
`season` is calendar-only, set automatically from the session date — nothing to state,
nothing to get wrong. The qualitative / moral-temperature season is not metadata: it
lives in the log body in the author's own words when relevant, and in the Seasons of
the Heart project. Also: `refcards` is cited only when the session actually created,
used, or decided about a card — otherwise the field stays empty.*
*Amended 2026-09-24 (v1.3): two sanctioned frontmatter variants — **Full** (the v1.2
shape, unchanged, the default) and **Compact** (for sessions where timing metadata was
not captured, e.g. reconstructed discourse logs). **Not retroactive:** logs written
under v1.0–v1.2 stand as-is; no back-editing required.*
*The theory: the Open Source Artist documents in the light — continuously, publicly, reproducibly.*

---

## 1. Purpose

A studio log entry is an atomic, timestamped record of one work session in the Art Operation.
It exists so that any experiment in the practice can be **reproduced** — by the artist later,
or by anyone with a web browser. Logs are the ground truth; Declarations, Releases,
PROSPECTIVEs and RETROSPECTIVEs are built on top of them.

The logs are **separate from but linked to** the Refcards project. Refcards are physical
index cards (atomic knowledge units); log entries cite them by ID — **but only when the
session actually created, used, or decided about a card.** A log with no card business
leaves `refcards` empty. Neither system pads the other.

## 2. File conventions

- **Location:** one `studio-logs/` directory per GitHub project repository, plus a master
  `studio-logs/` in the operation's root repo for cross-project sessions.
- **One file per session:** `studio-logs/YYYY-MM-DD-HHMM-<slug>.md`
  (24h time, local timezone; slug in kebab-case, e.g. `2026-09-20-1430-chronotopium-no12.md`).
- **Plain Markdown**, GitHub-flavored. YAML frontmatter at the top, body below.
  In the Full variant the body follows a fixed section order; in the Compact variant the
  body may be narrative. **In both variants, `Decisions` and `Next actions` are mandatory** —
  a session with no decisions recorded is a session not yet understood.

## 3. Frontmatter

Two variants are sanctioned. **Full is the default.** Compact is for sessions where timing
metadata was not captured — typically reconstructed discourse logs and quick captures.
The choice is per-session, declared by the shape used; do not mix variants within one file.

### 3a. Full variant (default)

```yaml
---
date: 2026-09-20
time_start: "14:30"
time_end: "16:10"
timezone: America/Toronto
season: autumn                      # calendar season only: spring | summer | autumn | winter
project: [chronotopium-series]     # project slug(s), kebab-case
stream: [image]                    # image | sound | text | mixed
session_type: studio               # studio | field | research | admin | discourse
workspace: historiotheque          # where the work happened
refcards: [RC-2026-0142, RC-2026-0143]   # ONLY cards this session created, used, or decided about; [] otherwise
tags: [assemblage, cardboard, first-pass]
related:
  - releases/5.1.0                 # links to declarations, releases, other logs
  - studio-logs/2026-09-18-1000-chronotopium-no11.md
---
```

### 3b. Compact variant

```yaml
---
project: [chronotopium-series]     # project slug(s), kebab-case
session_type: discourse            # studio | field | research | admin | discourse
stream: [image, sound]             # image | sound | text | mixed
workspace: historiotheque          # where the work happened
season: autumn                     # calendar season only: spring | summer | autumn | winter
tags: [discourse, video-presentation, cubism]
date: 2026-09-20
reconstructed: true                # ONLY for backfilled entries; add a provenance note in the body
---
```

**When to use which:** Full whenever the session's timing is known — it usually is, since
the filename already carries the start time. Compact when timing metadata was not captured
and cannot be recovered honestly. When in doubt, use Full.

**Not retroactive:** v1.3 does not invalidate any existing log. Entries written under
v1.0–v1.2 stand as-is; no back-editing is required or expected. (Two 2026-09-23 discourse
logs already used the compact shape before it was sanctioned — they are grandfathered,
not corrected.)

**Controlled vocabularies** (extend as needed, but never ad hoc — propose additions in the log):

- `season`: the calendar season only — spring | summer | autumn | winter, by solstice/equinox
  date. Set automatically from the session date when the log is written; never asked, never
  carried over unexamined. Pure archival metadata (lets future queries pull "everything logged
  in autumn 2026" without parsing dates).
- `stream`: image, sound, text, mixed.
- `session_type`: studio, field, research, admin, discourse (a video discourse counts as a session).
- `project`: the project's kebab-case slug, matching its repo/directory name.
- `reconstructed`: marks backfilled entries; always paired with a provenance note in the body
  ("Reconstructed <date> from <source>; times approximate.").

**On the qualitative season:** the moral-temperature reading (Seasons of the Heart) is not
frontmatter in either variant. When it matters to the session, write it in the log body in
your own words — it is interpretation, not metadata, and it can change within a day. The
Seasons of the Heart project remains its canonical home.

## 4. Body

**Full variant** — fixed section order:

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

**Compact variant** — the body may be narrative (a title, a session account in your own
order), but `Decisions` and `Next actions` remain mandatory sections. Omit any other
section that doesn't apply.

## 5. Cross-referencing conventions

- **Refcards:** cite as `RC-YYYY-NNNN` (e.g. `RC-2026-0142`). The number is the card's own
  number in the Refcards project; the log never renumbers cards. **Cite only cards the
  session actually created, used, or decided about** — relevance is the whole rule. When
  in doubt, leave the field empty; the card indexes remain searchable on their own.
- **Other logs:** relative path links (`../2026-09-18-1000-chronotopium-no11.md`).
- **Official documents:** cite by type and identifier
  (`Declaration 2028–2029`, `Release 5.1.0`, `PROSPECTIVE 2026-10`).
- **Tags:** kebab-case, shared across logs and Refcards so both systems stay searchable
  as one index.

## 6. Session skeletons (copy-paste)

**Full:**

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

**Compact:**

```markdown
---
project: []
session_type:
stream: []
workspace: historiotheque
season:
tags: []
date: YYYY-MM-DD
---

## Decisions

## Next actions
```

## 7. How to add a log (the working protocol)

Tell Oracle: **"add a studio log"** (or "log this session") and describe the session —
what you did, decided, hit, and made. Oracle drafts the entry in the Full variant by
default (Compact on request, or when timing metadata is honestly unavailable), files it,
validates it against this spec, and reads it back for correction before it's final.
The trigger phrase is the whole interface.

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
