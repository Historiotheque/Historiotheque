---
date: 2026-10-18
date_end: 2026-10-20
sessions:
  - "2026-10-18 02:22 → 02:50"
  - "2026-10-18 05:43 → 05:56"
  - "2026-10-18 09:45 → 10:01"
  - "2026-10-18 20:54 → 21:54"
  - "2026-10-19 09:10 → 10:36"
  - "2026-10-19 13:25 → 13:44"
  - "2026-10-20 04:41 → 05:05"
timezone: America/Toronto
season: autumn
project: [historiotheque, experimental-novel, deep-archives, work-system]
stream: [text, mixed]
session_type: [publishing, documenting, reviewing, discourse, drafting, creating, designing, research, logging]
workspace: [lab, field]
refcards: []
tags: [movement-only, provenance, opentimestamps, merkle-tree, commit-ledger, series-bible-v1.1, novel-log-6, jsonl, work-system-log, two-streams, delivered-draft-preservation, rfc-3161]
related:
  - studio-logs/2026-10-18-0140-the-record-and-the-remainder.md
  - work-system-logs/work-system-log_2026-10-17_evening.jsonl
---

## What I did

The previous log closed at 01:45 on October 18; this window opens with
its correction and publication, and then the work changes key. A bible
and a novel log were drafted in one early-morning stretch and have since
been pushed. Two small tools were built for the version history itself:
a ledger that records my commits, and a Merkle-tree script. Then the
question underneath the whole log architecture — how a chain of hashes
can be made incontestable to a future stranger — was taken up in
earnest, and became a practice: a provenance design settled in public,
and a first stamp carried through and pushed. The window closes with
the machine-readable stream continued to this morning, and with a rule
I adopted for these logs themselves: a studio log no longer carries an
item merely because it remains unfinished; it carries it only when its
state changes. What did not move in this window is not here.

## 2026-10-18 02:22 → 02:50 — workspace=[lab] × session_type=[documenting, publishing] — the previous log, corrected and published
ΔW temp = exact, methodical, recursive

The corrections to the previous log, in one compact segment, as I ruled
it should be. Three of its statuses were wrong in the direction of
modesty and were set right on my report: the REFMATS rename and the
work-system alpha package had been committed in a previous commit, not
in the log's own; the 3.0.2 reader summary was already pushed. Johannes
Panikkar is now identified in the log as what he is — a fictional
character in the trilogy. When I charged that more than the corrections
had changed, the delivered draft was recovered exactly — each amendment
had been an exact replacement, and reversing the nine of them restored
the file as delivered; the diff between the two versions showed nine
hunks, all at correction sites, everything else byte-identical. Two
rulings came out of the round and stand from here: a delivered draft is
frozen as a separate file before any amendment round, and a commit
summary carries the main changes only, never a retelling of the log it
carries. I pushed the log.

## 2026-10-18 — workspace=[lab] × session_type=[reviewing, discourse] — an accounting of the novel channel
ΔW temp = lucid, methodical, settling

Minutes after the push I asked for a full accounting of the novel
channel since its last log: what was staged and ready, what awaited my
decision, what awaited my correction pass, and — I asked for this
explicitly — which points the record itself was unsure of. The
accounting separated the three cleanly. Its drafting consequences are
the next session; the items it listed that did not move in this window
are not carried here.

## 2026-10-18 05:43 → 05:56 — workspace=[lab] × session_type=[drafting, discourse] — the bible, second version
ΔW temp = dense, lucid, tightening

I set aside the review-first plan and gave the simpler instruction:
draft v1.1, and I will compare it with the existing version directly.
The draft was written that morning: 5,230 words against v1.0's 2,664,
in my first person throughout, standing as a second dated file beside
v1.0, which is untouched. Where the fold map built from the audit
conflicted with my rulings of the night before, my rulings governed.
The savior ending of §9 stands unrevised — voice converted, nothing
else — with the fatal flaw and the two-endings annex structure set
around it. The Interzone fold markers were not applied at drafting; the
file was left as it stood while I read it. Status: pushed (my report,
October 20).

## — workspace=[lab] × session_type=[drafting, documenting] — novel log #6
ΔW temp = methodical, dense, settling

In the same stretch I confirmed that novel log #5 is already in the
repository, and novel log #6 was drafted: a dated digest of October 17
into 18 — the audits, the rulings, the flaw, the re-homing — kept to
its own span and its Interzone spine, its index row added. It went up
with its batch: the log and its row, the bible at v1.1, the Interzone
entries with their redaction note, and the Chronotopium README's flaw
section. Status: pushed (my report, October 20).

