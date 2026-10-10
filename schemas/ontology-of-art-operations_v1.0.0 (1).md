# Ontology of Art Operations

**Version:** 1.0.0 · **Date:** 2026-10-10

## 0. What this document is

A formal ontology of the domain of the Art Operation: the kinds of things that exist in the practice, the fields that describe each kind, and the relations between kinds. In information-science terms: concepts plus relations, not categories alone. This is discourse — scaffolding around the work, never the work.

## 1. Versioning

Semantic versioning, MAJOR.MINOR.PATCH, for this and all new documents going forward:

- **MAJOR** — changes that are not backward-compatible: a redefinition that breaks what earlier versions meant.
- **MINOR** — backward-compatible additions: new kinds, fields, or relations that extend without breaking.
- **PATCH** — clerical fixes: wording, typos, formatting; no change of meaning. ("Clerical" in his sense: polish, not forgery.)

Versions are assigned at publication, not during drafting. A working document is polished in place — words, sentences, and sections changed freely before it goes out — and the first published version is v1.0.0. There is no new version for every edit; the version history records published versions only.

Documents already versioned as v1.0 or similar keep their names. The audit trail is not rewritten.

## 2. Governing conventions

- **Terminology is law.** Only the artist's words name his concepts. New terms are proposed in conversation and enter the ontology only when he adopts them.
- **Faceted description.** A thing is described along several orthogonal axes at once (a Session carries session_type = the verb and workspace = the place, independently), not forced into one hierarchy.
- **List-valued fields.** Where a thing can honestly carry several values, the field takes a list.
- **Open, ratified vocabularies.** New values are proposed and adopted, never invented ad hoc.
- **No-backfill.** Old records stand under the version of their date. Corrections arrive as new versions or new records, never silent rewrites.
- **Reconstruction marking.** Anything reconstructed carries a line saying so, with date and sources.

## 3. Classes (kinds)

| Class | What it is |
|---|---|
| Operation | The maximal unit of the ontology: the artist's whole art-research practice, taken as a working system, identified simply as the Art Operation. It carries no era-name. |
| Branch | A major division of an Operation (The Experimental Novel; The Deep-Archives Project). |
| Project | A named, bounded body of work, possibly nested inside a Branch or another Project. |
| Series | A sequence of related Works (the Noise Field Paintings; the Chronotopium-Series). |
| Work | An individual artifact: a painting, a track, a text, a video. |
| Technique | How a Work is made: materials, tools, processes. |
| Procedure | An ordered set of steps the operator follows (a release procedure; an upload procedure). |
| Heuristic | A fast-and-frugal decision rule for the operator. A Checklist is a kind of Heuristic: a yes/no decision tree built for him to follow. |
| Refcard | An atom of knowledge, in the simplified library-card-catalog sense. |
| ReferenceMaterial (Refmat) | Source material the work draws on. |
| Concept | A named idea the practice works with. |
| Session | A unit of work, described by session_type (the verb) and workspace (the place). |
| Log | A dated record of Sessions and other events (studio logs, dream logs, design-concept logs). |
| Declaration | An official dated statement about the practice: production-year declarations, official releases, prospectives, retrospectives, antilogs. |
| Release | A versioned publication of Works or systems, carrying semantic versions. |
| Schema | A formal description of a category: the fields every instance carries. |
| Taxonomy | A controlled vocabulary of categories, usually hierarchical. |
| Ontology | A formal specification of the kinds in a domain and the relations between them. This document's own kind. |

## 4. Relations

- **nested-in / has-part** — Branch → Operation; Project → Branch or Project; Series → Project; Work → Series.
- **uses** — Work → Technique.
- **follows** — Session → Procedure; Session → Heuristic.
- **records** — Log → Session.
- **declares** — Declaration → Operation, Project, or Release (a declaration is about something).
- **publishes** — Release → Work (or set of Works).
- **draws-on** — Work or Project → ReferenceMaterial; Work → Concept.
- **described-by** — any instance → Schema.
- **supersedes** — a new version supersedes the old; the old stands.

## 5. Minimal fields every instance carries

identifier, title, version, date (and time where order within a day matters), status, relations (the links above), notes.

## 6. Version history

- 1.0.0 (2026-10-10) — First published version.
