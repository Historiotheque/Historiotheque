# Design Concept Log — Format Specification v1.0

*For logging novel design concepts: the whole-novel-at-once visions, treated as systems /
simulations. Drafted 2026-09-20.*
*Companion to the Studio Log Format Spec v1.0 and the GitHub Repository Structure Spec v1.0.*

---

## 1. Purpose

A design concept is the high-dimensional object: a fully-formed novel conceived all at
once — its systems, simulations, characters, and philosophical machinery — before a word
of it is written. The design concept log captures these objects *as concepts*, separate
from the one-section-at-a-time writing tracked in the NOVELS repo and the studio logs.

This log exists because of the central finding of the novelistic phenomenology: design
concepts arrive whole and instantaneous, while writing is a 1D bottleneck (Gordon Brander,
*Hypertext Montage*). Logging the concept preserves the high-dimensional object intact
instead of letting it dissolve into the bottleneck.

## 2. File conventions

- **Canonical location:** the dedicated `design-concepts` repository in the Historiotheque
  GitHub organization — one repo for all design concepts, the way the Refcards repo holds
  all cards. (Decided 2026-09-20.)
- **One file per concept:** `design-concepts/YYYY-MM-DD-<slug>.md`.
  Project repos link to concept IDs (`DC-YYYY-NNN`); they don't duplicate the files.
- Revisions to a concept are new dated versions, not edits — the history of the concept
  is part of the data. Link versions in frontmatter (`supersedes` / `superseded_by`).

## 3. Frontmatter

```yaml
---
id: DC-2026-001
title: "The Nihilist"
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
The novel as it arrived: premise, world, arc — stated as one continuous vision, not
outlined chapter by chapter. Write it the way it came: all at once.

### Systems and simulations
The novel treated as a system: what are its moving parts, its rules, its feedback loops?
What is being simulated? (This is the "novel-as-a-system" / novelistic phenomenology layer.)

### Philosophical machinery
The theories the novel carries and how they are expressed — through characters, dialogue,
structure — rather than expounded. Name them where they have names (historiotherapeusis, …).

### The bottleneck note
Where this concept currently stands against the 1D bottleneck: what has been written
(one section at a time), what is stuck, and what the next writable section is.

### Open questions
What the concept still needs — research, decisions, missing machinery.

## 5. How to log one

Tell Oracle: **"log a design concept"** and describe the novel as it came to you — whole.
Oracle drafts the entry in this format, assigns the next `DC-YYYY-NNN` ID, files it, and
reads it back for correction before it's final.
