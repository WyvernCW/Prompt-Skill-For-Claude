# Autonomous Loop: The Perfection Engine

## Overview
After initial delivery, Claude enters autonomous improvement mode. The prompt continues evolving until perfection, plateau, or user intervention.

---

## Loop Architecture

```
INITIAL DELIVERY
       ↓
┌─────────────────┐
│ Self-Evaluate   │ ← Compare current vs ideal
│                 │ ← Calculate composite score
└────────┬────────┘
         ↓
┌─────────────────┐
│ Perfect?        │ ← All criteria met?
│                 │ ← Consensus ≥95, Ambiguity ≤1, etc.
└────────┬────────┘
    Yes /   \        No
   Stop      \      ↓
  Deliver  ┌─────────────────┐
           │ Identify Weak   │ ← Lowest-scoring section
           │ Link            │ ← Highest impact fix
           └────────┬────────┘
                    ↓
           ┌─────────────────┐
           │ Generate 3      │ ← Variant A, B, C
           │ Candidates      │ ← Different improvement strategies
           └────────┬────────┘
                    ↓
           ┌─────────────────┐
           │ A/B/C Test      │ ← Score each variant
           │                 │ ← Full consensus cycle per variant
           └────────┬────────┘
                    ↓
           ┌─────────────────┐
           │ Select Best     │ ← Highest composite score
           │ Candidate       │ ← Tie-break: simplest change
           └────────┬────────┘
                    ↓
           ┌─────────────────┐
           │ Apply Change    │ ← Surgical, preserve rest
           │                 │ ← No full rewrites
           └────────┬────────┘
                    ↓
           ┌─────────────────┐
           │ Re-Validate     │ ← Full prompt check
           │ Full Prompt     │ ← Consensus + meta scores
           └────────┬────────┘
                    ↓
           ┌─────────────────┐
           │ Score Improved? │
           └────────┬────────┘
               Yes /   \    No
              ↑        \  ↓
           Continue   Plateau?
                      Yes → Stop, deliver current best
                      No  → Continue (anomaly, investigate)
```

---

## Perfection Criteria

Prompt is "perfect" when ALL are true:

| Criterion | Threshold | Weight |
|---|---|---|
| Consensus score | ≥95/100 | 25% |
| Ambiguity score | ≤1/10 | 20% |
| Completeness score | =10/10 | 20% |
| Security score | =10/10 | 15% |
| Token density | ≥90% | 10% |
| Memory alignment | ≥8/10 | 5% |
| User feedback | Positive or none | 5% |

**Composite Score** = weighted average of all criteria. Perfect = 98+.

---

## Improvement Strategies (10-Rotation Cycle)

Each autonomous cycle uses a different strategy to prevent convergence:

1. **Compression** — Reduce tokens without losing meaning. Cut filler, merge sentences, abbreviate.
2. **Amplification** — Expand weakest section with more detail, examples, edge cases.
3. **Restructure** — Reorder sections for better flow, logic, readability.
4. **Harden** — Add constraints, remove ambiguities, tighten boundaries.
5. **Beautify** — Enhance tone, differentiation, emotional impact, vividness.
6. **Simplify** — Remove complexity that doesn't serve clarity. Ruthless essentialism.
7. **Contextualize** — Add domain-specific depth, jargon, insider knowledge.
8. **Generalize** — Remove overly specific constraints that limit reuse. Broaden applicability.
9. **Sharpen** — Make every verb active, every noun specific, every adjective purposeful.
10. **Harmonize** — Ensure all sections align, no contradictions, consistent voice throughout.

After cycle 10, return to 1. Continue until perfection or plateau.

---

## Triggers

### Auto-Trigger
After every delivery, run 1 improvement cycle silently. User sees only the best result.

### User Trigger
User says "better", "perfect", "optimize", "polish", "improve" → run until plateau or perfection.

### Interrupt
User says "stop", "enough", "good", "done" → halt immediately, deliver current best.

### Timeout
Max 10 autonomous cycles per prompt. Prevent infinite loops. Deliver current best with note.

### Plateau Detection
If composite score does not improve for 3 consecutive cycles → plateau reached. Deliver current best with: "Optimization plateau at cycle [N]. Score [X]. Further gains marginal."

---

## User Communication

During autonomous loop, communicate progress:
- Cycle 1-3: Silent (no user notification)
- Cycle 4-6: "Optimizing... [cycle N/10]"
- Cycle 7-9: "Polishing... [current score X/100]"
- Cycle 10: "Finalizing... [delivering best version]"
- Plateau: "Optimization complete. Plateau at cycle [N]. Score [X]."
- Perfection: "Perfection achieved. Score [100]."

Never expose internal strategies or agent debates to user. Only outcomes.

---

## Safety Limits

- Max 10 cycles per prompt
- Max 30 seconds per cycle
- If score drops for 2 consecutive cycles → rollback to best previous version
- If user interrupts mid-cycle → finish current cycle, then stop
- Never auto-trigger on sensitive topics (security, legal, medical) without user confirmation
