# Procedural Study Format

**Version 1.0.0 — 2026-10-08**
Alex Gagnon (A.G.)
The Historiotheque · New Documentation · Specs

---

## Purpose

A procedural study is the worked example of *Procedural Theory*: one generator, stated completely in the theory's plaintext notation, so that a reader can audit it and a programmer can implement it. Studies are numbered gaplessly in order of writing (Study 1, Study 2, ...) and kept in the New Documentation folder beside *Procedural Theory*, until the procedural arm is promoted to a repository of its own.

## Status — declared, never implied

Every study carries exactly one status, stated in its header:

- **Live** — the chain as executed, recorded at the time. Parameters are as run.
- **Prospective** — a chain designed in advance of execution.
- **Reconstructed** — a generator that could produce a work of the kind studied, derived after the fact from the finished work. A reconstruction is not the original process, and says so, with its sources named (normally: the finished work itself, with its dimensions).

## The format

Five blocks, in this order. Nothing else is required; nothing required may be omitted. A block that does not apply is written as an explicit statement — never silently dropped.

**1. Header.**
```
STUDY <n> — <name>
STATUS      <Live | Prospective | Reconstructed>, <date>.
            <For Reconstructed: sources.>
SIGNATURE   <function_name>( x, y, <parameters> )
```

**2. CHAIN.** The generator as a chain of named stages, one stage per line, using := (is defined as). Rules:
- Plaintext notation only: F( p ), f( p + H( p ) ), n( x, y ).
- Amplitudes and thresholds are always explicit numbers. No unnamed constants.
- Offsets are named ( o1, o2, ... ) and their roles stated.
- A stage that does not occur is a finding, and is stated in NOTES (for example: "No WARP stage: the geometry stays rectilinear").

**3. CKPT.** The checkpoint tail, two lines:
```
SEED    family: <distribution / hash / field family>;
        exact: <recorded | withheld | unknown>
SELECT  <KEEP | BRANCH | PARK | RE-ENTER | STOP> —
        <the criterion, in one line>
```
For a Reconstructed study, SELECT states honestly what survives (normally: the finished work is the surviving selection) and reconstructs no selection event. SEED exact is `unknown` for reconstructions — a reconstruction claims a family, never a seed.

**4. PALETTE.** For image studies: the colours, as sampled or specified values, each labelled *sampled* or *specified*; plus any measured summary statistics of the source work (dimensions, mean saturation, mean value), labelled *measured*. For sound or text studies, the equivalent block is named for its material (REGISTER / LEXICON) and follows the same labelling rule.

**5. NOTES.** What the generator does not do: stages absent, post-steps not generated (for example, an artist's seal or signature), known divergences from the source work, and the divergences' size where it can be stated.

## Parameters

Every parameter in the SIGNATURE is glossed in one line, in the block where it is first used or in NOTES: what it controls, and what changes when it moves. A new seed, by itself, should produce a sibling of the studied work — same family, different individual — and the study should make clear which parameters hold the family and which hold the individual.

## Worked example (abridged)

```
STUDY 5 — Historiometric Noise
STATUS      RECONSTRUCTED, 2026-10-07. Source: the finished
            painting, 1024 x 1024.
SIGNATURE   historiometric_noise( x, y, seed, block_scale,
              speckle_density, outline_count )

CHAIN
  m     := n_low( p )
  A     := partition( p; cell = canvas/6 )
  B     := partition( p + o; cell = canvas/12 )
  base  := palette_pick( hash( A ), hash( B ), m )
  g1    := base * ( 0.85 + 0.3 * n_high( p ) )
  mask  := cluster( r( p ) > 0.997 )
  g2    := vivid( p ) where mask, else g1
  final := stamp( g2; outline squares, about 24 )

CKPT
  SEED    family: cell hash + speckle field; exact: unknown
  SELECT  the finished painting is the surviving selection

PALETTE (sampled; measured: saturation about 0.20, value about 0.40)
  slate grey-green (93, 102, 91); charcoal-green (62, 63, 58);
  grey-taupe (100, 86, 71); ochre-tan (116, 105, 78)

NOTES
  No WARP stage: displacement is by partition offset.
  The artist's seal is a post-step, not generated.
```