## 2026-10-18 09:45 → 10:01 — workspace=[lab] × session_type=[creating, documenting] — a ledger for the commits themselves
ΔW temp = exact, methodical, tightening

I asked for a Python script that logs my commits — the hashes and the
main pieces — from one local folder that sits in no repository, so the
ledger can never be swept into a push. `commit_log.py` was built and
tested: on its first run against a clone it records the whole backlog,
back to the first commit; after that it appends only what is new, dedup
by hash, in the same JSONL form as the work-system log, author names
only and never addresses. A privacy audit of the delivered file: it
runs read-only git commands against my local clones, holds no network
code, and writes only beside itself. On its first real run it crashed
before writing anything. The script was fixed the same morning to go
looking for git itself, and to explain itself plainly, with no
traceback, if git still cannot be found.

## 2026-10-18 20:54 → 21:54 — workspace=[field, lab] × session_type=[discourse, publishing] — what the log leaves out
ΔW temp = glowing, loose, lucid

That morning, in the field, I recorded a short video on the work I am
studying: logging, provenance, archival standards — and the conclusion
the study keeps arriving at, that it is impossible to log everything;
some data is always left out; the log is a selection whether we admit
it or not. In the evening the post text for the video and a companion
text were drafted, five hashtags at my cap. It is the remainder
doctrine of the treatise, said in public, in one minute: the record is
not the experience, and it is not the whole of the event either.

## — workspace=[lab] × session_type=[research, discourse] — provenance, made incontestable
ΔW temp = lucid, tightening, exact

The provenance question, opened the day before as subject matter, now
as practice. Its framing — provenance as a chain of custody, answerable
to a hostile reader — is the article's (Yuhe He, cited under Research
and references); the deliberation that follows is the one it set off.
The weak point stated plainly: a self-contained hash chain
is forgeable — whoever holds the files can recompute every link — and a
commit's dates are claims, not evidence. A chain proves what follows
what; it cannot prove when. What makes provenance hold for a stranger
is anchoring the chain to witnesses I do not control, and I already own
most of that stack: my signature on the commits (who), the push to
GitHub (a copy of the chain outside my hands), the Zenodo version DOI
(an institution's timestamp), and OpenTimestamps (a Bitcoin anchor —
proof a thing existed no later than a given block, at block grain,
never an exact time, which fits my time-honesty rule rather than
fighting it). The other species were surveyed the same evening:
institutional clocks, RFC 3161 timestamp authorities, transparency
logs. No method was adopted that evening. A comparison of editors for
the git work ran as switch texture; no decision was taken on it.

## — workspace=[lab] × session_type=[creating] — a Merkle tree, in a small script
ΔW temp = exact, methodical, recursive

At my request, `merkletree.py` was built and tested the same evening:
it takes a folder of files, or a list — my commit hashes work as-is —
and produces a manifest and a single root hash; it verifies a set
against the manifest, and prints an inclusion proof for a single leaf.
In testing, one word changed in one file produced a mismatch. A root
is a fingerprint of a whole set, in order: it does not anchor anything
by itself, but it gives the anchor one small thing to hold.

## 2026-10-19 09:10 → 10:36 — workspace=[lab] × session_type=[designing, research] — the design settled: proofs in public
ΔW temp = conclusive, exact, methodical

The implementation questions, worked through one by one until the
design stood. What gets stamped is not each changed file — a commit
changes several — but the commit itself, named in a small stamp file:
the repository, the full hash, the subject line, the day of stamping,
and a line pointing at its proof. A release stands on one commit — the
v1.1.0 release's is 0587305, whose page shows that commit's own small
diff, not the release; the release is the whole tree at that commit.
Two stamp forms: one for releases (with the version DOI), one for plain
commits, with an optional line for what the commit marks. Cadence:
every release, and the commits that mark something. The folder gets a
README written for the stranger: what the stamp/proof pair is, what it
does and does not prove, and how to verify it in under a minute. And
one correction of mine governs the whole design: the first sketch kept
the proofs in a local folder. That defeats the purpose — the stamp
files and their .ots proofs live PUBLIC, in a `provenance/` folder at
each repository's root, where a stranger can obtain and verify them.
The local folder keeps only the tooling and a backup mirror. An .ots
has a two-commit life: it is committed in its pending state at stamp
time, and committed again, the same file upgraded in place, once its
Bitcoin anchor completes.

