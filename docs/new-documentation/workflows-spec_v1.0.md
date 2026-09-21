# Workflows Folder Spec v1.0

*For the Art Operation at the Historiotheque, under The New Documentation. Drafted 2026-09-20.*
*Companion to the Studio Log Format Spec v1.0 and the GitHub Repository Structure Spec v1.0.*

---

## 1. Principles

- **A workflow is a repeatable procedure, not a statement.** The `docs/` folders hold the
  operation's official documents — Declarations, Releases, Prospectives, Retrospectives.
  `workflows/` holds the machinery that produces them: the step-by-step procedures by which
  the Art Operation runs. Documents say what is true; workflows say what to do.
- **Workflows are operation-level.** They live in the root repo (`Historiotheque/Historiotheque`),
  never in project repos, because they govern the operation as a whole. A project repo's
  README may *reference* a workflow; it never duplicates one.
- **Every workflow is auditable.** The Art Operation is transparent by design (Art Operation 4.0).
  Each procedure leaves an audit trail: who ran it, when, with what result. Running a workflow
  is itself an event worth logging.
- **Workflows are versioned documents.** Procedures change. When a procedure changes, its
  workflow file gets a new version and a changelog entry — never a silent edit.
- **Workflows and studio logs are linked systems.** Opening and closing a work session
  ((AG)-Method: snapshot, declaration, inventory) is itself a workflow, and every logged
  session implicitly followed one.

## 2. Where workflows live

```
Historiotheque/Historiotheque/
└── workflows/
    ├── README.md              # what a workflow is; how to run and revise one
    ├── wf-index.md            # every workflow: ID, title, status, version
    ├── wf-2026-001-cutting-an-official-release.md
    ├── wf-2026-002-writing-a-declaration-of-production-year.md
    └── …
```

**Naming rule:** one file per workflow, named `wf-YYYY-NNN-<slug>.md`.
The ID `WF-YYYY-NNN` is stable; the slug may change. IDs are sequential within the year.

## 3. The workflow file format

### 3.1 Frontmatter

```yaml
---
id: WF-2026-001
title: "Cutting an Official Release of the Historiotheque"
status: draft            # draft | active | deprecated
version: 1.0
date_created: 2026-09-20
date_modified: 2026-09-20
trigger: "A Release of the Historiotheque is declared"
frequency: "aperiodic"   # daily | weekly | aperiodic | on-trigger
prerequisites: ["git", "the release-notes template"]
inputs: ["the set of changes since the last Release"]
outputs: ["the Release notes document", "updated project index entries"]
operator_role: "Chief Archivist"   # which Art Operation role runs this (see §5)
audit: true               # this workflow leaves an audit trail
related: [RC-2026-0005]   # Refcard IDs for the concepts it touches
---
```

### 3.2 Body sections (all mandatory)

1. **Purpose** — what this procedure accomplishes and why it exists. One paragraph.
2. **Trigger** — the event or schedule that starts it. Never "whenever"; be specific.
3. **Prerequisites** — tools, files, permissions, and states that must hold before step one.
4. **Inputs and outputs** — what goes in, what comes out, and where the outputs are filed.
5. **Procedure** — the steps, numbered. Each step states the action and the check that
   confirms it is done. Steps that mutate state are marked **[mutation]**; steps that are
   checkpoints are marked **[checkpoint]**.
6. **Rollback / recovery** — how to undo the procedure or recover from a failed run.
   A workflow without a rollback path is not a workflow; it is a wish.
7. **Verification** — how to confirm the procedure succeeded. What would a stranger
   check to be certain?
8. **Audit trail** — what gets recorded, and where: the studio log entry, the commit
   message convention, the dated line in `wf-index.md`.
9. **Changelog** — appended entries, newest first: `v1.1 (2026-10-02): …`
10. **Open questions** — what the procedure does not yet cover.

## 4. The first workflows to write

These cover the operation's recurring machinery. They are named before they are written:

| ID         | Title                                                | Why first                                    |
|------------|------------------------------------------------------|----------------------------------------------|
| WF-2026-001 | Cutting an Official Release of the Historiotheque    | the defining operation-level procedure        |
| WF-2026-002 | Writing a Declaration of Production-Year             | the other great recurring ceremony           |
| WF-2026-003 | Onboarding a new project (repo + index + cards)      | turns projects into documented systems       |
| WF-2026-004 | Opening and closing a work session (the (AG)-Method) | session snapshots, declaration, inventory    |
| WF-2026-005 | Importing works into the archive                     | the Artwork Archive Plan, step by step        |
| WF-2026-006 | Taking a full backup of the operation                | before any change to the root repo           |
| WF-2026-007 | Publishing a document to Medium / the Historiotheque | from `.md` to the world                      |

## 5. Operator roles

Every workflow names the Art Operation role that runs it. Roles follow the Art Operation
doctrine (Chief Archivist, Chief Historian, Documentarian, Media Analyst, Historical
Therapist, Linguist/Semiotician, and the Chief Artistic Officer / Chief Information
Officer pair). A one-person operation wears all the hats; the role field exists so the
*function* is recorded, not the person. When the operation grows, the hats are already
labeled.

## 6. Workflows and the other systems

- **Docs → workflows:** every official document type in `docs/` should eventually have a
  workflow that produces it (Declarations, Releases, Prospectives, Retrospectives).
- **Workflows → logs:** running a workflow produces artifacts (a Release, a backup);
  the session that ran it is logged per the Studio Log Spec, with the workflow's ID
  in the log frontmatter (`workflow: WF-2026-001`).
- **Workflows → Refcards:** the concepts a procedure depends on are cited as card IDs.
  When a procedure invents a concept, a card gets written.
- **Workflows → index:** `wf-index.md` is the master map — ID, title, status, version,
  last run date. Nothing in `workflows/` is invisible.

---

*Specs in this system: Studio Log Format v1.0 · GitHub Repository Structure v1.0 ·
Workflow/Procedure Format v1.0 · Citation standard: Chicago 17th (author-date in
logs/cards, notes-bibliography in documents).*


- - - - - - -

**A note on what this is.** This repository belongs to an ongoing research-creation
project at the intersections of art, history, and philosophy — the open working
record of one artist-researcher's practice. It documents a method, not a manual:
nothing here is instruction, counsel, or advice on running an art operation, a
studio, or a creative life, and nothing here is presented as a model to follow.
What holds in this laboratory may not hold in yours.

All works are offered in good faith as contributions to public discourse and
aesthetic reflection. Take what is useful and leave the rest — the responsibility
for interpretation, and for whatever is done with it, remains with each participant
in that dialogue.

[A.G. (c) 2026. ![A.G. (c) 2026. All Rights Reserved](https://historiotheque.files.wordpress.com/2016/11/ag_signature_official_2015_50px_cropped.jpg) All Rights Reserved.](http://alexgagnon.com)
