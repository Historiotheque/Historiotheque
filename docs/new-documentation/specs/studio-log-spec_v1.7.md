# Historiotheque Studio Log — Format Specification v1.7

*LIVE — minted 2026-10-04. First applied in studio-logs/2026-10-04-0516-workspace-temperature-and-switchboard.md.*

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
*Amended 2026-09-25 (v1.4): authorship rule — logs are written in the first person;
the Chief Art Operator is the author. Path convention — repo-relative paths in logs
(the permanent addresses); local staging paths belong in the upload checklist, not
in the logs. **Not retroactive:** logs written under v1.0–v1.3 stand as-is.*
*Amended 2026-09-25 (v1.5): season-naming rule — wherever a season designation is
recorded (README field, log body, project document), it carries only the author's own
designation. If no season has been named, the field is left blank or marked `[unnamed]`.
A season is never assigned by anyone but the author, and never inferred from content.
**Not retroactive:** logs written under v1.0–v1.4 stand as-is.*
*Amended 2026-09-29 (v1.6; minted 2026-09-30): `session_type` becomes a list-valued
verb vocabulary derived from the Historiotheque Work Schema (Facet A); `studio` and
`field` retire as `session_type` values (they are places — they live on the workspace
axis now); `admin` retires as vague (use the precise A3 verb); `publishing` added as
the verb for putting work out into the world. `workspace` becomes list-valued —
studio | lab | field, functional zones, never rooms; "historiotheque" retires as a
value (the spec prose names it as the containing place). Field sessions are first-class
entries under this spec (`workspace: [field]`); no separate spec. Body boundary markers
may carry active-space headers (§4). §7 states the trigger phrase without naming an
actor. New §9 states the versioning policy. **Not retroactive:** logs written under
v1.0–v1.5 stand as-is; no back-editing required or expected.*
*Amended 2026-10-04 (v1.7 — minted 2026-10-04): frontmatter time becomes `sessions:` —
a list of the log's actual work sessions, derived from the record (silence gap of
60 minutes; a cluster counts as a session at ≥3 recorded traces or ~10 minutes of
engagement), replacing `time_start`/`time_end`, which flattened multi-session arcs
into a single envelope dressed as a session. `date:` is the date of the first session.
Derived times carry a stated tolerance of ±15 minutes and are ratified by the Operator
at drafting; reconstructed segments (work away from the record) carry a wider tolerance
and a provenance note. Segment headers are minted only at a configuration switch and
carry the segment's full span (date, then start → end; the end date appears only when
it differs). A `ΔW temp` line sits under each segment header: three QoT (qualities of
time) qualia, derived from the segment's record, proposed at drafting, ratified by the
Operator; the terms live in the companion vocabulary (`studio-log-vocabulary.md`).
Sub-threshold micro-switches are narrated in the body as switch texture, not headed.
In the Compact variant, segment headers and ΔW temp lines are permitted, not required.
**Not retroactive:** logs written under v1.0–v1.6 stand as-is; no back-editing required
or expected.*
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

**Authorship:** logs are written in the first person. The Chief Art Operator is the author.

**Field sessions** are first-class entries under this spec: a session in the field is an
ordinary log with `workspace: [field]` in the frontmatter. There is no separate field-log
spec; if field recording ever needs frontmatter no studio session needs, that is the day
for a sibling spec — not before.

## 2. File conventions

- **Location:** one `studio-logs/` directory per GitHub project repository, plus a master
  `studio-logs/` in the operation's root repo for cross-project sessions.
- **One file per log entry:** `studio-logs/YYYY-MM-DD-HHMM-<slug>.md`
  (24h time, local timezone; slug in kebab-case, e.g. `2026-09-20-1430-chronotopium-no12.md`).
  An entry may span several work sessions; the filename time is the entry's drafting time.
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
date: 2026-09-20                       # date of the FIRST session in `sessions:`
sessions:
  - "2026-09-20 14:30 → 16:10"          # one line per work session; end date only when it differs