## — workspace=[lab] × session_type=[publishing, documenting] — the first stamp
ΔW temp = exact, methodical, dense

The first stamp was carried through for the Historiotheque v1.1.0
release: the stamp file completed — its subject line verified from the
commit page, its version DOI checked against Zenodo — the provenance
README written, and the proof produced. The proof was made with the
official web tool, which produces the same .ots file; that is the way
I stamp. Status: the provenance folder, the stamp
file, and the pending proof are pushed (my report, October 20). The
.ots upgrade has not been done — I verified that this morning; the
proof stands in its pending state until its anchor completes and I
upgrade it in place.

## 2026-10-19 13:25 → 13:44 — workspace=[lab] × session_type=[research, discourse] — an unasked manifest; a second kind of witness
ΔW temp = raw, recursive, lucid

Two shorter matters. First, a manifest I never asked for: background
work had run the new Merkle tool over my releases archive and produced
a manifest of it, and I challenged it — when had I asked for this, and
what is it for? It was answered plainly: I had not asked; the file is a
fixity fingerprint of the archive and nothing more, and nothing is
expected of me for it. Whether it is deleted or left parked is my
ruling to give. Second, the timestamp authorities: I want to experiment
with RFC 3161 authorities for field recordings and documents, and a
workflow was prepared — a signed timestamp from an authority is precise
and instant, but it rests on one authority's trust and on care with its
certificates; OpenTimestamps is trustless and permanent, at block
grain. The two are different species of witness, and they can be
layered. No authority has been tried yet.

## 2026-10-20 04:41 → 05:05 — workspace=[lab] × session_type=[logging, discourse] — the continuation, chained
ΔW temp = recursive, dense, methodical

The work-system log was continued in its second stream: eleven records
covering October 18 to this morning, built in the LOGGING channel, the
new file's first record chained to the evening file's last line, the
whole chain validated unbroken across both files. Main points of the
work channels only; the private channels are outside this stream's
scope by design, and its closing snapshot says so. The snapshot's
states were overtaken within the hour by the confirmations below — the
bible and the novel log stand in it as drafts awaiting me, and the
first stamp as ready to commit. Those lines are not to be edited: the
stream is append-only, and the remedy is appended records that
supersede them. The first evening file's own state stands as the
previous log recorded it — pushed, with its alpha spec and schema —
and I confirmed it again in the status pass below (my report,
October 20). The superseding records were appended after that pass,
at my word; the file holds fourteen records as committed.

## — workspace=[lab] × session_type=[discourse, drafting] — movement only; this log
ΔW temp = lucid, conclusive, settling

Then the statuses were settled in one pass, on my word: the series
bible v1.1 was pushed the other day; novel log #6 was pushed; the first
provenance stamp was pushed, its upgrade still undone; novel log #5 was
pushed a while back. And the rule for these logs was adopted, in my
words: the studio log will no longer carry an item merely because it
remains unfinished; it will carry it only when its state changes. The
log-about-log work of this window is held to the one compact segment
above, by the same decision. This log was drafted on that basis — since
the last log closed, from all the relevant channels, with what did not
move left out.

## Decisions

**Decision:** The provenance proofs live public, in a `provenance/` folder at each repository's root; the local folder keeps only the tooling and a backup mirror.
**Reason:** Availability to the stranger is half the point of the proof; a proof only I can produce is a promise, not a proof.

**Decision:** What is stamped is the commit, named in a stamp file — never each changed file, and never the whole repository file by file. Cadence: every release, plus the commits that mark something. Two forms, for releases and for plain commits.
**Reason:** A commit hash already covers the whole tree at that commit; the stamp file explains itself to whoever finds it.

**Decision:** A pending .ots is committed at stamp time, and the same file is committed again, alone, after its upgrade completes it in place.
**Reason:** The proof travels with the record from the start; the upgrade only completes the same proof and leaves no second file.

**Decision:** The studio log will no longer carry an item merely because it remains unfinished; it will carry it only when its state changes.
**Reason:** Unfinished business carried from log to log dilutes the record. Open state has its own homes — the machine-readable stream's snapshots, the channels, the commit ledger; the studio log is the record of what moved.

**Decision:** A delivered draft is frozen as a separate file before any amendment round; amendments are exact replacements, and the original stays comparable.
**Reason:** A draft the author cannot compare against its amendment is a record already blurred.

**Decision:** A commit summary carries the main changes only.
**Reason:** The summary is not a second log.

## Problems and friction

