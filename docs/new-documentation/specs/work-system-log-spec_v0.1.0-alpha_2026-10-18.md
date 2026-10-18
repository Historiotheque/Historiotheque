# Work-System Log Spec

Version 0.1.0-alpha · 2026-10-18
Status: alpha — adopted for the first official log. The machine-readable
schema is `work-system-log_schema_v0.1.0-alpha_2026-10-18.json`, in
the schemas folder (`../../schemas/` from here). The proposal of 2026-10-17 stands as the dated record of
how this spec was reached.

## 1. What this is

My work runs as one work-system across many projects, workspaces and
media. The studio logs and the novel logs record that work in prose.
The work-system log records it as data: one JSON object per line
(NDJSON / JSONL), one record per atomic unit of work, append-only.

The two streams are separate and complementary. Neither is the source
of the other, and neither is a rendering of the other. The same event
is lived once and recorded twice — in prose, in the .md logs, for
reading; as records, here, for querying, chaining and merging. They
interlock by timestamps, by shared vocabularies, by citable record
ids, and by the same qualitative content.

The record is not the experience. Numbers, where they appear at all,
live in the optional derived block, are labelled derived, and support
a reading; they never replace it.

## 2. Format

- NDJSON / JSONL: one JSON object per line, no pretty-printing, no
  literal newlines inside a record.
- Append-only: a line is never edited. A correction is a new record
  with event=correction that supersedes an earlier id. This is the
  no-backfill doctrine in machine form.
- A file is a session file: the records of one working stretch or one
  period, named `work-system-log_YYYY-MM-DD_<period>.jsonl`.

## 3. The record

Required envelope, on every record:

- `v` — schema version of the record (1 in alpha)
- `id` — unique record id, never reused. Alpha form: dated and
  human-readable, e.g. `2026-10-17E-01`, sortable within its file
- `seq` — integer, position in this file only, strictly increasing
- `ts` — when the event happened, ISO 8601 with local offset; may be
  null only when a `time` block states the honest precision
- `recorded_at` — when the record was written; differs from `ts` for
  off-computer work recorded later
- `tz` — America/Toronto
- `event` — event type, from the dictionary (§4)
- `actor` — operator | archivillus | system: who performed the act,
  not who narrated the record
- `session_id` — the working stretch this belongs to; a pause of
  about 60 minutes on the same subject does not split a session
- `shard` — the origin of the record (a repo, a workspace, a channel)

Optional blocks, as the event needs them: `span` (with `time_basis`
required whenever a span is stated — the time-honesty rule), `time`
(the honest precision when `ts` is null), `context` (workspace,
session_type, project, stream — the existing vocabularies of the
studio logs, carried over), `delta` (what is new, moved, gone, in one
first-person line), `aesthetic` (the problem, its tension, its
solution and why the solution is elegant; problems carry stable ids
so a solution months later links back), `temperature_vector` (a
qualitative reading per workspace or project — a vector, never a
scalar), `snapshot` (the state of the whole surface at departure),
`links` (§5), `provenance` (sources, commit, `prev_hash`),
`properties` (an event-specific bag; variability here is normal).

## 4. Dictionaries

Definitions live in separate versioned dictionary files; records stay
compact. A dictionary is itself append-only: a term is added by a
record, superseded by a later record, never edited.

Event types, alpha: session_started, session_continued, session_ended,
switch, work_act, reading, listening, deliberation, decision,
audit_completed, aesthetic_problem_opened, elegant_solution,
refcard_created, refcard_moved, file_created, publishing,
commit_linked, snapshot, correction, encounter, rest.

Session types and workspaces: the controlled vocabularies of the
studio logs, carried over unchanged. Qualia: the adjectives of the
Delta-W temperature readings, defined in my work terms in their own
dictionary as they are adopted.

## 5. Interoperation with the .md logs

- The `links` block is the joint. A record names the Interzone
  entries it rests on by timestamp, and the studio log or novel log
  it belongs with by file — or null, with the relation named, while
  that log is unwritten.
- A studio log or novel log may cite record ids from this stream in
  its own text or reproducibility notes.
- Neither stream revises the other. A disagreement is settled the
  way the prose record settles everything: a new dated entry, never
  a silent edit.

## 6. Integrity

Each record's provenance carries `prev_hash`: the sha256 of the
previous line exactly as written. The first record of a file carries
null. The chain makes the ledger tamper-evident; the git history is
the second chain. In alpha there is no per-record `record_hash` —
whether it returns is a beta decision. The chain of the first
official log was verified complete before this spec was adopted.

## 7. What alpha leaves open

- One shard file per repo or workspace, or session files merged at
  snapshot time. Alpha practice: session files, each record tagged
  with its shard.
- Whether `temperature_vector` appears per segment, per snapshot
  only, or both.
- The event-type list in my final words.
- Whether `record_hash` returns in beta.

The spec changes by version, never by editing this file's account of
what alpha was.
