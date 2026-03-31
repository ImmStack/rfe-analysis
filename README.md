# RFE Analysis

Open-source AI prompts for analyzing US immigration cases. Built for people navigating the visa process — whether you're a developer, attorney, or someone who just got an RFE and needs to understand what USCIS is asking for.

## What's Inside

### [RFE Analysis](skills/rfe-analysis/SKILL.md)
Upload a USCIS Request for Evidence (RFE) letter and get a structured breakdown:
- **Issue identification** — what USCIS is challenging, categorized by type (evidence gap, legal argument, policy interpretation, credibility)
- **Severity assessment** — critical / high / medium / low for each issue
- **Evidence patterns** — what types of documentation are commonly used in similar situations
- **General observations** — trends and patterns for this type of RFE

Supports: H-1B, EB-1A, EB-2 NIW, O-1A, L-1A/B

### [Visa Assessment](skills/visa-assessment/SKILL.md)
Analyze a professional profile against US talent visa criteria:
- **EB-1A** — Extraordinary Ability (10 criteria, Kazarian two-step)
- **EB-1B** — Outstanding Researcher
- **EB-2 NIW** — National Interest Waiver (Dhanasar three-prong)
- **O-1A / O-1B** — Extraordinary Ability / Achievement
- Criterion-by-criterion analysis with strength ratings

## Quick Start

### Option 1: Use with Claude Code

Clone this repo and use the built-in slash commands:

```bash
git clone https://github.com/ImmStack/rfe-analysis.git
cd rfe-analysis

# Analyze an RFE
claude "/analyze-rfe" < your-rfe-text.txt

# Assess a profile
claude "/assess-visa" < your-profile.txt
```

### Option 2: Use with Any LLM

1. Open the skill file you want (e.g., `skills/rfe-analysis/SKILL.md`)
2. Copy the **System Prompt** section
3. Paste it as the system message in ChatGPT, Claude, or any LLM
4. Paste your RFE text or professional profile as the user message
5. Get your analysis

### Option 3: Free Hosted Tool

Don't want to set anything up? Use the free hosted version:

- **RFE Analysis:** [s.immstack.ai/rfe](https://s.immstack.ai/rfe) — upload PDF, get instant analysis
- **Visa Assessment:** [s.immstack.ai](https://s.immstack.ai) — paste LinkedIn URL, get instant assessment

No sign-up required. We don't store your documents.

## How It Works

### RFE Analysis Methodology

The RFE skill categorizes every issue USCIS raises into one of four types:

| Category | What it means | Difficulty |
|----------|--------------|------------|
| **Evidence Gap** | Missing documents USCIS requested | Usually easiest |
| **Legal Argument** | Existing evidence needs better framing | Medium |
| **Policy Interpretation** | Case conflicts with USCIS standards | Harder |
| **Credibility** | Inconsistencies in statements/documents | Most serious |

Each issue gets a severity rating and a description of how similar cases are typically addressed — based on publicly available USCIS policy, regulations, and AAO decision patterns.

### Visa Assessment Methodology

The assessment skill evaluates profiles against the actual regulatory criteria:

- **EB-1A**: 10 criteria per 8 CFR 204.5(h)(3), with Kazarian two-step analysis
- **O-1A**: 8 criteria per 8 CFR 214.2(o)(3)(iii)
- **NIW**: Dhanasar three-prong framework
- Each criterion rated as strong / moderate / weak based on available evidence

## Examples

- [NIW RFE Analysis Example](skills/rfe-analysis/examples/niw-rfe-example.md) — synthetic example showing a three-prong Dhanasar challenge

## Important Disclaimer

These tools provide **educational information only** and do not constitute legal advice. Every immigration case is unique — the same evidence can lead to different outcomes depending on the specific facts, the adjudicator, and the service center.

**Always consult with a qualified U.S. immigration attorney about your specific situation.**

The analysis uses general language ("in cases like these", "common patterns") rather than personalized conclusions. This is intentional — we provide information about how the immigration system works, not advice about what you should do.

## Contributing

Found a way to improve the prompts? PRs welcome. Some ideas:

- Additional visa types (EB-3, H-1B1, TN, E-2)
- More example analyses (must be synthetic — no real case data)
- Translations of the prompts
- Integration guides for other LLM platforms

## License

MIT — use it however you want.

---

MIT License
