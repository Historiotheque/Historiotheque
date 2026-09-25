---
date: 2026-09-25
time_start: "11:20"
time_end: "12:40"
timezone: America/Toronto
season: (to be named — mine to name, never assigned)
project: []
stream: [text]
session_type: research
workspace: historiotheque
refcards: []
tags: [error-taxonomy, risk, somatic-principles, feldenkrais, releases, zenodo, doi, methodology, reproducibility, operator-error, next-actions]
related:
  - studio-logs/2026-09-25-0700-doctrine-session.md
---

## What I did

Session in three movements: field recordings → instruments built → releases published. In order:

1. **Field recordings on a walk.** I made three audio recordings: one on why methodology matters, two on the common types of errors in an Art Operation and their levels of severity. Back home I took notebook notes in point form: knapsack optimization problems and linear programming; ArtOps problems plus design patterns/antipatterns; distributed logs for reliability and robustness (built-in redundancy, timestamps for every new session — my session-management material); workflow and workspace management; knapsack problems in everyday life (what to optimize for — time, energy — SOLVE FOR X); computational complexity and cost analysis of ArtOps work (time/space complexity of tasks, workflow, workspace organization); Taylorist methodology applied to ArtOps (small costs add up), costly signaling, and my "Cost of Ping" theory — signaling games, the cost of sending a message, the risks and errors in communication.
2. **Error taxonomy drafted (v0.1).** I had Oracle build the taxonomy straight from those notes: ten error classes — accounting, transcription, interpretation, methodology/technique, workflow management, workspace management, system, operator, communication/signaling, and DON'T KNOWS (the junk drawer, per my mentor's faceted-taxonomy discipline) — with an S1–S5 severity scale, blast radius, compounding rules (severity multiplies, never adds), and a mitigation map. Staged NEW for `Historiotheque/Research/risks/` (the upload creates the folder). No personal content in it — the philosophy went in, the people didn't.
3. **Repo minimalism adopted as doctrine (my decision, my words).** I want the smallest sufficient set of repos, and I will archive or deprecate any that are extraneous. Lesson from my intelligence-analysis mentor: a representative sample of categories, plus one junk drawer for the DON'T KNOWS. Consequence: no new repos for any of this — risks, logistics, and the future hermeneutics of Art Operations all go as folders under Research. The DON'T KNOWS drawer becomes a standing convention: every taxonomy I publish gets a terminal unclassified category, and it's never closed.
4. **Somatic principles filed front and center (my instruction).** Fifteen years of Feldenkrais practice (on and off): effortlessness and ease, *la plage d'aisance* (my teacher's French term — the range of ease), the kinesphere, reversibility of movement, the familiar/unfamiliar/strange zones of "mature behavior" — plus my tangent-lines image of errors as diverging paths that never return. Martial arts: Karate, Tai Chi Qigong, Aikido, the internal martial arts — martial virtues (not civic virtues; not about waging war), economy of motion, meeting force. Taoism (*wu wei* — the same truth as the plage d'aisance, in another tradition) and Stoicism (the dichotomy of control — the audit trail as a Stoic document; *amor fati*, which is why the releases aren't brochures). And the liminal space: Workspace and Lifespace overlap, and the body is the crossing-point. Staged as `somatic-principles-v0.1.md`, NEW, for `Historiotheque/Research/`. Some things I keep private; these principles I share — that boundary is mine to draw, and I drew it.
5. **Research folder READMEs.** `docs/` had no README and neither would `risks/` — both now staged NEW (`docs/README.md` carries the spec versioning/audit conventions; `risks/README.md` states how the taxonomy is used: checklists as its executable form, incident records citing the version, the Pattern Language named as its companion).
6. **Next Actions list created.** A living list at my personal files (NOT GitHub-bound): uploads, today's releases, parked items, reminders, standing habits. First entry class of document of its kind — the operation's own to-do list, kept where I can refer to it.
7. **The "methodology matters" article shared and analyzed.** I sent Oracle the text of my June 23, 2026 Medium article ("ART-OPS-IN-A-BOX: Why Methodology Matters in an Interdisciplinary Art-Research Practice") with explicit instructions: no files, just mirror it back with analysis. His reading, which I endorse: the article is the charter and the repos are the implementation — the log spec is reproducibility as a file format, no-backfill is reproducibility as law, the Pattern Language is the "toolbox of tricks inventoried," the somatic principles are "inhabit their mental and physical spaces" finally filed, the scale-down doctrine is "I am unable to document absolutely everything" grown up, and the ArtOperation manual is the closing design concept (Historiotheque no. 1 → Historiotheques everywhere) built out. Two refinements: emulation-vs-forgery — the article *defends* apprentice-phase copying (Joyce, Burroughs, Cubism) as learning from the inside; the forgery is stopping at the surface without the method ever being built — "copy all the way down or not at all." And "no more secrets" gets its boundary: no more secrets *about method*; the interior stays private — the Workspace/Lifespace distinction doing its job. Proposed next actions recorded (file the article as Markdown; log Noise/Rhythm in the Workspace as design concepts; the emulation doctrine as one paragraph; cite the article in RQ-2026-016's anchors; a noise-vs-error clarifying note for taxonomy v0.2; the "inhabitation manual" standard for the log spec).
8. **Releases published: v1.0.0 of Research and v1.0.0 of DesignConcepts.** Oracle drafted both titles and notes in my voice; I confirmed the bare-version title convention (the title is the version; the notes carry the meaning) and kept the "What's not done" paragraph deliberately — not a brochure. Next: take the Zenodo DOIs and publish the badges to the respective repo READMEs.
9. **The .zenodo.json omission — logged as an operator error, as I ordered.** I published both first releases without committing `.zenodo.json` files. Classification: class 8 (operator error — I forgot the step) compounded with class 5 (workflow/sequencing — the file belongs *before* the first release, per the procedure Oracle gave me that same morning). Consequences: not fatal. The releases published, Zenodo archived the snapshots, the DOIs (concept + version) are minted — nothing is lost. What I lose is metadata: without the file, Zenodo falls back to sparse auto-generated metadata (repo name as title, no creators, no license set). Fixes: (a) edit the metadata directly on Zenodo for both v1.0.0 records — published records allow metadata edits, only the files are frozen — adding proper title, myself as creator with ORCID, description, license; (b) commit `.zenodo.json` to each repo now, so all future releases pick it up automatically at release time (it's read from the tagged snapshot). Mitigation: the release procedure gets a checklist with ".zenodo.json committed?" on it, so the sequencing error doesn't recur. Not a brochure: the error stays in the record, and the failsafe gets built on top of the named error — which is exactly what the taxonomy I published this morning says to do.

Also recorded: the Pattern Language ↔ error taxonomy cross-citation reminder (when both are published, each cites the other).

The qualitative season for this session is mine to name. (Never assigned.)

## Decisions

- **Decision:** Smallest sufficient set of repos; archive/deprecate the extraneous; no new repos for risks, logistics, or hermeneutics — folders under Research. / **Reason:** my decision; my mentor's faceted-taxonomy discipline (representative categories + a DON'T KNOWS drawer). Don't mint infrastructure before the corpus exists.
- **Decision:** Every taxonomy I publish carries a terminal DON'T KNOWS category, never closed. / **Reason:** the discipline above; unclassifiable items wait there until they earn classification.
- **Decision:** Somatic principles filed front and center in `Historiotheque/Research/`; personal details excluded. / **Reason:** my instruction — some things I share, some I keep private; the boundary is mine.
- **Decision:** Release titles are the bare version (`v1.0.0`); the "What's not done" paragraph stays in every release's notes. / **Reason:** semantic-versioning convention (the title is the version, the notes carry the meaning); the not-a-brochure doctrine.
- **Decision:** No individual is named or criticized in this log or any GitHub-bound file. / **Reason:** my STRICT rule — I don't publish criticisms of individuals.
- **Decision:** The .zenodo.json omission is logged as a class-8/class-5 error; fix = manual Zenodo metadata edit for both v1.0.0s + `.zenodo.json` committed now + release-procedure checklist. / **Reason:** not-a-brochure; failsafes are built on named errors.

## Problems and friction

- The .zenodo.json omission (see above) — class 8 compounded with class 5. Caught the same day, fixes sequenced, checklist mitigation ordered.
- I couldn't find the error taxonomy in System Files — turned out to be the staging-vs-GitHub two-stage system: Oracle stages in the Library, I upload. Resolved by attaching the file directly. Worth noting as friction in the handoff, not as anyone's fault.

## Ideas and sketches

- "Inhabitation manuals" (`seed`): logs complete enough that a stranger can temporarily *be* the operator — the strong sense of reproducibility from my June article. Candidate bar for the log spec's next version, or a research question.
- Noise vs. error (`seed`): generative material vs. failure mode — one word, two categories. Clarifying note for taxonomy v0.2.
- Emulation-vs-forgery doctrine (`proposal`): apprentice-phase emulation (legitimate, defended in the article) vs. surface copying without method (forgery). One paragraph — Pattern Language entry or short note.
- "No more secrets about method / the interior stays private" (`seed`): the Workspace/Lifespace boundary stated as the answer to the transparency question.

## Research and references

- My own article, "ART-OPS-IN-A-BOX: Why Methodology Matters in an Interdisciplinary Art-Research Practice" (Medium, 2026-06-23) — shared in chat this session, analyzed, endorsed as the charter of the operation. Candidate for Markdown conversion and filing in the repos. Flag for BIBLIOGRAPHY.md entry (self-citation).

## Feedback and collaboration

Directives I gave Oracle this session: the error taxonomy commissioned from my walk notes (no personal content); repo minimalism stated as doctrine; the somatic principles commissioned with the privacy boundary drawn; the two Research folder READMEs commissioned; the personal Next Actions list commissioned (not GitHub-bound); both release titles/notes commissioned, then confirmed (bare-version convention; "What's not done" kept); the .zenodo.json omission ordered into this log as an operator error; no individual to be mentioned (STRICT); the season left for me to name.

## Reproducibility notes

Not an experimental session. The session's durable outputs: this log; `error-taxonomy-v0.1.md` and `somatic-principles-v0.1.md` (staged, upload pending); `docs/README.md` and `risks/README.md` (staged); the personal Next Actions list (Library, not GitHub-bound); two release-notes staging files; two published releases — v1.0.0 `Historiotheque/Research` and v1.0.0 `Historiotheque/DesignConcepts` — with Zenodo DOIs minted and README badges pending, plus the .zenodo.json fix sequenced. Re-running the session means re-reading those files and the chat record of the article analysis.

## Artifacts produced

**Text:** title: Studio log 2026-09-25-1200 release-day session (this file) · abstract: Spec-v1.4 record of the walk field recordings, the error taxonomy v0.1, the somatic principles v0.1, repo minimalism doctrine, Research folder READMEs, the personal Next Actions list, the "methodology matters" article analysis, the v1.0.0 releases of Research and DesignConcepts, and the .zenodo.json omission logged as an operator error. Written in the first person — the Chief Art Operator is the author. · keywords: studio-log, error-taxonomy, somatic-principles, releases, zenodo, operator-error · date: 2026-09-25 · file: `Historiotheque/studio-logs/2026-09-25-1200-release-day-session.md`

**Text:** title: Error taxonomy for Art Operations v0.1 · abstract: Ten error classes (incl. DON'T KNOWS), S1–S5 severity scale, blast radius, compounding rules, mitigation map — the risk-management layer of the operation. · keywords: error-taxonomy, risk · date: 2026-09-25 · file: `Historiotheque/Research/risks/error-taxonomy-v0.1.md` — staged, upload pending

**Text:** title: Somatic principles for the Art Operation v0.1 · abstract: Feldenkrais (plage d'aisance, kinesphere, reversibility), the internal martial arts (martial virtues, economy, meeting force), Taoism (wu wei), Stoicism (dichotomy of control, amor fati), the liminal Workspace/Lifespace overlap. · keywords: somatic-principles, feldenkrais, operator · date: 2026-09-25 · file: `Historiotheque/Research/somatic-principles-v0.1.md` — staged, upload pending

**Text:** title: Research folder READMEs (docs/, risks/) · abstract: Index READMEs for the two folders; docs/ carries the spec versioning/audit conventions, risks/ states the taxonomy's use. · keywords: readme, research-repo · date: 2026-09-25 · file: `Historiotheque/Research/docs/README.md`, `Historiotheque/Research/risks/README.md` — staged, upload pending

**Text (personal, not GitHub-bound):** title: Next Actions — Chief Art Operator · abstract: Living to-do list: uploads, releases, parked items, reminders, standing habits. · keywords: next-actions · date: 2026-09-25 · file: Library personal file (not GitHub-bound)

**Published:** Release v1.0.0, `Historiotheque/Research` — first release, scholarly apparatus; Zenodo DOI minted, README badge pending. / Release v1.0.0, `Historiotheque/DesignConcepts` — first release, design-concepts laboratory; Zenodo DOI minted, README badge pending.

## Next actions

- Upload the pending batches to GitHub, in my sequence — owner: me — when: manual (error taxonomy + risks README; somatic principles; docs README; this log + studio-logs README)
- Take the Zenodo DOIs → publish the badges to the Research and DesignConcepts READMEs — owner: me — when: now
- Fix .zenodo.json: manually edit v1.0.0 metadata on Zenodo (title, creator + ORCID, description, license) for both repos; commit `.zenodo.json` to each repo for future releases — owner: me (Oracle drafts the files on my word) — when: today
- Add ".zenodo.json committed?" to the release procedure checklist — owner: Oracle — when: next procedure touch
- Name the qualitative season for this session — owner: me — when: now
- Verify the governance build landed — owner: Oracle — when: Sat 2026-09-26 ~19:20 EDT (cron set)
- Answer the 5 clarifying questions for the v5.2.0 Release draft — owner: me — when: whenever
- DevOps side chat: full Git/GitHub Desktop lesson + CulturalSoftware fork execution — owner: me + Oracle — when: my word
- Ostrom knowledge-commons reading brief; Cultural Software README rewrite draft — owner: Oracle — when: on my word
