# Procedural Theory

**Version 1.0.0 — 2026-10-08**
Alex Gagnon (A.G.)
The Historiotheque · New Documentation

---

## Introduction

Procedural Theory is the theory of a method: making by designed operations, applied in chains, to surfaces — and of everything that follows from working that way for a long time.

The method is older than the computers it now runs on. It was practised iteratively in musical composition, at the guitar and the piano, and collectively in bands, where each player acts on the others' material. It was practised in painting from the late 1990s: not painting in a linear manner, but applying *treatments* to a surface — a thin layer, then another treatment — most formally in The History-Project (begun 2001), whose aim was to paint the concept(s) of History, and whose Process-Painting Manifesto (2004) stated the method directly. It was formalized as workflow in training in computer-assisted sound design: parameters, envelopes, saved sounds accumulating as populations, samplers re-entering recorded material into new work. It then migrated, unchanged in shape, to code and to digital images at the same time.

It is therefore not only design. It is an early form of *development*: chains are built, tested, versioned, branched, merged, released, and archived — the life-cycle later recognized in software development, and the root of what this operation calls Cultural Software.

The theory is a design science. Theory comes first and specifies the problem; a design concept is proposed as a solution; the solution is executed as a chain of operations; the resulting work judges the theory back. The end-goal of the formalization is not the formalization. It is infrastructure: a History-Machine — a machine for sampling, storing, compressing, processing, selecting, error-correcting, and transmitting, of which the Historiotheque is a small-scale instance.

Notation throughout is plaintext. A function is written F( x ). A point is p = ( x, y ). A change of workspace configuration is written dW.

## Primitives

Terms pointed at, not defined; the principles fix their meaning by use.

- **Surface (state), S** — anything that can receive an operation: a canvas, an image field, a sound signal, a text, a body of code, a workspace.
- **Operation, F** — a designed concept made operable: F( S ) is the surface after F acts on it. In painting an operation is a treatment; in code, a function; before either, a design concept. These are one thing at three levels: imagined, made operable, applied.
- **Parameters, k** — the settings of an operation, F( S, k ): colour, opacity, amplitude, scale, threshold.
- **Noise source, R** — a draw from a distribution: a family, and optionally a seed.
- **Population, P** — a set of states alive at once: a series.
- **Selection, Sel** — judgment applied to a population by the Witness (below).
- **Chain** — operations composed in order (section 1).
- **Checkpoint** — a saved state plus the record of the decision taken at it.
- **Seed** — a saved state, or a parameter set, from which a new chain starts.

## Principles

**P1 — Operation.** All making, in this method, is operations on surfaces. There is no unmediated mark: every mark is the output of some F, designed or undesigned.

**P2 — Chain.** Operations act in chains, and order is constitutive: F( G( S ) ) is not in general G( F( S ) ). The sequence is information, which is why the sequence is what the record keeps.

**P3 — Selection.** A chain that only generates is incomplete. Generation proposes; the Witness disposes. No population becomes a lineage without a selection event.

**P4 — Witness.** The selecting observer — the Witness — is a model built from witnessed change: WIT = M( dW ), read in section 5. Selection at every scale is that model, acting.

**P5 — Transmission.** What is handed on is never the works alone. It is works, a record of deltas, and error correction sufficient for a later Witness to rebuild a model close to the sender's. A generation of culture is one application of the History-Function (section 5).

**P6 — Phases.** Activity in a procedural operation is phased: it ramps, peaks, collapses, and decays (section 6). Collapse under excessive complexity is a law of the method, at two loci, not an accident that befalls it.

## 1. The chain

A chain is composition:

S1 = F1( S0 )
S2 = F2( S1 )
Sn = Fn( ... F2( F1( S0 ) ) ... )

Three properties govern everything built on chains.

*Non-commutativity.* Order matters (P2). Treatment B over treatment A is a different surface from A over B.

*Irreversibility.* Most operations have no inverse. Flattening, merging, adding noise: no operation recovers S0 from S1. A chain runs one way; this is the mathematical root of the operation's rule that records are never rewritten — some steps cannot, in principle, be walked back.

*Higher order.* A function may take a function as input. The canonical case is domain warping. Instead of evaluating F at p, evaluate it at a displaced point:

W( F, H )( p ) = F( p + H( p ) )

where H( p ) is a displacement computed by another function. Chains of warps — a warp field built from a field already warped — produce the turbulent, folded structures characteristic of noise field work. A design concept is often exactly this: not an operation, but a way of combining operations.

*Parameters and noise injection.* An operation with parameters, F( S, k ), can be varied by drawing noise into its parameter space:

k_new = k + e

where e is a draw from R. Small draws give variations inside a family; large draws found new branches. A checkpoint fixes a k in the record, which is what makes injection a designed act rather than drift.