timezone: America/Toronto
season: autumn                      # calendar season only: spring | summer | autumn | winter
project: [chronotopium-series]     # project slug(s), kebab-case
stream: [image]                    # image | sound | text | mixed
session_type: [composing]          # verbs, list-valued — see controlled vocabularies
workspace: [lab]                   # studio | lab | field — functional zones, list-valued
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
session_type: [discourse]          # verbs, list-valued — see controlled vocabularies
stream: [image, sound]             # image | sound | text | mixed
workspace: [lab]                   # studio | lab | field — functional zones, list-valued
season: autumn                     # calendar season only: spring | summer | autumn | winter
tags: [discourse, video-presentation, cubism]
date: 2026-09-20
reconstructed: true                # ONLY for backfilled entries; add a provenance note in the body
---
```

**When to use which:** Full whenever the session's timing is known — it usually is, since
the filename already carries the drafting time. Compact when timing metadata was not captured
and cannot be recovered honestly. When in doubt, use Full.

**Not retroactive:** v1.7 does not invalidate any existing log. Entries written under
v1.0–v1.6 stand as-is; no back-editing is required or expected. (Two 2026-09-23 discourse
logs already used the compact shape before it was sanctioned — they are grandfathered,
not corrected.)

**Controlled vocabularies** (extend as needed, but never ad hoc — propose additions in the log):

- `season`: the calendar season only — spring | summer | autumn | winter, by solstice/equinox
  date. Set automatically from the session date when the log is written; never asked, never
  carried over unexamined. Pure archival metadata (lets future queries pull "everything logged
  in autumn 2026" without parsing dates).
- `sessions`: the log's actual work sessions, one line each, in chronological order —
  `"YYYY-MM-DD HH:MM → HH:MM"`, the end date repeated only when the session crosses
  midnight. Sessions are *derived* from the record (channel messages, commits, file
  changes, the Operator's reports): activity clusters split at a silence gap of
  60 minutes; a cluster counts as a session at ≥3 recorded traces or ~10 minutes of
  engagement. Derived times are inner bounds — first trace to last trace — accurate to
  a stated tolerance of ±15 minutes (one Switchboard switch), and are ratified by the
  Operator at drafting: derivation proposes, the Operator disposes. Sessions away from
  the record (field work, work at the easel) are reconstructed from the Operator's
  report, carry a wider tolerance, and are marked as reconstructed with their provenance
  stated in the body. A silent period is never silently absorbed into a neighbouring
  session; at drafting it is surfaced to the Operator as a question.
- `stream`: image, sound, text, mixed.
- `session_type`: verbs, list-valued, derived from the Historiotheque Work Schema
  (Facet A — Functional Mode). The sanctioned core:
  - *reading* (A1 — intake & absorption)
  - *composing, creating, designing, drafting, sketching, prototyping* (A2 — generative
    & formative; "creating" covers painting and other making)
  - *archiving, documenting, logging, indexing, citing, formatting* (A3 — technical
    & structural)
  - *publishing, producing, curating, exhibiting, distributing* (A4 — synthesis & output;
    "publishing" is the verb for putting work out into the world: pushing logs, cutting
    releases, posting)
  - *discourse, research, reflecting, reviewing* (A5 — meta-cognitive; a video discourse
    counts as a session)

  Retired as `session_type` values: `studio`, `field` — they are places, and they live on
  the workspace axis now; `admin` — too vague, use the precise A3 verb for what was actually
  done. (A v1.5 log reading `session_type: studio` is understood as `workspace: [studio]`
  plus the A2 verb for the work.) The word "lab" is NOT retired — `workspace: [lab]` is
  fully live; only `session_type: [lab]` is gone, because it said nothing the workspace
  value didn't already say. Bodily/somatic practice is not a `session_type`: write it in
  the log body.
- `workspace`: studio | lab | field — functional zones, list-valued, never rooms. The values
  name what the space is *for*; the actual rooms are never named in logs. The Historiotheque
  is the containing place — the spec prose names it; it is not a value. List every zone the
  session moved through; the body headers (§4) record the sequence. `workspace: [field]`
  marks field sessions.
- `project`: the project's kebab-case slug, matching its repo/directory name.
- `reconstructed`: marks backfilled entries; always paired with a provenance note in the body
  ("Reconstructed <date> from <source>; times approximate.").

The two axes compose: `workspace × session_type` names the session's active space
(see §4). The frontmatter records the arc — every value the session touched.

**On the qualitative season:** the moral-temperature reading (Seasons of the Heart) is not
frontmatter in either variant. When it matters to the session, write it in the log body in
your own words — it is interpretation, not metadata, and it can change within a day. The
Seasons of the Heart project remains its canonical home.

**On naming a season:** wherever a season designation is recorded — the studio-logs
README's season field, a log body, a project document — it carries only the author's
own designation. If no season has been named, the field is left blank or marked
`[unnamed]`; placeholder prose does not belong in published documentation. A season is
never assigned by anyone but the author, and never inferred from a log's content.

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

### Segment headers and ΔW temp
Within the body, a new segment header is minted **only when the configuration actually
switches** — a delta exists only where `workspace × session_type` changes; no switch,
no header. The header carries the segment's full span and configuration, and a short
segment title in the author's own words may be appended after the configuration:

```markdown
## 2026-10-03 10:12 → 11:47 — workspace=[lab, field] × session_type=[research, discourse]
ΔW temp = dense, polyphonic, glowing

