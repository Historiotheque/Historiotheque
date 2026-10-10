# Formalization of the Work-System — Module 0: Foundations

**Version 1.0.0 — 2026-10-10**
Alex Gagnon (A.G.)
The Historiotheque · New Documentation

---

## Introduction

This module states the foundations of the Art Operation as an axiomatic system: the processes, practices, and methodologies of the Work-System, and their theoretical underpinnings, set out in plain language, without mathematical notation, auditable by anyone.

The system is evolutionary. It always has an axiomatic core — this module — and the core persists even as it changes: axioms may be revised, but only as events, and there is no state of the system without a core. Modules import one another the way programs import libraries: a term defined in one module is used, not redefined, in the others. The axioms are stated for art operations as a class — any operation of this kind, anyone's — and the Work-System of the Historiotheque is the instance at hand: the system its author devised, stated so that it generalizes.

## Imports

- **WT** — Workspace Theory: Axioms and Consequences, Version 1.0.0 (2026-10-04). Supplies workspace, configuration, delta, and record in their workspace sense; axioms WT.A1–A10; consequences WT.C1–C9.
- **LS** — Studio Log Specification, Version 1.7. Supplies the form of the log, and the measurement procedure by which sessions are derived from traces for the studio logs. (Used by Module 1.)
- **WS** — Historiotheque Work Schema. Supplies the vocabulary of works, projects, and reference materials.
- **SB** — The Switchboard Method, introduction. Supplies the practice of movement and switching, stated generally at WT.A8.

## Primitives

Terms pointed at, not defined. The axioms fix their meaning by use. Workspace, configuration, delta, and record are imported from WT and not restated here. Module 0 adds two.

- **Operator** — (imported, WT) whoever works in the workspace, from inside it; in this operation, the one Operator, who works and witnesses.
- **Work** — what the operation makes: a cultural artifact.
- **Session** — a bounded arc of work. (Refined in Module 1. LS is its measurement procedure for the studio logs — the derivation rules keep the logs tidy; they are not the definition of a session.)

**Derived, not primitive — Time.** Time is derived from the deltas: the order and the measure of time are read off the changes — in the workspace (WT.A4) and in the works themselves, which have their own deltas. Where nothing changes, no time passes in the system.

## The Core Axioms

**A0 — The core persists.** At every moment the system has an axiomatic core. The Operator may revise any axiom — including this one — but a revision is an event: versioned, entered in a changelog, never silent, never retroactive. There is no state of the system without a core. Through every collapse of the workspace the core persists, and the workspace regrows from it (WT.C7). *Audit: ask of any present state of the system which core it answers to; the answer always exists, and every change of core can be pointed to as a dated event.*

**A1 — Operators, inside.** An art operation is worked by its operator or operators from inside the workspace; the operators witness the work, and there is no outside position from which an operation is worked. (WT.A7.) This Work-System has exactly one Operator. *Audit: every act of work in the record traces to an operator working from within a configuration — in this instance, to the one Operator.*

**A2 — Works are cultural artifacts.** The operation makes works, and every work is a cultural artifact. The modes of expression are, at present, four: Images, Sounds, Texts, and Code. The list of modes is open — new modes may be added as the practice develops, by revision event (A0) — but no work falls outside every mode. *Audit: name a work; it stands in one of the named modes, or in several at once — never in none.*

**A3 — Situated work.** Every act of work occurs in a workspace, in a configuration, within a session. Nothing is made nowhere, and nothing is made at no time in the arc of a session. *Audit: take any work act from the record; its workspace, its configuration, and its session can each be named.*

**A4 — Stepwise change.** The operation changes only by deltas: consecutive configurations, each accessible from the one before, in a single step. No single step reconfigures the whole. Large changes are paths of small ones. (WT.A4.) *Audit: between any two configurations in the record, the chain of deltas can in principle be walked, step by step.*

**A5 — The record.** The operation records its work and its deltas, and the record is a working part of the system, kept inside it — not an account rendered afterward. An unrecorded delta is unrecoverable. The record grows; it is not rewritten. (WT.A9.) *Audit: remove the record, and the operation loses its past; check any entry — it stands as written, and corrections arrive as new entries, never as edits of the old.*

**A6 — Openness.** The operation is not closed. Its boundary is an envelope the Operator opens and closes, and materials, signals, energy, and finished work flow across it. A system whose envelope stays shut settles into equilibrium — collabrium — and the work dies. (WT.A10, WT.C6.) *Audit: trace one input from arrival to finished work; if nothing can be traced across the envelope, the system is closing.*

## A Definition

**D1 — Recorded work.** A work is *recorded* when the record registers it — as the output of a session, or as produced within one. Recorded is a status, not a kind of work: an unrecorded work is a work all the same (A2), only unrecoverable if it is lost (A5). The record defines no works; it defines which works the operation can still reach.

## A First Derivation

**T1 — Attribution.** Every work is attributable to the Operator, to a session, and to a configuration.
*Derivation:* by A3, the act that made the work occurred in a workspace, in a configuration, within a session; by A1, the maker is the one Operator. Nothing further is assumed. ∎

## What Module 0 Does Not Decide

Session boundaries and the form of the log (Module 1, importing LS); switching (the Switchboard module, importing SB); the essence of a series — the properties a series necessarily implies in every instantiation (the Production module); the modal layer — possible states of the operation against what the record holds across all snapshots (pending ruling).

## Application

This module is written from, and for, the Operator's own Art Operation @ The Historiotheque. It is stated generally, and is meant to be generalizable: extended and applied to other art operations, each instantiating the axioms in its own terms — its own operators, its own modes, its own record.