## 2. Aura, sillage, patina

A translucent treatment blends instead of replacing:

S_new = a * T + ( 1 - a ) * S_old, with a between 0 and 1.

Expanded over a chain, the final surface is a weighted sum of every treatment in its history. Each earlier treatment carries a weight: the product of the ( 1 - a ) factors applied after it. The weights shrink but are not zero — unless some layer is fully opaque ( a = 1 ), which sets the weight of everything before it to exactly 0 and erases that lineage.

The non-zero weight of past states in the present state is the phenomenon this theory tracks under three names at three timescales: **aura**, the presence of earlier layers in a single surface; **sillage**, the wake a state leaves as a process moves — the phenomenology of that persistence; **patina**, the same accumulation written by time over years: wear, damage, decay — the marks of history on objects. Patina is a chain whose operations were not designed: the world applies its own functions, and the weights accumulate anyway. A theory of patina — including digital patina, the usage history and ageing of files and images — is a standing part of this research programme.

## 3. Populations, generations, thresholds

Work in this method is done on populations, not singletons — a practice constant from painting series worked a dozen at a time to digital series accumulating variants. One evolutionary step:

P_next = Sel( vary( P ) + cross( P ) + re-enter( archive ) )

*vary* applies operations with altered parameters, noise injection included. *cross* builds a state from two or more parents — layers copied across variants, merged, flattened — so descent is a network, not a tree, and "jumbled" is a legitimate recorded ancestry where flattening has merged the lines. *re-enter* returns parked states from the archive to the living population: parking is dormancy, not deletion. Variants evolve unevenly; selection operates continuously, in where operations are spent, and decisively, at the end of a series.

In digital image work, states accumulate **Visual Interestingness (V.I.)** as operations add colour and structure. Each variant can pass a threshold individually; a series ends at a key point, when V.I. in the population is at its highest and Sel acts: the chosen few each found a new series (branching), or are re-combined (merging). In the analog painting practice the same boundary appeared as the loop-back, the population's output becoming the next population's material. The constant across media: a generation is a population, and its boundary is a selection event.

Selection is a chain-level requirement (P3). What Sel computes, in the one case studied formally, is the next section's subject.

## 4. Interestingness, beauty, compression

Following Schmidhuber: let M be an observer with an encoding of what it sees, and let L( S, M ) be the description length of a work S under that encoding — how much M needs to state S, having found its regularities.

Beauty( S, M ) = - L( S, M )

Interestingness is the first derivative of beauty — the observer's compression progress as it learns from S:

I( S ) = L( S, M_before ) - L( S, M_after )

Pure noise does not compress and does not improve: I = 0. A trivial field is already fully compressed: I = 0. Between them sit states that arrive partly unpredictable and become describable — structure emerging — and those are the interesting ones. V.I. rising during a modulation phase is this derivative, watched by eye: operations buying new compressibility, step after step, until the saving per step falls toward zero at a high level — the key point of section 3, where selection belongs.

A computational selection function is therefore specifiable in outline: an observer M fitted to the operator's archive and past selections; a description at the levels actually judged (palette, distributions, scales present, novelty against the archive); two thresholds — eligibility for a variant, harvest for a series; and M updated after every generation, since the observer learns. Whether such a model can predict the operator's selections well enough to run Sel is an open, testable question, and is recorded here as a research direction, not a result. The fuller treatment — what in a practice is reproducible, what is auditable, and what is not disclosed — is given in *A Note on Reproducibility (of Experiments)*, in this folder.

## 5. The Witness and the History-Function

The observer of section 4 has, in this operation, a name and a task. The observer is the **Witness**, and its model is built from the changes it has witnessed — the workspace's delta history:

M = Compress( dW( 1 ), dW( 2 ), ... , dW( t ) )
WIT = M( dW )

Taste is compressed witnessed history, acting. The operation is then a closed loop:

Sel applies M to a population; the approved operations execute and produce the next dW; M updates on that dW. Every delta is both an output of the operation and the next input to the Witness.

Two axioms govern the Witness in this theory:

**W1 — No unwitnessed operation.** Every dW updates M, whether or not it is recorded. An unrecorded delta still changes the Witness; it simply cannot be transmitted, because what was not recorded cannot be handed on.

**W2 — Transmission rebuilds the Witness.** A receiver who rebuilds a model from a transmitted record — M_receiver = Compress( record of dW ) — holds a Witness close to the sender's only as far as the record is faithful. An error in the record does not merely garble a fact; it rebuilds a slightly wrong Witness downstream.

At the largest scale the same structure is the transmission of the Cultural Treasure — here, the Treasure. Let T be the Treasure held by one generation. The History-Function is:

H( T ) = ECC( Sel_M( T ) )