[body of the segment]
```

- Line 1: date first, then start → end (the house order — the same order as the
  filenames); the end date appears only when the segment crosses midnight. The
  configuration follows the em dash. A reader sees the whole session — its span,
  its place, its work — on one line.
- Line 2: `ΔW temp` — the workspace temperature of the *change*, in formula form:
  three QoT (qualities of time) qualia, derived from the segment's record (its switch
  texture, its drift across configurations, what it produced), proposed at drafting
  and ratified by the Operator. The qualia are a controlled vocabulary, defined in
  the companion document `studio-log-vocabulary.md`; new terms enter it only from a
  ratified log, each with its date of introduction and first-used context. No hue
  terms: the qualia carry the whole reading.
- Division of labor: the frontmatter `sessions:` records when work happened; the body
  headers record the configuration sequence inside and across those sessions — the
  score of the arc.
- **Switch texture:** switches below the session threshold (a configuration held only
  briefly, or producing nothing) are not headed; they are narrated in the segment's
  body as texture — the felt grain of the switching — so rapid sub-threshold movement
  stays visible without shredding the page into headers.
- Backward-compatible: a bare timestamp line still parses. Each version adds; it never breaks.

**Compact variant** — the body may be narrative (a title, a session account in your own
order), but `Decisions` and `Next actions` remain mandatory sections. Omit any other
section that doesn't apply. Segment headers and ΔW temp lines are permitted in the
Compact variant, not required.

## 5. Cross-referencing conventions

- **Refcards:** cite as `RC-YYYY-NNNN` (e.g. `RC-2026-0142`). The number is the card's own
  number in the Refcards project; the log never renumbers cards. **Cite only cards the
  session actually created, used, or decided about** — relevance is the whole rule. When
  in doubt, leave the field empty; the card indexes remain searchable on their own.
- **Other logs:** relative path links (`../2026-09-18-1000-chronotopium-no11.md`).
- **Paths:** cite repo-relative paths (the permanent addresses — e.g.
  `Historiotheque/studio-logs/…`). Local staging paths belong in the upload
  checklist, not in the logs.- **Official documents:** cite by type and identifier
  (`Declaration 2028–2029`, `Release 5.1.0`, `PROSPECTIVE 2026-10`).
- **Tags:** kebab-case, shared across logs and Refcards so both systems stay searchable
  as one index.

## 6. Session skeletons (copy-paste)

**Full:**

```markdown
---
date: YYYY-MM-DD
sessions: []
timezone: America/Toronto
season:
project: []
stream: []
session_type: []
workspace: []
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
session_type: []
stream: []
workspace: []
season:
tags: []
date: YYYY-MM-DD
---

## Decisions

## Next actions
```

## 7. How to add a log (the working protocol)

Say **"add a studio log"** (or "log this session") and describe the session —
what you did, decided, hit, and made. The entry is drafted in the Full variant by
default (Compact on request, or when timing metadata is honestly unavailable), filed,
validated against this spec, and read back for correction before it's final.
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

**To add a citation:** say **"add a citation"** and name the source (author, title,
and whatever else you remember). It is formatted in Chicago style, assigned the next ID,
appended to the repository's BIBLIOGRAPHY.md, and read back for correction.

## 9. Versioning

This spec is versioned rarely and deliberately. Vocabulary grows through the extend-as-needed
rule (§3) without minting a new version; new versions are minted only for structural changes —
conflicts, absurdities (a value that says nothing), or appreciable differences in what the
spec demands. Minor clarifications accumulate in the amendment history at the top. No backfill:
old logs stand under the spec of their date.
