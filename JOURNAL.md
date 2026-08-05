## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/36
**Issue title:** Architecture doc doesn't explain the hybrid retrieval scoring formula
**Tier:** [x] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
The current project documentation fails to explain the mathematical logic behind how search results are ranked. Specifically, `docs/ARCHITECTURE.md` states that the system blends vector and keyword scores, but it lacks the exact scoring formulas, normalization steps, and default configuration parameters used by the engine. A successful fix requires reviewing `rag/retriever/hybrid.py` to extract the precise linear combination math and updating the architecture guide with clear equations and an illustrative example so other developers can understand how search queries are processed.

**Branch name:** docs/36-hybrid-retrieval-scoring
**Setup confirmation:** [x] App runs locally at localhost:5173
**Cohort ledger:** [x] Issue added to cohort ledger

## Week 8 — Reproduction & solution planning

**Reproduction commit link:** https://github.com/jal35/pathreview/commit/f559fe3
**Reproduction summary:**
I verified the gap by opening `docs/ARCHITECTURE.md` and finding that the hybrid retrieval system sections completely lacked the specific algebraic scoring formulas and parameter limits used by the active backend engine.

**PLAN.md link:** https://github.com/jal35/pathreview/blob/docs/36-hybrid-retrieval-scoring/PLAN.md
**Walkthrough video (recommended):** **Blockers or open questions:** None. The core formulas have been successfully verified and documented.

## Week 9 — Solution building & PR submission

### Check-in 1 (mid-week)
**Current progress:**
I have fully implemented the missing hybrid scoring formulas, parameter rules, and an edge-case example inside `docs/ARCHITECTURE.md`. 
**Next steps:**
Open the Pull Request and complete final journal logs.
**Blockers:** None.

---

### Check-in 2 (end of week)
**PR link:** https://github.com/ascherj/pathreview/pull/878
**Branch:** `docs/36-hybrid-retrieval-scoring`
**What you built:**
Added detailed documentation for the hybrid retrieval engine scoring formulas, explaining min-max score normalization, linear weight combination rules ($0.7$ vector / $0.3$ keyword), and modal miss handling.
**Tests added or updated:**
None required (Documentation issue).
**Self-review confirmation:** [x] make check passes  [x] make test-unit passes
**Draft PR feedback received from:** none