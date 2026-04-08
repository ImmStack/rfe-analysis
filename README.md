<p align="center">
  <img src="https://img.shields.io/badge/Skills-5-blue" alt="Skills">
  <img src="https://img.shields.io/badge/Visa_Types-6-green" alt="Visa Types">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="MIT License">
  <img src="https://img.shields.io/github/stars/AIStack-Legal/rfe-analysis?style=social" alt="Stars">
</p>

# Immigration AI Skills

Open-source AI prompts for US immigration cases. Works with Claude, ChatGPT, or any LLM. Built for developers, attorneys, and anyone navigating the visa process.

**5 skills** covering the full immigration workflow: strategy, evidence planning, petition drafting support, RFE analysis, and expert letter frameworks.

## Skills

| Skill | What it does | Lines |
|-------|-------------|-------|
| [Petition Strategy](skills/petition-strategy/SKILL.md) | Figure out which visa to pursue. Compares EB-1A vs NIW vs O-1A vs EB-1B with criteria mapping | 368 |
| [Evidence Checklist](skills/evidence-checklist/SKILL.md) | Per-criterion evidence guide with Tier 1/2/3 strength ratings for EB-1A, NIW, O-1A | 565 |
| [Expert Letter Framework](skills/expert-letter/SKILL.md) | Structure recommendation letters. Independent vs dependent experts, per-criterion guidance | 410 |
| [RFE Analysis](skills/rfe-analysis/SKILL.md) | Break down a USCIS RFE notice. Issue mapping, deficiency classification, severity, service center patterns | 355 |
| [Visa Assessment](skills/visa-assessment/SKILL.md) | Evaluate a profile against visa criteria. Strength ratings per criterion | 265 |

## Quick Start

### Claude Code

```bash
git clone https://github.com/AIStack-Legal/rfe-analysis.git
cd rfe-analysis

# Plan which visa to pursue
claude "/plan-strategy"

# Generate evidence checklist
claude "/evidence-checklist"

# Analyze an RFE
claude "/analyze-rfe"

# Assess a profile
claude "/assess-visa"

# Draft expert letter framework
claude "/draft-expert-letter"
```

### ChatGPT / Claude / Any LLM

1. Open any skill file (e.g., `skills/rfe-analysis/SKILL.md`)
2. Copy the **System Prompt** section
3. Paste as the system message in your LLM
4. Paste your RFE text, profile, or question as the user message

### Free Hosted Tool

No setup needed:

- **RFE Analysis:** [aistack.legal](https://aistack.legal) — upload PDF, get instant analysis
- **Visa Assessment:** [aistack.legal/linkedin](https://aistack.legal/linkedin) — paste LinkedIn URL

No sign-up. Documents are not stored.

## What's Covered

| Visa Type | Strategy | Evidence | Expert Letters | RFE Analysis | Assessment |
|-----------|----------|----------|----------------|--------------|------------|
| EB-1A (Extraordinary Ability) | All 10 criteria | Tier 1/2/3 per criterion | Per-criterion guidance | Full support | Full support |
| EB-2 NIW (National Interest Waiver) | Dhanasar 3 prongs | Per-prong evidence | Prong-specific | Full support | Full support |
| O-1A (Extraordinary Ability) | All 8 criteria | Tier 1/2/3 per criterion | Per-criterion guidance | Full support | Full support |
| EB-1B (Outstanding Researcher) | 2 requirements | Basic | Basic | Partial | Full support |
| O-1B (Arts/Entertainment) | 6 criteria | Basic | Basic | Partial | Full support |
| H-1B (Specialty Occupation) | 4 RFE areas | N/A | N/A | Full support | N/A |

## How It Works

Each skill contains a detailed system prompt encoding immigration law knowledge from public sources:

- **8 CFR** (Code of Federal Regulations) — the actual rules
- **USCIS Policy Manual** — how USCIS interprets the rules
- **Published AAO decisions** — how the Administrative Appeals Office has applied the rules
- **Federal case law** — Kazarian v. USCIS (EB-1A framework), Matter of Dhanasar (NIW framework)

The prompts classify, analyze, and explain — they don't give legal advice. Every skill includes UPL compliance rules that keep the AI in educational territory.

### RFE Analysis Deep Dive

The RFE skill classifies every issue USCIS raises:

| Category | What it means | Typical difficulty |
|----------|--------------|-------------------|
| Evidence Gap | Missing documents | Usually easiest |
| Legal Argument | Evidence needs better framing | Medium |
| Policy Interpretation | Case conflicts with USCIS standards | Harder |
| Credibility | Inconsistencies in documents | Most serious |

Deficiency types: `NO_EVIDENCE`, `INSUFFICIENT_QUANTITY`, `INSUFFICIENT_QUALITY`, `WRONG_EVIDENCE_TYPE`, `MISSING_CONTEXT`, `FINAL_MERITS`

Service center detection from receipt number (TSC = quantitative focus, NSC = narrative focus).

## Important Disclaimer

These tools provide **educational information only** and do not constitute legal advice. Every immigration case is unique.

**Always consult with a qualified U.S. immigration attorney about your specific situation.**

The skills use general language ("in cases like these", "common patterns") rather than personalized conclusions. This is intentional.

## Contributing

PRs welcome:

- Additional visa types (EB-3, TN, E-2, EB-5)
- More examples (must be synthetic, no real case data)
- Translations
- Integration guides for other LLM platforms
- Improvements to existing skills

## License

MIT
