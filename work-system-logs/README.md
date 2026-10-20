# Work-system logs

The machine-readable logs of my work-system: one JSON record per
atomic unit of work, append-only, under the Work-System Log Spec
(alpha spec: `new-documentation/specs/work-system-log-spec_v0.1.0-alpha_2026-10-18.md`;
its schema file: `schemas/work-system-log_schema_v0.1.0-alpha_2026-10-18.json`).

These are official records, not experiments. The studio logs and the
novel logs remain their own prose stream; this stream is separate
and complementary, interlocked with them by timestamps, shared
vocabularies and citable record ids — neither stream is a rendering
of the other, and neither revises the other. The prose stream lives
in the sibling folder `studio-logs/`; the two folders point at each
other, and each stream cites the other by timestamp and record id.

Records are never edited. A correction is a new record that
supersedes an earlier one.

First official log: `work-system-log_2026-10-17_evening.jsonl`
(9 records, 2026-10-17 evening; hash chain verified at adoption).

Second log: `work-system-log_2026-10-18_to_2026-10-20.jsonl`
(14 records, 2026-10-18 → 2026-10-20; its first record chained to the
evening log's last line, the chain verified unbroken across both
files. It closes with appended superseding records — the status
confirmations, the movement-only decision, and a fresh snapshot.)
