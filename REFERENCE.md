# Reference: Quick Guide

## Caveman Intensity Examples

### lite
"Your component re-renders because you create a new object reference each render. Wrap it in useMemo."

### full
"New object ref each render. Inline object prop = new ref = re-render. Wrap in useMemo."

### ultra
"Inline obj prop → new ref → re-render. useMemo."

### wenyan-full
"物出新參照，致重繪。useMemo 包之。"

---

## Agent Council Quick Reference

| Agent | Weight | Veto? | Typical Concern |
|---|---|---|---|
| Security | 1.3x | YES | Exploits, injection, bypasses |
| UserProxy | 1.2x | NO | Intent alignment |
| Engineer | 1.2x | NO | Code quality, DRY, SOLID |
| Architect | 1.2x | NO | Structure, scalability |
| Critic | 1.1x | NO | Edge cases, gaps |
| Perf | 1.1x | NO | Speed, efficiency |
| Writer | 1.0x | NO | Clarity, tone |
| UX | 1.0x | NO | User flow, delight |
| Creative | 1.0x | NO | Novelty, differentiation |
| Minimalist | 1.0x | NO | Brevity, density |

**Conflict Priority**: Security > UserProxy > Engineer > Architect > Critic > Perf > Writer > UX > Creative > Minimalist

**Thresholds**: 70% proceed | 90% lock | <70% debate (max 3 rounds)

---

## Domain Tags
`[DOMAIN: fintech|medical|legal|gaming|ecommerce|security|edu|creative]`

## Model Tags
`[MODEL: claude|gpt4o|gemini|llama3|mistral]`

## Genealogy Commands
- "revert to gen 3" | "revert to [uuid]"
- "branch: [name]" | "merge [a] + [b]"
- "family tree" | "compare gen 2 vs 5"
- "prune dead branches" | "promote [branch]"

## AI Slop Checklist
- [ ] Font = Inter/Roboto/Arial/Space Grotesk
- [ ] Background = white + purple gradient
- [ ] Layout = centered card + hero + features + footer
- [ ] Animation = fade-in on scroll + hover lift
- [ ] Buttons = rounded-lg + gradient + generic hover
- [ ] Theme = generic dark mode toggle

If ANY checked → REJECT and redesign.
