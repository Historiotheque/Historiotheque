# GitHub Repository Structure Spec v1.0

*For the Art Operation at the Historiotheque, under The New Documentation. Drafted 2026-09-20.*
*Companion to the Studio Log Format Spec v1.0.*

---

## 1. Principles

- **One project = one repository.** Each novel, series, system, or research line gets its own
  repo, named with its kebab-case slug (`chronotopium-series`, `schizobot-lite`, `solitude-and-death`).
- **Refcards are universal; everything else is local.** There is exactly one Refcards system
  (one repo). Project repos *reference* card IDs; they never duplicate cards.
- **Bibliographies are per-repo.** Each repo keeps its own `BIBLIOGRAPHY.md` with the sources
  actually used there. The root repo keeps the master bibliography.
- **Theory lives with its project.** The philosophy behind a novel or project is documented
  in that project's repo, in long form — and decomposed into atomic Refcards that point at it.
- **Everything cross-references by stable ID.** Card IDs (`RC-YYYY-NNNN`), citation IDs
  (`BIB-YYYY-NNN`), log filenames, document identifiers. IDs never change; titles may.

## 2. The operation root repo — `the-historiotheque/the-historiotheque`

The cultural software itself, and the only repo that sees the whole operation.
Named exactly like the organization so its README renders as the org's public profile
page — the front door and the master index in one repo (the same convention as
`antiface/antiface` on the personal account). This keeps the repo count minimal.

```
the-historiotheque/
├── README.md                  # what the Historiotheque is; map of the whole system
├── BIBLIOGRAPHY.md            # master bibliography (superset / index of project ones)
├── studio-logs/               # cross-project and operation-level sessions
├── docs/
│   ├── declarations/          # Official Declarations of Production-Year
│   ├── releases/              # Official Releases (semantic versioning)
│   ├── prospectives/          # PROSPECTIVEs
│   ├── retrospectives/        # RETROSPECTIVEs
│   └── new-documentation/     # The New Documentation and its specs (this file lives here)
├── schemas/                   # the schema family (REFMATS, ALX, Historiotheque Work Schema…)
├── projects/
│   └── index.md               # every project repo, its slug, status, and URL
└── workflows/                 # operation-level procedures (e.g. how to cut a Release)
```

## 3. The universal Refcards repo — name TBD (candidates: `refcard-system`, `card-index`, `the-card-catalog`)

The atomic knowledge base. One concept per card, tens of thousands of them, on anything.
(The repo needs its own name — the user already has a repo called Refcards.)

```
<refcards-repo>/
├── README.md                  # what a Refcard is; the atomicity rule; how to write one
├── index.md                   # master map: entry points, tag cloud, curated trails
├── cards/
│   ├── RC-2026/               # sharded by year: cards/RC-YYYY/RC-YYYY-NNNN.md
│   │   ├── RC-2026-0142.md
│   │   └── RC-2026-0143.md
│   └── RC-2025/
│       └── …
└── trails/                    # curated sequences of cards (reading paths through the system)
    └── historiotherapeusis.md # e.g. a trail assembling one theory from its cards
```

**Sharding rule:** one directory per year. If a year ever exceeds ~2,000 cards, split into
`RC-YYYY-A/`, `RC-YYYY-B/` thousand-blocks. Never put tens of thousands of files in one
directory — filesystems and the GitHub UI both choke.

### The Refcard file format

```markdown
---
id: RC-2026-0142
title: "Historiotherapeusis: definition"
type: concept        # concept | definition | quote | question | method | reference | distinction
date_created: 2026-09-20
date_modified: 2026-09-20
tags: [historiotherapeusis, history-project, theory]
related: [RC-2026-0107, RC-2025-0891]   # other card IDs, both directions maintained by hand
sources: [BIB-2026-004]                 # citation IDs from a BIBLIOGRAPHY.md
physical_location: "Box 3, divider HISTORY"  # where the physical index card lives, if any
status: developing                     # seed | developing | stable | superseded
---

The atomic content. One concept, stated as tightly as possible. A card may be three
sentences long. If it wants to be an essay, it belongs in a project's `theory/`
directory instead, and the card becomes its pointer.
```

**Atomicity rule:** one card = one concept. If a card needs the word "and" in its title,
it is two cards. Cards link; they don't contain.

## 4. The project repo template

```
<project-slug>/
├── README.md                  # the project: what it is, status, season, links
├── BIBLIOGRAPHY.md            # sources used by this project (BIB-YYYY-NNN IDs)
├── studio-logs/               # session files per the Studio Log Spec v1.0
├── theory/                    # long-form philosophy/theory behind the project
│   ├── overview.md            # the project's conceptual scheme, in full
│   ├── historiotherapeusis.md # e.g. one theory document per major theory
│   └── novelistic-phenomenology.md
├── docs/                      # project-level official documents, if any
├── artifacts/
│   ├── images/                # artifact registry (metadata; binaries optional)
│   ├── sounds/
│   └── texts/
└── src/                       # code, if the project has any (Schizobot, scripts…)
```

**How theory and Refcards divide the work:** `theory/` holds the developed, long-form
account — the full exposition of historiotherapeusis, say, or the novelistic phenomenology.
The Refcards hold the *atoms*: definitions, distinctions, quotes, questions, methods.
Every theory document ends with a **card index** listing the Refcard IDs that compose it;
every such card links back to the theory document. Long form and atoms stay in sync
by reference, not by duplication.

## 5. Cross-repo referencing

- **Card → anything:** `RC-2026-0142` is globally unique; cite it from any repo, log, or document.
- **Log → card:** the log frontmatter's `refcards:` field (Studio Log Spec §3).
- **Theory → cards:** card index at the foot of each theory document.
- **Bibliography → everything:** cite `BIB-YYYY-NNN`; the full Chicago entry lives in the
  repo's `BIBLIOGRAPHY.md`.
- **Official documents → repos:** Declarations and Releases name project slugs;
  project READMEs link back to the documents that govern them.

## 6. Seeding order (what to build first)

1. `the-historiotheque` root with `docs/` and this spec — the map before the territory.
2. The Refcards repo (name TBD — see §3) with the format and the first cards (start with the named theories:
   historiotherapeusis, novelistic phenomenology, the Archives-Project philosophies).
3. One project repo as the template exemplar (the Chronotopium or Solitude and Death).
4. `BIBLIOGRAPHY.md` in the root — seed with the reading list, then grow per project.
5. Backfill: existing theory texts go to `theory/`; existing notes get decomposed into cards.

---

*Specs in this system: Studio Log Format v1.0 · GitHub Repository Structure v1.0 ·
Citation standard: Chicago 17th (author-date in logs/cards, notes-bibliography in documents).*
