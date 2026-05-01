# Prompt Protocol

> **Self-evolving 10-agent consensus prompt engineering.**  
> Token-optimized caveman output. No AI slop frontend. Persistent memory. Real autonomous loop. Prompt genealogy. Domain modules. Model adapters.

[![Version](https://img.shields.io/badge/version-12.0-blue)](./MANIFEST.json)
[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)
[![Claude](https://img.shields.io/badge/Claude.ai-Compatible-orange)](https://claude.ai)

---

## What is This?

**Prompt Protocol** is a skill package for Claude that transforms it into a self-improving prompt engineering factory. It doesn't just write prompts — it *forges* them through a 10-agent debate council, perfects them through an autonomous improvement loop, remembers what works across sessions, and tracks every evolution in a genealogy tree.

Every prompt is:
- **Forged** by 10 specialized agents debating and voting
- **Perfected** by an autonomous loop that stops only at perfection or plateau
- **Remembered** by a persistent memory system (with `window.storage` support)
- **Tracked** in an evolutionary genealogy tree (revert, branch, merge)
- **Specialized** by domain modules (fintech, medical, legal, gaming, etc.)
- **Portable** across models (Claude, GPT-4o, Gemini, Llama 3, Mistral)
- **Validated** against output contracts for structured data
- **Delivered** in caveman mode — maximum density, zero filler

---

## Installation

### Claude.ai (Web)
1. Download [`prompt-protocol.zip`](./prompt-protocol.zip)
2. Go to **Settings → Customize → Skills → Upload Skill**
3. Select the ZIP file
4. Toggle **ON**

### Claude Desktop App
1. Download [`prompt-protocol.zip`](./prompt-protocol.zip)
2. Go to **Settings → Capabilities → Skills → Upload Skill**
3. Select the ZIP file
4. Toggle **ON**

### Claude Code CLI
```bash
# Extract to skills directory
unzip prompt-protocol.zip -d ~/.claude/skills/
```

---

## Quick Start

Once installed, just ask Claude to write a prompt:

> *"Write me a prompt for a real-time stock trading dashboard"*

Prompt Protocol automatically activates and delivers a dense, description-only prompt forged by the agent council.

### Switch Caveman Intensity
```
/caveman lite       # Professional but tight
/caveman full       # Classic caveman (default)
/caveman ultra      # Maximum abbreviation
/caveman wenyan-lite    # Semi-classical Chinese
/caveman wenyan-full    # Full 文言文
/caveman wenyan-ultra   # Extreme classical compression
```

### Use Domain Specialization
```
[DOMAIN: fintech]   # Injects PCI-DSS, idempotency, double-entry
[DOMAIN: medical]   # Injects HIPAA, PHI protection, FHIR
[DOMAIN: gaming]    # Injects frame budgets, netcode, tick rate
```

### Target Different Models
```
[MODEL: gpt4o]      # Adapts for OpenAI format, XML tags
[MODEL: gemini]     # Adapts for Google format, numbered steps
[MODEL: llama3]     # Adapts for shorter context, explicit examples
```

---

## Architecture

```
User Request
    │
    ▼
┌─────────────────┐
│  SKILL_BOOT.md  │ ← Ultra-compressed core (~1,000 tokens)
│   (loads first) │
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼
SKILL.md   [LOAD: *]   ← Full docs on-demand
(full)     (lazy load)
    │
    ▼
┌─────────────────┐
│ 10-Agent Council │ ← Architect, Writer, Critic, Security,
│  (debate + vote) │    UX, Perf, Creative, Minimalist,
│                  │    UserProxy, **Engineer**
└────────┬────────┘
         │ 70% threshold
         ▼
┌─────────────────┐
│ Autonomous Loop │ ← 10-strategy rotation, plateau detection
│ (perfection engine)│   Max 10 cycles, interruptible
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼
Memory    Genealogy   ← Persistent storage, lineage tracking
System    Tracker
    │         │
    └────┬────┘
         ▼
┌─────────────────┐
│  Final Output   │ ← Caveman mode, zero code, description-only
│  (delivered)    │
└─────────────────┘
```

---

## File Structure

| File | Size | Purpose |
|------|------|---------|
| [`SKILL_BOOT.md`](./SKILL_BOOT.md) | 5.9 KB | Ultra-compressed core loader. Loads first. References full docs on-demand. |
| [`SKILL.md`](./SKILL.md) | 26.1 KB | Complete protocol specification. The master document. |
| [`AGENT_COUNCIL.md`](./AGENT_COUNCIL.md) | 6.5 KB | 10-agent collaboration system. Profiles, debate protocol, voting rules. |
| [`AUTONOMOUS_LOOP.md`](./AUTONOMOUS_LOOP.md) | 5.8 KB | Real autonomous perfection engine. 10-strategy rotation cycle. |
| [`MEMORY_SYSTEM.md`](./MEMORY_SYSTEM.md) | 5.2 KB | Persistent memory with `window.storage` support. 4-layer architecture. |
| [`GENEALOGY_TRACKER.md`](./GENEALOGY_TRACKER.md) | 4.4 KB | Prompt lineage system. Revert, branch, merge, compare, prune. |
| [`DOMAIN_MODULES.md`](./DOMAIN_MODULES.md) | 4.0 KB | 8 domain specializations. Regulatory constraints, terminology, best practices. |
| [`MODEL_ADAPTERS.md`](./MODEL_ADAPTERS.md) | 3.5 KB | 5 model adapters. Format translation, context awareness, safety calibration. |
| [`OUTPUT_CONTRACTS.md`](./OUTPUT_CONTRACTS.md) | 4.1 KB | Schema validation for structured outputs. 5-step validation pipeline. |
| [`FRONTEND_GUIDE.md`](./FRONTEND_GUIDE.md) | 6.3 KB | No AI slop bible. Typography, color, motion, spatial, background rules. |
| [`PROMPT_TEMPLATES.md`](./PROMPT_TEMPLATES.md) | 4.4 KB | 6 reusable prompt patterns with domain and model slots. |
| [`ADVANCED_TECHNIQUES.md`](./ADVANCED_TECHNIQUES.md) | 2.6 KB | 10 power-user techniques. Constraint stacking, temporal layering, etc. |
| [`REFERENCE.md`](./REFERENCE.md) | 1.9 KB | Quick reference. Caveman levels, agent weights, domain tags, commands. |
| [`EXAMPLES.md`](./EXAMPLES.md) | 5.4 KB | 4 real-world prompt examples. Dashboard, image gen, API, landing page. |
| [`MANIFEST.json`](./MANIFEST.json) | 3.0 KB | Skill metadata, changelog, compatibility flags, settings. |

**Total:** 15 files, ~89 KB unpacked

---

## The 10-Agent Council

| Agent | Weight | Veto? | Specialty |
|-------|--------|-------|-----------|
| **Security** | 1.3x | ✅ | Threat modeling, exploits, injection |
| **UserProxy** | 1.2x | ❌ | Intent alignment, satisfaction |
| **Engineer** | 1.2x | ❌ | Code quality, DRY, SOLID, complexity |
| **Architect** | 1.2x | ❌ | Structure, scalability, patterns |
| **Critic** | 1.1x | ❌ | Edge cases, contradictions, gaps |
| **Perf** | 1.1x | ❌ | Speed, efficiency, token economy |
| **Writer** | 1.0x | ❌ | Clarity, tone, token efficiency |
| **UX** | 1.0x | ❌ | User flow, intuition, delight |
| **Creative** | 1.0x | ❌ | Novelty, differentiation, wow |
| **Minimalist** | 1.0x | ❌ | Brevity, density, no waste |

**Conflict Priority:** Security → UserProxy → Engineer → Architect → Critic → Perf → Writer → UX → Creative → Minimalist

**Thresholds:** 70% proceed | 90% consensus lock | <70% debate (max 3 rounds)

---

## Key Features

### 🧠 Persistent Memory
- **4-layer architecture:** Prompt History, Pattern Library, User Preferences, Skill Evolution Log
- **`window.storage` support:** Auto-save after every prompt, auto-load at session start
- **Fallback:** Export/import memory snapshot for cross-session persistence
- **Decay system:** Unused patterns fade, successful patterns reinforce

### 🧬 Prompt Genealogy
- Every prompt has: ID, Parent ID, Generation, Branch
- **Operations:** Spawn, Revert, Branch, Merge, Prune, Compare
- **Commands:** `"revert to gen 3"`, `"branch: experiment"`, `"merge alpha + beta"`

### 🏛️ Domain Modules
Auto-detects or tags: `fintech`, `medical`, `legal`, `gaming`, `ecommerce`, `security`, `edu`, `creative`

### 🔌 Model Adapters
Translates for: `claude` (default), `gpt4o`, `gemini`, `llama3`, `mistral`

### 📋 Output Contract Validation
5-step validation for structured outputs: Schema check → Type validation → Format compliance → Cross-field consistency → Edge case handling

### 🎨 No AI Slop Frontend
- **NEVER:** Inter, Roboto, purple gradients, centered cards, fade-in scroll
- **ALWAYS:** Distinctive fonts, sharp accents, CSS-first motion, asymmetric layouts, atmospheric backgrounds

---

## Caveman Mode Examples

| Level | Example |
|-------|---------|
| **lite** | "Your component re-renders because you create a new object reference each render. Wrap it in useMemo." |
| **full** | "New object ref each render. Inline object prop = new ref = re-render. Wrap in useMemo." |
| **ultra** | "Inline obj prop → new ref → re-render. useMemo." |
| **wenyan-full** | "物出新參照，致重繪。useMemo 包之。" |

---

## Version History

See [`MANIFEST.json`](./MANIFEST.json) for full changelog.

- **v12.0** — Added Engineer agent, SKILL_BOOT.md, genealogy, domain modules, model adapters, output contracts, window.storage persistence
- **v11.0** — 9-agent collaboration, autonomous loop, persistent memory, self-evolving skill, frontend no-AI-slop protocol
- **v10.0** — Frontend design protocol with AI slop detection
- **v9.0** — Caveman mode with 6 intensity levels

---

## Contributing

This is a self-evolving skill. After every 10 prompts, the system analyzes performance and proposes upgrades. You can also force evolution:

```
"Evolve skill: add [capability]"
```

The skill will generate a proposal. You approve, reject, or modify.

---

## License

MIT License — use it, fork it, evolve it.

---

> *Forged by 10-agent debate. Perfected by autonomous loop. Remembered by persistent memory. Tracked by genealogy. Specialized by domain. Portable by model adapter. Validated by contract. Delivered by caveman. Designed with soul. Evolved forever.*
