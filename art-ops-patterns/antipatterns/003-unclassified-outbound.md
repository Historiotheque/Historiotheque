# ANTIPATTERN-003: Unclassified Outbound

**Context:** Outbound signals of every kind.

**Symptoms:** Messages that say nothing classifiable: no topic, no ask, no time frame — or an ask buried under processing-out-loud. The receiver must either mind-read or interrogate. Threads multiply: every unclassified signal spawns two clarifying signals.

**The failure:** Exporting classification labor onto the receiver. The limiting case is the identical copy-pasted message sent daily: pure carrier, zero payload, maximum tax — the sender paid one paste, the receiver pays attention every day.

**Remedy:** PATTERN-002 — classify before sending; state content, what's wanted, and time frame, in the signal itself.

**Related:** PATTERN-001, PATTERN-002.
