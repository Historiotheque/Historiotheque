---
date: 2026-09-25
time_start: "07:00"
time_end: "09:35"
timezone: America/Toronto
season: autumn
project: []
stream: [text]
session_type: research
workspace: historiotheque
refcards: []
tags: [pattern-language, doctrines, audit-trail, cultural-software, doi, zenodo, devops, scale-down, governance]
related:
  - studio-logs/2026-09-24-2230-governance-design.md
---

## What I did

Overnight (~00:30): I had Oracle execute the governance build, accepting the usage-limit risk. Fifteen files under `Historiotheque/governance/` (+`ethics/`), zip built and verified locally. Upload still pending — manual, on my side, sequenced with my other batches.

Morning session (~07:00–09:35), in order:

1. **Solo-dev pitfalls, deep-dived.** At my request Oracle elaborated the "working-memory monolith" material from yesterday (externalize state, WIP limits, modularity/next-move cards, interrupt handlers, tests as executable memory, convention over decision, scheduled collapse, exocortex), then delivered nine more pitfalls with programmer-grade countermeasures: no code review → blind-spot compounding; the hero cycle → circuit breaker (sleep as canary); yak-shaving → tooling budget; bike-shedding → two-way-door sort; the rewrite trap → strangler fig; big ball of mud → boy scout rule; documentation debt; Switchboard depth tension → shallow/deep modes; premature abstraction as a strength to protect. All offered as Pattern Language candidates, none filed.
2. **Pattern Language status confirmed.** First pass done 2026-09-24 (24 stubs, Capture→Plan→Execute→Log→Review→Publish, PAT/APAT IDs). Second-pass candidates from this morning's pitfalls folded into the draft-in-memory. Full pattern-form edition deferred in stages, on my word.
3. **Tap-on-shoulder standing instruction** (my words): every time Oracle notices me describing something in my practice that looks like a pattern/antipattern candidate, he asks whether it should go in the Pattern Language. Prompt, don't file. Same rhythm as the governance nudge.
4. **DesignConcepts descriptions rewritten** after I broadened the repo concept (novels-only → novel/series/album/workspace/Art Operation). Three copy-paste staging files written and attached (my client mangles chat formatting). I applied the org bullet and index row myself; the README rewrite turned out byte-identical to my current version — no commit, file left intact.
5. **Doctrines adopted.** Terminology rule (my correction): in GitHub-bound files, only MY words for my concepts; new terms proposed explicitly in chat first — this after "apparatus" turned out to be Oracle's unasked shorthand for my "repositories, checklists, procedures." No-backfill doctrine (mine): the audit trail stays intact or the operation's credibility goes out the window; spec changes get changelogs, never rewrites of old records. Reconstruction marking (my instruction): every reconstructed record carries at least one line stating it was reconstructed.
6. **Release timeline confirmed:** May 1 soft v5.0.0 → May 21 MAJOR v5.0.0 → July 3 MINOR v5.1.0 → next is MINOR v5.2.0. My open calls: whether to mention generative AI; how much forward-looking material goes in the Release vs the Declaration.
7. **Pattern Language placement decided:** folder under `Historiotheque/Research` `methods/` now; standalone repo when it earns it. Folder test passed (coherent family, needs its own index); repo test not yet (no independent audience, release rhythm, or publication-scale corpus).
8. **DOI practice settled.** I worried early DOIing looked like minting without work. Verdict: it's the designed use — the concept DOI is for exactly this (stable identifier for an evolving project, always resolving to latest); version DOIs ride my real releases. FORCE11's Importance principle ("software is a legitimate research product, same citation importance as papers or books") adopted as load-bearing for the practice. Published Zenodo records can't be self-deleted (files frozen; metadata editable; supersede by new version) — but with versioning, that doesn't matter.
9. **Cultural Software elaborated at length.** I had Oracle take my antiface README (DOI 10.5281/zenodo.17395458) and rewrite the concept from inside the running system: the six FORCE11 principles mapped onto things I already built (ID schemes, audit trail, semantic versioning, open working record); the org as the concept scaled from package to distribution; the Zenodo Community as the persistence layer; Cultural DevOps as the missing ops discipline; the Pattern Language as source-code documentation. Thesis: the README described the concept from outside; the operation now IS an instance of it. Oracle offered to draft the README update — pending my word.
10. **CulturalSoftware fork plan** (high-level, detailed lesson parked for the DevOps side chat): fork antiface/CulturalSoftware → Historiotheque org via the Owner dropdown; a hard fork — history preserved, no pulls/merges back, like LibreOffice/OpenOffice; the antiface line stays frozen as the early theory under its DOI; the org line gets its own DOI series and holds the generalized theory (culture as software, psychotechnology). CulturalDevOps stays a separate future repo: theory vs. operations.
11. **Path hygiene ruled on.** `C:\Dev\Playground\.venv\Scripts\python.exe`-style paths are 100% fine in public files (industry-normal; exact paths aid reproducibility). The actual risk in a filepath is the username inside `C:\Users\...` — that's why people redact. We scanned the 2026-09-24 devops log: all paths are `C:\Dev\...`, no username anywhere. Nothing to fix. Recorded as STRICT: no username-bearing paths in GitHub-bound files, ever; Oracle gates every such file before staging.
12. **Ostrom parked:** I want to read up on Elinor Ostrom's knowledge-as-commons. Reading brief on offer; no browser without my word.

