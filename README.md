# /intel

[![GitHub release](https://img.shields.io/github/v/release/unisone/intel-skill?style=flat-square)](https://github.com/unisone/intel-skill/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-skill-blueviolet?style=flat-square)](https://claude.ai/code)
[![skills.sh](https://img.shields.io/badge/skills.sh-compatible-green?style=flat-square)](https://skills.sh)

> **Market intelligence in seconds.** For builders who need business decisions, not just information.

<p align="center">
  <img src="assets/demo.gif" alt="intel demo" width="600">
</p>

---

## ⚡ Quick Install

```bash
npx skills add unisone/intel-skill
```

**No API keys required.** Uses Claude Code's built-in WebSearch.

---

## 🎯 What is /intel?

A Claude Code skill that turns market research from **hours into seconds**.

While `/last30days` helps you find prompts that work, **`/intel` helps you find products to build.**

Get actionable intelligence on:
- 🔍 **Gaps** — Unmet needs and opportunities
- 🏢 **Competitors** — Market landscape mapping
- 💬 **Sentiment** — What people love and hate
- 💰 **Pricing** — Strategy and positioning
- 📈 **Trends** — Direction and velocity
- 😤 **Pain** — Top frustrations worth solving
- ✅ **Validate** — Quick idea go/no-go

---

## 📋 Commands

| Command | Purpose |
|---------|---------|
| `/intel gaps [topic]` | Find market gaps & unmet needs |
| `/intel competitors [product]` | Map competitive landscape |
| `/intel sentiment [topic]` | Quantify love/hate ratio |
| `/intel pricing [category]` | Research pricing strategies |
| `/intel trends [topic]` | Analyze direction & velocity |
| `/intel pain [category]` | Find top frustrations |
| `/intel validate [idea]` | Quick idea validation (BUILD/DON'T BUILD) |
| `/intel full [topic]` | Complete market intelligence |

---

## 🚀 Examples

### Validate an Idea (New!)
```
/intel validate "AI-powered CRM for freelancers"
```
**Returns:** Problem exists? (YES/NO) → Competition level → Differentiation opportunity → **BUILD/DON'T BUILD** verdict

### Find Market Gaps
```
/intel gaps "AI video editing"
```
**Returns:** Ranked unmet needs with demand signals, quotes, and strategic implications.

### Analyze Competitors
```
/intel competitors Notion
```
**Returns:** Competitive matrix with positioning, pricing, sentiment, and positioning gaps.

### Check Sentiment
```
/intel sentiment "Claude Code"
```
**Returns:** Score (1-10), most loved/hated features, trend direction.

### Full Report
```
/intel full "personal finance apps"
```
**Returns:** Complete market intelligence combining all modes.

---

## 📊 Output Format

Every `/intel` response includes:

| Section | What You Get |
|---------|--------------|
| **TL;DR** | One-paragraph executive summary |
| **Key Findings** | 3-5 insights with evidence and quotes |
| **Data Summary** | Quantified metrics table |
| **Strategic Implications** | If building / If investing / Contrarian take |
| **Confidence Breakdown** | Source diversity, recency, signal strength |
| **Limitations** | Data gaps, bias warnings, blind spots |

---

## 🧠 How It Works

```
1. PARSE → Understand mode and topic
2. SEARCH → Run 5-8 targeted WebSearches
3. EXTRACT → Pull quotes, numbers, signals
4. SYNTHESIZE → Weight sources, find patterns
5. OUTPUT → Structured intelligence with citations
```

---

## 📁 Examples

See the [`examples/`](examples/) folder for complete output samples:

| File | Topic |
|------|-------|
| [gaps-example.md](examples/gaps-example.md) | AI video editing market gaps |
| [competitors-example.md](examples/competitors-example.md) | Notion competitive analysis |
| [sentiment-example.md](examples/sentiment-example.md) | Claude Code sentiment |

---

## 🔧 Requirements

- Claude Code (with WebSearch capability)
- No external API keys needed

---

## 🤝 Contributing

PRs welcome! See [CONTRIBUTING.md](CONTRIBUTING.md).

Ideas for contribution:
- Additional output modes
- Better search templates for specific industries
- Localization for non-English markets

---

## 📜 License

[MIT](LICENSE) — build something great.

---

## 🔗 Links

- **GitHub:** [github.com/unisone/intel-skill](https://github.com/unisone/intel-skill)
- **skills.sh:** `npx skills add unisone/intel-skill`
- **Author:** [@alexxzay](https://twitter.com/alexxzay)

---

<p align="center">
  <strong>Stop guessing. Start knowing.</strong>
</p>

## Also By @unisone

- [claude-learner](https://github.com/unisone/claude-learner) — Auto-generate CLAUDE.md improvements from session analysis
- [moltbot-config](https://github.com/unisone/moltbot-config) — Production memory engine, self-review system, and configs for Moltbot
- [agentpulse](https://github.com/unisone/agentpulse) — Real-time agent monitoring dashboard