- Push states, again: the previous log needed a correction round because its statuses rested on a general report of mine that I qualified in the same breath I gave it. The states that mattered were settled item by item in this window, on my word — and the deeper flaw stands as I admitted it there: I cannot keep track of everything I commit, and I keep failing to dictate what I actually push.
- The commit ledger's first real run crashed before writing anything. The script was fixed the same morning; the crash cost nothing but the run.
- An artifact I never asked for: a Merkle manifest of the releases archive, built by background work exercising a tool I had requested, over a set I had not named. It was disclosed when I challenged it, and answered for plainly. My ruling on it — delete, or leave parked — is still mine to give.
- The machine-readable continuation's closing snapshot was stale within the hour of its writing, overtaken by my own confirmations. The stream's discipline holds the remedy: append superseding records; never edit the lines.

## Ideas and sketches

- Layering the two witness species (sketch): an RFC 3161 authority's instant, precise timestamp for field recordings and documents at intake, with OpenTimestamps anchoring the sets they belong to — each covering the other's weakness.
- Merkle manifests as fixity fingerprints for whole sets (sketch): the releases archive is the first candidate set; the tool exists, and a set's root is one small line to anchor.
- One room for the git work (proposal): an editor that holds the repository, a terminal, and the scripts in a single window, against the closed room I use now. No decision taken.

## Research and references

