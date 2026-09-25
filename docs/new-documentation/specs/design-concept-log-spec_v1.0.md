# Design Concept Log — Format Specification v1.0

*For logging design concepts across the whole practice: novels, series, albums, the
workspace itself, the Art Operation — any designed whole. Drafted 2026-09-20,
broadened from novels-only 2026-09-20.*
*Companion to the Studio Log Format Spec v1.0 and the GitHub Repository Structure Spec v1.0.*

---

## 1. Purpose

A design concept is the high-dimensional object: a fully-formed whole conceived all at
once — a novel's systems and simulations, a series' visual logic, an album's arc, the
workspace as a system — before a unit of it is made. The design concept log captures
these objects *as concepts*, separate from the one-piece-at-a-time execution tracked in
project repos and studio logs.

This log exists because of the central finding of the novelistic phenomenology: design
concepts arrive whole and instantaneous, while execution is a 1D bottleneck (Gordon Brander,
*Hypertext Montage*). Logging the concept preserves the high-dimensional object intact
instead of letting it dissolve into the bottleneck. The format was proven on novels
(DC-2026-001) and generalizes to every designed thing in the practice.

## 2. File conventions

- **Canonical location:** the dedicated `DesignConcepts` repository in the Historiotheque
  GitHub organization — one repo for all design concepts, the way the Refcards repo holds
  all cards. (Decided 2026-09-20.)
- **One file per concept:** `concepts/YYYY-MM-DD-<slug>.md` (a `concepts/` folder at the repo root —
  not `design-concepts/`, which would redundantly repeat the repo name).
  Project repos link to concept IDs (`DC-YYYY-NNN`); they don't duplicate the files.
- Revisions to a concept are new dated versions, not edits — the history of the concept
  is part of the data. Link versions in frontmatter (`supersedes` / `superseded_by`).

## 3. Frontmatter

```yaml
---
id: DC-2026-001
title: "The Nihilist"
domain: novels                    # novels | series | sound | texts | workspace | operation
date_conceived: 2025-03-14        # when the concept arrived, if known
date_logged: 2026-09-20
project: [the-nihilist]           # project slug(s), if assigned
status: concept                   # concept | outlining | drafting | stalled | archived
related_cards: [RC-2026-0107]     # Refcard IDs for the concept's atoms
related_logs: []                  # studio log files touching this concept
supersedes: null
---
```

## 4. Body — fixed section order

### The concept, whole
The work as it arrived: premise, world, arc — stated as one continuous vision, not
broken into steps. Write it the way it came: all at once.

### Systems and simulations
The concept treated as a system: what are its moving parts, its rules, its feedback loops?
What is being simulated? (For novels this is the novelistic phenomenology layer; for a
series, its visual logic; for the workspace, its deltas.)

### Philosophical machinery
The theories the work carries and how they are expressed — through characters, images,
sound, structure — rather than expounded. Name them where they have names
(historiotherapeusis, …).

### The bottleneck note
Where this concept currently stands against the 1D bottleneck: what has been executed
(one unit at a time), what is stuck, and what the next actionable step is.

### Open questions
What the concept still needs — research, decisions, missing machinery.

## 5. How to log one

Tell Oracle: **"log a design concept"** and describe the concept as it came to you — whole,
whatever kind of work it is. Oracle drafts the entry in this format, assigns the next
`DC-YYYY-NNN` ID, files it, and reads it back for correction before it's final.
