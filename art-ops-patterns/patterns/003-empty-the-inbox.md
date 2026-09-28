# PATTERN-003: Empty the Inbox

**Context:** Every staging area, incoming folder, and backlog in the operation.

**Problem:** Intake without outflow is a tar pit. New artifacts arrive, get roughly treated, and settle — and the staging area becomes a second archive nobody trusts. The operation then carries two of everything: the archive and the pile.

**Solution:** Staging is for intake only, and intake is a pipeline with an end:

1. **Take in** — the artifact enters staging, dated.
2. **Treat** — clean it, convert it, make it legible.
3. **Classify** — file it under the operation's taxonomies.
4. **Document** — log what was done, in the log the spec requires.
5. **Archive** — move it to its permanent home.
6. **Close** — remove it from staging. Version control is the Done column: the commit is the trace that it was finished.

Run emptying passes on a rhythm — a little at a time, continuously — rather than waiting for a grand cleanup that never comes. Nothing sits in staging forever. That is the whole rule.

**Worked example:** The interzone file: entries drained one by one into their destination repos, each move committed, the file shrinking instead of growing.

**Related:** ANTIPATTERN-001, PATTERN-001.