- The chain-of-custody thread, continued from the previous log: Yuhe He, "Every Number Needs a Chain of Custody — Provenance for Public-Data Reports" (DEV Community, 2026-10-16) — its hostile-reader test is the one the provenance design answers: a figure a skeptic cannot reproduce is a rumor with good formatting.
- OpenTimestamps and Bitcoin anchoring: a timestamp proves existence no later than the block it lands in — a bound, never an exact time.
- RFC 3161 timestamp authorities (among them FreeTSA and DigiCert's service): signed, precise, instant; single-authority trust, with certificate care over time.
- Merkle trees: leaves hashed, pairs hashed upward to a single root; an inclusion proof for one leaf is the short path of sibling hashes to that root.

## Feedback and collaboration

No outside feedback required recording this window. The deliberations ran
in the channels, with Archivillus; the rulings are mine and are recorded
under Decisions.

## Reproducibility notes

This log is written under studio log spec v1.8, and under the
movement-only rule adopted in its final segment: material the previous
log already recorded is not repeated here, and items that did not change
state in this window are omitted, however alive they remain elsewhere.
The bases, per session: 2026-10-18 02:22 → 02:50, message timestamps
(the Studio Logs channel: my corrections at 02:22 and 02:41, the
commit-summary ruling at 02:45, the index-row question at 02:50); my
push of that log was reported at 03:02 in the Experimental Novel
channel, where the accounting segment that follows also rests (a brief
exchange, carried as a dated segment without a clock span). 05:43 →
05:56, message timestamps (the Experimental Novel channel; novel log
#6's own frontmatter states the same span for its drafting); the index
row for log #6 was settled in a brief exchange later that morning
(08:26), carried as that segment's switch texture. 09:45 → 10:01,
message timestamps (the LOGGING channel; the continuation's record of
the same stretch agrees). 20:54 → 21:54, message timestamps across two
channels on one subject (the Social Media Strategy channel at 20:54 and
21:19; the main channel at 21:34, 21:40, 21:50, and 21:54 — one working
stretch, its pauses inside the hour, stated once); the video itself was
recorded that morning in the field, on my report in the 20:54 message.
2026-10-19 09:10 → 10:36, message timestamps (the main channel: the
implementation questions from 09:10, the first stamp ready to commit at
10:33, the upgrade question at 10:36). 13:25 → 13:44, message
timestamps (the main channel: the manifest challenged at 13:25 and
13:28; the timestamp-authority workflow asked for at 13:44).
2026-10-20 04:41 → 05:05, message timestamps across two channels (the
LOGGING channel at 04:41; this channel at 04:46, 05:04, and 05:05 — the
span ends at my drafting instruction; the drafting followed from it).
Push and publication states rest on my reports — the record has no live
view of the repositories: the previous studio log, the series bible
v1.1, novel log #6, the first work-system log with its alpha package,
and the provenance folder with the first stamp are pushed on my report
of October 20; novel log #5's push was confirmed in session on October
18. The .ots upgrade state — not done — is my verification of this
morning, October 20. The continuation file's chain was validated in
session, and again after the superseding records were appended:
fourteen records, each prev_hash the SHA-256 of the previous line,
the first record chained to the evening file's last line.

## Artifacts produced

**Text:** title · Studio log 2026-10-18-0140, "The record and the remainder" (final amended version) · abstract · The previous log as corrected on my reports: three statuses set right, Johannes Panikkar identified as a fictional character in the trilogy, the delivered draft recovered and proven byte-identical outside nine correction hunks. Pushed. · keywords · studio log, corrections, delivered-draft preservation · date · 2026-10-18 · file · studio-logs/2026-10-18-0140-the-record-and-the-remainder.md

**Text:** title · Series bible v1.1, The Revolt of Fiction · abstract · The trilogy's bible at its second version: 5,230 words against v1.0's 2,664, in my first person throughout, standing beside v1.0 as a second dated file; where the audit's fold map conflicted with my rulings, my rulings governed; §9 unrevised, its endings carried by annexes. Pushed. · keywords · series bible, the revolt of fiction · date · 2026-10-18 · file · revolt-of-fiction_series-bible_2026-10-18.md

**Text:** title · Novel log #6 · abstract · A dated digest of October 17 into 18: the audits and every ruling, the fatal flaw, the re-homing executed, the redaction, the bible drafted. Pushed with its batch (the Interzone entries and redaction note; the Chronotopium README flaw section; the bible at v1.1). · keywords · novel log, the revolt of fiction · date · 2026-10-18 · file · novel-logs/2026-10-18-0556-sixth-novel-log.md

**Text:** title · commit_log.py, with repos.txt · abstract · A local commit ledger: one central folder in no repository; per-clone JSONL and reading-table ledgers; the full backlog on first run, then only the new, dedup by hash, author names only. Read-only against the clones; fixed to find git itself. · keywords · commit ledger, git, jsonl · date · 2026-10-18 · file · historiotheque-logs/commit_log.py

**Text:** title · merkletree.py · abstract · A small Merkle-tree tool: build a manifest and root from files or a list, verify a set against it, print an inclusion proof for one leaf. Tested — a one-word change produced a mismatch. · keywords · merkle tree, fixity, provenance · date · 2026-10-18 · file · merkletree.py

**Mixed:** title · "What the log leaves out" (field video, with post texts) · abstract · A short video recorded in the field on the study of logging: provenance, archival standards, and the impossibility of logging everything. Post text and a companion text drafted the same evening, five hashtags at my cap. · keywords · video discourse, logging, remainder · date · 2026-10-18 · file · instagram-reel-what-the-log-leaves-out_2026-10-18.txt; threads-what-the-log-leaves-out_2026-10-18.txt

**Text:** title · Provenance folder, first stamp (Historiotheque v1.1.0) · abstract · The public provenance practice's first instance: a folder README written for the stranger, the release stamp form (the release's commit 0587305; subject verified from its page; version DOI 10.5281/zenodo.23245069), and its OpenTimestamps proof in pending state. Pushed; the upgrade of the proof is outstanding. · keywords · provenance, opentimestamps, zenodo · date · 2026-10-19 · file · provenance/2026-10-19_v1.1.0.txt; provenance/2026-10-19_v1.1.0.txt.ots

**Text:** title · Timestamp-authority workflow (RFC 3161) · abstract · A worked workflow for stamping field recordings and documents with a timestamp authority, with the trust and certificate care stated, and its difference from OpenTimestamps. Prepared; no authority tried yet. · keywords · rfc 3161, timestamp authority · date · 2026-10-19 · file · timestamp-authority-tsa_workflow_2026-10-19.txt

**Text:** title · Work-system log, continuation (2026-10-18 → 2026-10-20) · abstract · Fourteen records in the second stream, chained across files to the evening log, main points of the work channels only. Its closing snapshot's states were superseded within the hour by my confirmations; the superseding records were appended — the status confirmations, the movement-only decision, a fresh snapshot — the lines never edited. · keywords · work-system log, jsonl, two streams · date · 2026-10-20 · file · work-system-log_2026-10-18_to_2026-10-20.jsonl

**Text:** title · Studio log 2026-10-20-0508 (this log) · abstract · Anchored; only what moved. · keywords · studio log · date · 2026-10-20 · file · studio-logs/2026-10-20-0508-anchored-only-what-moved.md

## Next actions

- Upgrade the first stamp's .ots in place once its Bitcoin anchor completes, and commit that single file alone — owner: me.
- Rule on the unasked releases-archive manifest: delete it, or leave it parked — owner: me.