where Sel_M selects by the true, the beautiful, and the good, and ECC is error correction — the redundancy, records, versions, and audit trails that defend the transmission against generation loss, transcription errors, accounting errors, and the rest. Culture's trajectory is H applied repeatedly: T_next = H( T_now ). The Art Operation, and Cultural Software generally, are implementations of H at working scale.

The History-Function is not new in this document. It was the object of study of the History-Paintings from 2001: the paintings were formal studies of H, with its anatomy made visible — Axes as the coordinate frame H acts on, Templates as the elements it takes as input, Conduits as the traces of its mappings. The H( x )-functions were designed in paint two decades before the notation existed to write them in.

A boundary, honestly marked: the model M( dW ) describes the operational Witness — the one that selects and transmits. Whether the true Witness is exhausted by the algorithmic and the mathematical is not claimed here. The soul is continuous; the procedural is discrete; and what the soul witnesses, it witnesses whole — the next section's subject.

## 6. Scale, complexity, phases

Name the small operations with lowercase letters — f, g — and reserve uppercase for their compositions. Let cost( f ) stand for something akin to the computational complexity of a lowercase operation: what it takes to execute and to hold. A chain's load is approximately the sum of its costs plus an interaction term, its operations being interrelated rather than independent. Scale an operation up and the load rises toward a capacity K. Then the collapse law, one law at two loci:

load above K in the workspace: workspace collapse
load above K in the operator: cognitive collapse

Activity A( t ) over a working cycle takes two named phases:

**PROD** — production: A ramps up slowly toward a peak, gains coming harder as the peak nears; then climax, at or near capacity.
**SLEEP** — after collapse, exponential decay:

A( t ) = A_peak * ( 1/2 )^( time since climax / h )

with h the half-life of the decay. The duration of SLEEP is not a parameter the operator sets; the cycle restarts when it restarts. What persists through every collapse is the simplest core of the operation, from which complexity regrows — the cycle is a rhythm, not a decline.

## 7. Sampling, reconstruction, graceful degradation

History itself is the discretization, in infinitesimal steps relative to the scale of History, of a fundamental and global continuum. Everything has a history; every process has a start_time and an end_time. Divide a process's interval into steps of size dt:

change_total = d( 1 ) + d( 2 ) + ... + d( N ), with N = ( end_time - start_time ) / dt

As dt shrinks, the sum carries the continuum it samples. The discretization is nested: a step at one scale contains continuities at smaller scales — a single dW holds a stretch of continuous life inside it, and a life is a single step at the scale of History.

A record is such a sampling. Reconstruction rebuilds an approximation of the signal from its samples and its record:

x_hat( t ) = rebuilt from the samples, the record, and error correction
error( t ) = x( t ) - x_hat( t )

Sampling too sparsely loses whole movements between checkpoints. Errors matter: transcription errors, accounting errors, missed steps. But degradation comes in two kinds. It is **catastrophic** when the core is lost early — a cliff. It is **graceful** when fidelity falls in the right order — fine detail first, the compressible core last — so that the pattern survives its own wearing. Patina, again, is graceful degradation made visible over time: history arrives degraded, always, and the operative question is never whether loss, but whether the loss is graceful. Error correction exists to push every transmission under the operation's control toward the graceful side.

## 8. The History-Machine

The end-goal of this formalization is a machine: the History-Machine, of which the Historiotheque is a small-scale instance — the large-scale instance being the institutional machinery, libraries, archives, museums, and states, that writes and preserves History. Its subsystems, in the vocabulary of this document:

- **Sampler** — logs, checkpoints, snapshots: processes recorded with start_time, end_time, and their deltas.
- **Store** — the archive: the sedimented sum of deltas, in strata.
- **Compressor** — schemas, notation, theory: the Witness model, made explicit and rebuildable.
- **Processor** — the chains: treatments, functions, and their implementations in code.
- **Selector** — Sel, judging by V.I. in the small and by the true, the beautiful, and the good in the large.
- **Error correction** — versions, audit trails, marked reconstruction.
- **Transmitter** — releases and publication: the Treasure handed to the next scale.
- **Clock** — the PROD / SLEEP cycle, with collapse and restart, the machine's own process — which also has a start_time, and will have an end_time, and is therefore a history inside the larger one.

Worked examples of the Processor are kept as **procedural studies**, each in the canonical format specified in the *Procedural Study Format* (specs/). Reconstructions among them are marked as reconstructions, with their sources — the record distinguishes what was witnessed from what was rebuilt, or it is not a record.

## On the horizon

- A catalogue of designed H( x )-functions, recovered from the History-Paintings and stated in this notation.
- The computational Sel of section 4, specified in full and tested against the archive.
- Translations of the canonical functions into the equation systems of image software, so the same studies can be executed there.