**The important note, as instructed — the scale-down doctrine (my words, my decision):** the operation will scale down *by design* to avoid anything resembling burnout. "We can't afford that luxury anymore" — the Art Operation @ The Historiotheque is too important for a whole season of dramatically reduced production. Fallow seasons remain, but they will come from rest and deliberate throttling, not from collapse. The distinction: burnout → shutdown is the fallow arriving *after* the fact, costing a season; scale-down → rest is the fallow *scheduled*, and the operation never fully stops. This is the circuit breaker from this morning's pitfalls, promoted from pattern to doctrine.

Also parked, for later development: the **failure-by-design** dossier (my term) — the Official Releases deliberately document failures, a philosophy with elements of Chaos Engineering ("fail on purpose"); and **Code Genres** — all media and all genres as code genres (cuneiform tablet, modern novel, Hollywood film), relevant to the Cultural Software theory. On the audit trail itself, my stated position: do everything possible to preserve it, up to but not including cryptographic measures (hashing etc.) — that stays beyond the feasibility filter.

My closing note: I go on with my day "with a clear conscience and in peace at knowing that I did my absolute best," doing "some of my very best work, and most critically important work, ever."

The qualitative season for this session is mine to name. (Never assigned.)

## Decisions

- **Decision:** Adopt the scale-down doctrine: throttle the operation by design; fallow seasons come from rest, never from burnout. / **Reason:** the operation is too important to risk a burnout-collapsed season; a scheduled fallow costs nothing, a collapse costs a season. (My decision, my words.)
- **Decision:** Studio logs record the Operation only — no personal or mundane matters (groceries, meals, medication, prayer/meditation). / **Reason:** my explicit rule; the logs are the operation's record, not a diary.
- **Decision:** Pattern Language lives in `Historiotheque/Research` `methods/` as a folder now; earns a standalone repo later. / **Reason:** passes the folder test (needs its own index), not yet the repo test (no independent audience or release rhythm). Don't mint infrastructure before the corpus exists.
- **Decision:** Fork (hard fork) antiface/CulturalSoftware into the Historiotheque org; never pull/merge between the lines. / **Reason:** the org line is a total refurbishment of the foundations, not a feature branch; the fork preserves history and provenance, the antiface line stays frozen as the early theory under its DOI.
- **Decision:** Keep DOIing repositories early (concept DOI from day one); version DOIs ride real releases only. / **Reason:** early DOIing is the designed use (citability + archiving), not abuse; the FORCE11 Importance principle makes the software a first-class research product.
- **Decision:** Terminology rule — only my words for my concepts in GitHub-bound files; new terms proposed explicitly in chat first, never installed silently. / **Reason:** "apparatus" was Oracle's unasked shorthand; my vocabulary is load-bearing.
- **Decision:** No-backfill doctrine — old records stand under the spec of their date; spec changes get changelogs. / **Reason:** my rationale — the audit trail intact or the operation's credibility goes out the window.
- **Decision:** Every reconstructed record carries at least one line stating it was reconstructed (date + sources). / **Reason:** my instruction — silent reconstruction forges the audit trail.
- **Decision:** STRICT path hygiene — no username/machine-identifying segments in local paths published to GitHub; generic paths (`C:\Dev`) are fine; Oracle gates every GitHub-bound file before staging. / **Reason:** my "come back and bite me" rule; the username is the actual risk in a path.
- **Decision:** "Not a brochure" — failures and errors stay in the record; Official Releases show the record as-is. / **Reason:** my principle; the releases' authority comes from showing what happened, including the failures.
- **Decision:** Park the marked-correction-vs-backfill distinction for a future governance draft; do not file it now. / **Reason:** my call — parked, not decided.

## Problems and friction

