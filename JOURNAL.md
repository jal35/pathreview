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