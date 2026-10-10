# Official Release Spec v1.0

*For the Art Operation at the Historiotheque. Drafted 2026-09-28.*
*Drawn from the corpus of past Official Releases (v2.0.1–v5.1.0), hybridized with software release conventions.*

---

## 1. What this spec governs

An **Official Release** is a versioned document of the practice itself — the Historiotheque as cultural software, released under semantic versioning. It marks a point in the life of the practice: a launch, a shutdown, a relaunch after a fallow period, a new season of work.

This spec governs Official Releases of the practice only. **Repo releases** — the release notes attached to individual repositories on GitHub — are separate documents and are not governed by this spec.

## 2. The two forms

Every Official Release exists in two forms:

- **Full text** — the canonical version, in the author's voice, as published externally. Lives in `releases/archive/`.
- **Reader summary** — a condensed summary of the main points, for readers browsing the repository. Lives in `releases/`.

The full texts live in `releases/archive/`, under their published names (`official-release-X.Y.Z.md`, some with a date prefix). Reader summaries live in `releases/`, each named for its release's date and marked `-summary` (`YYYY-MM-DD-official-release-X.Y.Z-summary.md`), so the filename itself names the form. The folder READMEs explain the distinction.

## 3. Versioning

Semantic versioning: MAJOR.MINOR.PATCH, applied to the practice:

- **MAJOR** — a breaking change in the practice: a relaunch after a long shutdown, a new location, a methodology rebuilt from scratch. The operation cannot go back.
- **MINOR** — new content or direction inside a running operation: new projects, new research lines, new seasons of work.
- **PATCH** — fixes and small refinements: corrections, small methodology adjustments, brief relaunches.

Each release states its number and, in one line, why this number — e.g. "MAJOR: rebuilt from scratch after the shutdown of 3.0.5."

## 4. Required sections

Drawn from the recurring structure of the past releases:

1. **Version + date** — "Official Release: The Historiotheque, version X.Y.Z," with the release date.
2. **State of the operation** — running, shut down until further notice, on hiatus/sabbatical, or in a fallow period. Name the season, when one has been named.
3. **What changed** — the work since the last release: projects, research, methodology refinements. Studio logs may be mined as source material.
4. **Follow-through** — what the previous release predicted, and what actually happened. Predictions are checked, never silently dropped.
5. **What's next** — the coming period: the next season, the next anticipated version, what the operator intends.

## 5. Voice

First person. The Official Release is the operator speaking about the operation.

## 6. Placement and naming

- Summaries: `releases/YYYY-MM-DD-official-release-X.Y.Z-summary.md` (the date is the release's date; the `-summary` suffix marks the form)
- Full texts: `releases/archive/official-release-X.Y.Z.md`

Past releases published before this spec are marked as reconstructed, per the reconstruction-marking rule: every reconstructed file carries at least one line stating that it was reconstructed, with the date and sources where known. (Wording of the folder-level note is provisional — to be confirmed.)

## 7. Relation to neighboring document types

- **Official Declarations** are forward-looking statements for the production year; Releases report what happened and assign it a version.
- **Studio logs** are the raw material; Releases are the distilled, versioned record.
- **Repo releases** live with their repositories and are out of scope for this spec.
