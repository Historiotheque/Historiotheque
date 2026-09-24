---
date: 2026-09-23
time_start: "23:15"
time_end: "00:40"
timezone: America/Toronto
season: autumn
project: [atmospherics-theory]
stream: [text]
session_type: research
workspace: historiotheque
refcards: []
tags: [atmospherics-theory, repo-scaffold, field-recording, github, project-lists, historiotheque-work-schema]
related:
  - ../atmospherics/atmospherics-theory-repo-structure_2026-09-23.md
---

## What I did

Late-night session in the Atmospherics Theory side chat, taking the theory from
conversation to repository. In order:

1. Filed the phenomenology-of-electroacoustic bibliography (received Sept 21) as
   `bibliography-phenomenology-of-electroacoustic-music_2026-09-21.md`, in a new
   `workspace/your_files/atmospherics/` folder.
2. Settled the field-recording practice: the ~20 ambient YouTube videos continue
   as the empirical arm of the theory. Streams separated by medium, not by day;
   rhythm instead of calendar (the atmosphere decides the recording day); essays
   begin as liner notes in video descriptions.
3. Drafted the `atmospherics-theory` repo top-level structure (8 numbered folders
   + README), framed by the Historiotheque Work Schema v1.0 — explicitly not the
   Cubism-research schema, since different research gets different schemas.
4. Built `atmospherics-theory.zip` (three iterations — see Problems and friction).
5. Drafted the initial commit message, the repo About description, and a README
   carrying the axiom, in `atmospherics-theory-commit-and-notes_2026-09-24.md`.
6. Drafted the project-list entries for both the org profile README (bullet) and
   `projects/index.md` (table row), placed directly after Research.
7. Settled the naming question: `atmospherics-theory` (with the S) for the folder;
   `AtmosphericsTheory` (CamelCase) for the GitHub repo, matching the house style
   (NoiseFieldTheory, SignalScience, RefcardsSystem).

## Decisions

**Decision:** Keep the field recordings going indefinitely.
**Reason:** They are the empirical arm of Atmospherics Theory — first-person field
recording as research method; the collection itself is the research instrument.

**Decision:** Separate streams by medium, not by day.
**Reason:** No rigid schedules — sounds live on YouTube, words start in video
descriptions, images stay inside the videos as title cards.

**Decision:** Rhythm instead of calendar for recording and publishing.
**Reason:** The atmosphere decides the recording day (storm fronts, pressure drops);
publish when a place-set coheres.

**Decision:** Start a dedicated `atmospherics-theory` repo in the Historiotheque org.
**Reason:** One home for the theory: founding documents, bibliography, essays,
recording index, concepts glossary.

**Decision:** Frame the repo structure with the Historiotheque Work Schema v1.0,
not the Cubism-research schema.
**Reason:** Different research, different schemas; the Work Schema's functional
modes (intake → output) fit an intake-heavy archival practice.

**Decision:** Keep the S — `atmospherics-theory` / `AtmosphericsTheory`.
**Reason:** It is the coined term; consistency is load-bearing; "atmospherics" is
also the standard English word.

**Decision:** List AtmosphericsTheory directly after Research in both project lists.
**Reason:** A theory research archive belongs in the research band of the lists.

## Problems and friction

- GitHub's web uploader silently dropped the empty folders — Git does not track
  empty directories. Not rate-limiting; by design.
- First fix (`.gitkeep` placeholders) failed: the OS hides dotfiles, so the file
  picker refused them ("This file is hidden").
- Resolved by replacing `.gitkeep` with a small visible `README.md` in each folder,
  describing what the folder is for — uploads cleanly and documents the repo.

## Ideas and sketches

- `seed`: Liner-notes-to-essays pipeline — a paragraph under each video grows into
  longer essays as the theory needs text.
- `proposal` (open, offered Sept 22): a working document on an atmospheric theory
  of literary authorship (Woolf case study). Still awaiting a tap.

## Research and references

- The call-for-submissions bibliography on the phenomenology of electroacoustic
  music (~30 refs, filed in the repo folder).
- Consulted: Historiotheque Work Schema v1.0; Taxonomy of Research, Projects, and
  Reference Materials (skimmed, set aside for this use); the org's repo list
  (naming-convention check); the org profile README; the primary-projects list
  (ATMOSPHERIC TONE already listed as project #3 — the recording series; this repo
  is its theory archive).

## Reproducibility notes

Zip built from `workspace/your_files/atmospherics/`:

```
mkdir -p atmospherics-theory/{01-intake,02-generative,03-founding-documents,04-bibliography,05-recordings-index,06-concepts,07-output,08-meta}
```

One `README.md` per folder (one line describing its purpose); root `README.md`
carries the theory-statement placeholder. Then:

```
zip -r atmospherics-theory.zip atmospherics-theory
```

## Artifacts produced

**Text:**
`bibliography-phenomenology-of-electroacoustic-music_2026-09-21.md` · the
call-for-submissions bibliography, filed verbatim · 2026-09-23 ·
`workspace/your_files/atmospherics/`

`atmospherics-theory-repo-structure_2026-09-23.md` · Draft 1 of the repo
top-level structure · 2026-09-23 · `workspace/your_files/atmospherics/`

`atmospherics-theory.zip` · the empty repo skeleton, zipped (v3: README.md per
folder) · 2026-09-24 · `workspace/your_files/atmospherics/`

`atmospherics-theory-commit-and-notes_2026-09-24.md` · initial commit message,
About description, README draft · 2026-09-24 · `workspace/your_files/atmospherics/`

`atmospherics-theory-list-entries_2026-09-24.md` · project-list entries (README
bullet + index.md table row) · 2026-09-24 · `workspace/your_files/atmospherics/`

## Next actions

- [ ] me — Upload the zip contents to the new GitHub repo (name: AtmosphericsTheory).
- [ ] me — Add the AtmosphericsTheory bullet to the org profile README after Research
      (entry text in `atmospherics-theory-list-entries_2026-09-24.md`; local draft at
      `workspace/your_files/historiotheque/org-profile-readme.md`, live file on GitHub).
- [ ] me — Add the AtmosphericsTheory table row to `projects/index.md` after Research
      (lives on GitHub; no local copy).
- [ ] me — Review `atmospherics-theory-commit-and-notes_2026-09-24.md` for
      AtmosphericsTheory vs atmospherics-theory naming consistency before committing.
- [ ] me — Decide on the open offer: the atmospheric literary authorship document.
