# PATTERN-001: Fast-and-Frugal Decision Trees

**Context:** Any procedure the operator must perform more than once — releases, uploads, triage, publishing.

**Problem:** Methods list steps but don't say which steps apply when. Vague guidance costs the operator their place mid-procedure, and a procedure held in memory is a procedure that drifts. What is needed is selection logic, not more steps.

**Solution:** State every repeatable procedure as a yes/no decision tree, walked top-down:

1. Each node asks one yes/no question the operator can answer from what's in front of them.
2. Each branch leads to the next question or to a leaf.
3. Each leaf is exactly one action — do it, then stop or return to the root.
4. Decision nodes reference the relevant taxonomy (e.g., the Signal Types taxonomy at "does this need a response?").
5. No node may require holding the whole procedure in mind. The tree holds it; the operator walks it.

**Worked example:** The Signal Types taxonomy is this pattern in its purest form — *Is the message classifiable? → Does it require a response? → Is it urgent? → Is action required?* — each answer walking the operator to a leaf (file as notice, respond routinely, act within the frame, interrupt everything). The release-publish checklist is the same form applied to shipping.

**Related:** PATTERN-002 (classification is the tree's first node), PATTERN-004 (trees as through-bound cost controls), ANTIPATTERN-001 (procedures without trees rot in staging).
