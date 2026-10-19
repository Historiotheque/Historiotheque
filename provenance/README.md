# Provenance

This folder holds timestamp proofs for this repository — for its releases, and for individual commits that mark something worth anchoring.

Each proof is a pair of files:

- **a stamp file** (`.txt`): a plain-text record naming a release tag or a commit by its full hash, with the details needed to find it again.
- **its proof** (`.ots`): a small binary file made with OpenTimestamps.

The commit hash written in a stamp file covers the entire state of the repository at that commit, because a commit's hash is computed over the whole tree. One proof therefore anchors the repository exactly as it stood at that release or at that commit — not only the files that a single commit happened to change.

## What a proof shows

The `.ots` file proves that the stamp file — and with it the commit hash recorded inside — existed **no later than** the date of the Bitcoin block in which its hash is anchored. The verification needs no one's permission and no trust in the author: the hash chain in the proof leads up to a block in a public ledger that no single party can rewrite.

Two honest limits:

- The proof bounds existence; it does not certify the exact hour anything was made. The dates inside git's own record remain the author's, as with any log.
- A proof says nothing about whether a text is true. It says the text existed, in exactly this form, by that date — and that any later alteration would show.

## Checking a proof

With the OpenTimestamps client installed (`pip install opentimestamps-client`), stand in this folder and run:

`ots verify 2026-10-19_v1.1.0.txt.ots`

It checks the proof against the stamp file beside it and reports the Bitcoin block and its date. `ots info` on the same file shows the chain inside the proof. A web verifier is also available at opentimestamps.org.

## Naming

- Release stamps: `YYYY-MM-DD_vX.Y.Z.txt` — the date stamped, then the tag.
- Commit stamps: `YYYY-MM-DD_<short hash>.txt` — one notable commit per file, its full hash inside.
- A stamp file may instead list several commits from one period, stamped when the period closes; the single proof then anchors the list as a whole.

A proof begins life "pending": its anchor in a Bitcoin block completes a few hours after stamping. The proof file is then updated in place, under the same name, in a later commit — so each `.ots` here is the completed, self-contained version, checkable offline against the public chain.
