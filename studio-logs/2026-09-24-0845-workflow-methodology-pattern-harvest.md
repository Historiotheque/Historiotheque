---
date: 2026-09-24
time_start: "08:44"
time_end: "10:30"
timezone: America/Toronto
season: TBD — ask Alex (not assigned)
project: [historiotheque]
stream: [text]
session_type: admin
workspace: historiotheque
refcards: []
tags: [methodology, devops, github-desktop, vscode, obsidian, switchboard-method, interruption-science, pattern-language, RQ-2026-018]
related:
  - ../research-questions/RQ-2026-018-interruption-native-practice.md
---

## What I did

Morning methodology session in "The Historiotheque" side chat — the DevOps loop
gets built for real, and the workflow methodology gets its first formal
treatment. In order:

1. **GitHub Desktop installed.** On the Configure Git screen: kept Name = A.G.
   and the GitHub private noreply email (address withheld — privacy-preserving
   stand-in; already configured)
   default; the real email never touches public commits.
2. **Cloned `Historiotheque/Research`** via the URL tab. Local path moved out of
   OneDrive (`Documents\GitHub\Research` → non-synced path) — OneDrive sync
   fights git over file locks and can corrupt `.git`.
3. **VS Code installed** (User installer, default path
   `AppData\Local\Programs\Microsoft VS Code`). Ticked "Add to PATH" on the
   Additional Tasks screen. Signed in with GitHub → Copilot free tier + Settings
   Sync.
4. **Obsidian vault sorted.** "THE REVOLT OF FICTION" was already top-level
   (misread of the tree — it is a sibling of REFCARDS_SYSTEM, not nested).
   Settled the big framing: **Obsidian = Thinking/ideation space, GitHub +
   VS Code = Making/publishing space.** Vault to be renamed IDEATION_VAULT (or
   similar); advised *against* REFCARDS_SYSTEM as the vault name — "refcard" now
   means the canonical RC-2026-NNNN artifacts, and the term must not drift.
   Rename route: quit Obsidian entirely, rename the folder in Explorer, reopen
   as vault (the vault manager UI no longer shows an obvious "close vault").
5. **Issues vs Projects doctrine.** Start with Issues — the planning/intention
   layer (what I intend; commits = what changed, logs = what happened). Projects
   kanban only when an issue list gets long enough to earn a board view. Both
   are web-only; GitHub Desktop doesn't show them.
6. **Solo-dev pitfalls canon.** Dropped threads as the core failure (working
   memory overload, no teammate to catch the thread), then the rogues' gallery:
   "I'll remember this", no definition of done, big-bang commits, the hijack,
   toolchain fiddling, version chaos, docs-at-the-end, no review ritual,
   feast-or-famine pacing. The synthesized system: capture → prioritize →
   small batch → commit → log → review.
7. **Capture points, deeply.** Governing principle: capture friction must stay
   below idea-decay rate. The always-open inbox, capture-the-handle, and the
   **resumption token** (the next physical action, left mid-sentence when
   switching — the anti-dropped-thread device). His distributed notebooks +
   timestamp habit validated as temporal indexing; the notebooks are sensors,
   Obsidian is the aggregator.
8. **Switchboard Method formalized.** Proximate task selection = **stack-pop
   scheduling** (LIFO on the desk pile / mind pile) — direct link to the
   Stacks-Project. The switching is the method; what gets automated is the
   switch *ritual*, not the selection. Planned: a Python script prompting for
   the resumption token + capture on every switch.
9. **RQ-2026-018 drafted** — "Can interruption be treated as the scheduling
   signal of an art operation?" Core inversion: the HCI literature treats
   interruption as damage to minimize; the Switchboard treats it as the
   scheduler. Filed as NEW; living index README updated (MODIFIED); both on the
   upload checklist, batch 2026-09-24.
10. **Pattern language planning.** Recommended title: *A Pattern Language for
    Art Operations*. Pattern form (Name → Context → Problem/forces → Solution
    → Consequences → Related) and antipattern form (Name → Context → Symptoms
    → Consequences → Refactored solution). Organize by workflow phase
    (Capture → Plan → Execute → Log → Review → Publish). ID scheme
    PAT-2026-NNN / APAT-2026-NNN. Seed corpus: 24 stubs harvested in a
    first pass over the 8 studio logs + recent conversations (first pass ≈ one
    .md file of cost; full pattern-form drafts deferred as a scaffold-zip-sized
    job). Home: start as a section under `Historiotheque/Research` `methods/`,
    earn its own repo when it outgrows it.
11. **Standing nudge recorded:** remind him about digitizing/scanning the paper
    notebooks and drawings (incl. the walking notebook) whenever conversation
    drifts anywhere near paper, notebooks, or walking.

## Decisions

**Decision:** Git identity = A.G. + GitHub noreply email.
**Reason:** Privacy — public commits expose author emails; the noreply address
still links commits to the account.

**Decision:** Local clones live outside OneDrive.
**Reason:** Sync conflicts with git internals; known corruption risk.

**Decision:** Obsidian is the Thinking space; GitHub/VS Code the Making space.
**Reason:** Ideation and publication need different tools and different
discipline; mixing them was the source of the vault-naming confusion.

**Decision:** Don't name the vault REFCARDS_SYSTEM.
**Reason:** Protects the canonical meaning of "refcard" (RC-2026-NNNN, GitHub
repo). Terms are load-bearing.

**Decision:** Issues first, Projects later (maybe).
**Reason:** Issues are the work; Projects is a view. A board with three cards
is theater.

**Decision:** Pattern language starts in Research/methods/, earns a repo later.
**Reason:** Don't mint infrastructure before the corpus exists.

## Problems and friction

- The Obsidian vault manager no longer shows an obvious "close this vault" —
  worked around via quit-and-rename. (Stale procedural knowledge; flagged, not
  guessed.)
- Token-cost honesty held: the harvest first pass was scoped to stubs
  (≈ one .md file); full pattern-form drafts explicitly deferred.
- Drafting slip: the rewritten living-index README mangled the RQ-2026-012
  line ("trickle-up from institutions or trickle-up from the workshop") —
  caught on re-read and fixed before filing.

## Ideas and sketches

- `seed`: Python switch-ritual prompter — on every task switch, asks for the
  resumption token and confirms the incoming idea was captured. Ten seconds,
  enforced by the machine.
- `seed`: GitHub CLI (`gh`) for issue creation from the terminal; Everything
  (voidtools) for instant file search; QuickAdd plugin for hotkey capture
  straight into the Obsidian inbox; GitHub issue templates with his own
  structure (goal, done-condition, notes).
- `seed`: Interruption science as his research — the interruption-*native*
  practice vs. the literature's damage-minimization. Low latent inhibition as
  instrument, not liability.
- `seed`: The pattern language is the meta-project — 20–30 years of practice
  made explicit as methodology. The patterns are the "how" layer, sitting
  alongside the specs in the three-layer model.

## Research and references

- RQ-2026-018 (this session) — filed NEW, index MODIFIED, checklist batch
  2026-09-24.
- Alexander (1977), GoF (1994), Coplien (organizational patterns),
  Brown et al. *AntiPatterns* (1998) — the pattern-language lineage, via
  conversation.
- Gloria Mark / HCI interruption literature — the inverted literature for
  RQ-2026-018.

## Next

- Second log planned today: the walk (cemetery meditation/prayer, possible
  field recordings, photos, Reels) — field session; then the afternoon at J.'s.
- Season field left TBD per the ask-don't-assign rule — Alex to fill.