- Could not recover the exact wording of Oracle's earlier "working memory" remarks (compacted context) — said so honestly instead of reconstructing, then delivered the full elaboration from my four bullets.
- The DesignConcepts README rewrite came back byte-identical to my current version — no commit possible; staging file left intact, deleted later.
- "Apparatus" was Oracle's term, installed unasked — I caught it, corrected the same session; it became the terminology rule.
- First draft of this log was written in the third person ("the operator") — wrong voice for my own logs; rewrote it in the first person before upload. (Not a brochure: the error stays in the record.)

## Ideas and sketches

- Failure-by-design dossier (`seed`): the deliberate documentation of failures in the Official Releases, with elements of Chaos Engineering; its own philosophy, to be developed.
- Code Genres (`seed`): all media and genres as code genres — cuneiform clay tablet, modern novel, Hollywood film; feeds the Cultural Software theory.
- CulturalDevOps repository (`proposal`): the ops discipline and its philosophy, separate from the CulturalSoftware theory repo.
- Marked correction vs. backfill (`proposal`, parked): removing PII/safety issues from a published record is a declared correction, not a falsification; silent editing would be the violation. For a future governance draft.
- Pattern Language second-pass candidates (`proposal`): this morning's ten pitfalls/antipatterns plus the scale-down doctrine (PAT Designed Scale-Down vs APAT Burnout-Driven Shutdown).
- Ostrom knowledge-commons reading (`seed`): I want to read up; brief on offer.

## Research and references

- FORCE11 Software Citation Principles (2016) — Importance, Credit and attribution, Unique identification, Persistence, Accessibility, Specificity. Consulted via my own lookup; the Importance principle quoted verbatim in session. Flag for BIBLIOGRAPHY.md entry.
- Ostrom, Elinor — knowledge as commons. Parked as a reading item at my request; not yet consulted.

## Feedback and collaboration

Corrections and directives I gave Oracle in this chat: the terminology correction ("apparatus"); the scale-down note commissioned for this log; the "not a brochure" principle restated; the filepath question that produced the STRICT path-hygiene rule; the fork-vs-new-repo question steered to a hard fork; the Cultural Software elaboration commissioned and the README rewrite offered (pending); the first-person-voice correction applied to this very log.

## Reproducibility notes

Not an experimental session. The session's durable outputs: this log; the doctrines and standing instructions recorded in Oracle's operating manual (tap-on-shoulder, terminology rule, no-backfill, reconstruction marking, path hygiene) and the memory log for 2026-09-25 (scale-down doctrine, fork plan, parked items, DOI verdicts). Re-running the session means re-reading those files myself.

## Artifacts produced

**Text:** title: Studio log 2026-09-25-0700 doctrine session (this file) · abstract: Spec-v1.3 record of the overnight governance build and the morning doctrine session: solo-dev pitfalls, Pattern Language status and placement, terminology/no-backfill/reconstruction doctrines, DOI/FORCE11 verdicts, Cultural Software elaboration, fork plan, path hygiene, and the adopted scale-down doctrine. Written in the first person — the Chief Art Operator is the author. · keywords: studio-log, doctrines, pattern-language, cultural-software, audit-trail · date: 2026-09-25 · file: `Historiotheque/studio-logs/2026-09-25-0700-doctrine-session.md`

**Text:** title: Governance build 2026-09-25 (15 files + zip) · abstract: Full governance repository build executed overnight at my direction: 15 files under governance/ (+ethics/), zip verified locally. Upload pending, manual. · keywords: governance, build · date: 2026-09-25 · file: `Historiotheque/governance/` (+ethics/) — staged, upload pending

**Text (transient):** title: DesignConcepts copy-paste staging files (3) · abstract: Org profile, index row, and README rewrites staged as attachable files; org bullet + index row applied by me, README byte-identical (no commit). · keywords: design-concepts, staging · date: 2026-09-25 · file: local staging copies (transient, deleted after pasting)

## Next actions

- Upload the pending batches to GitHub, in my sequence — owner: me — when: manual (governance batch: 15 NEW; studio-log batch: this log NEW + README check)
- Verify the governance build landed — owner: Oracle — when: Sat 2026-09-26 ~19:20 EDT (cron set)
- Answer the 5 clarifying questions for the v5.2.0 Release draft — owner: me — when: whenever
- DevOps side chat: full Git/GitHub Desktop lesson (clone, fetch/pull, merge, PRs) + CulturalSoftware fork execution — owner: me + Oracle — when: my word
- Ostrom knowledge-commons reading brief — owner: Oracle — when: on my word
- Cultural Software README rewrite draft — owner: Oracle — when: on my word
- GitHub Desktop practice on test repos — owner: me — when: my plan
