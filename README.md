# /intel

> Market intelligence in seconds. For builders who need business decisions, not just information.

While `/last30days` helps you find **prompts that work**, `/intel` helps you find **products to build**.

## What is this?

A Claude Code skill that turns market research from hours into seconds. Get actionable intelligence on gaps, competitors, sentiment, pricing, trends, and pain points — all with evidence and sources.

## Installation

```bash
# Clone to your Claude skills directory
git clone https://github.com/unisone/intel-skill.git ~/.claude/skills/intel
```

No API keys required. Uses Claude Code's built-in WebSearch.

## Commands

| Command | What it does |
|---------|--------------|
| `/intel gaps [topic]` | Find market gaps & unmet needs |
| `/intel competitors [product]` | Map competitive landscape |
| `/intel sentiment [topic]` | Quantify what people love/hate |
| `/intel pricing [category]` | Research pricing strategies |
| `/intel trends [topic]` | Analyze direction & velocity |
| `/intel pain [category]` | Find top frustrations |
| `/intel full [topic]` | Complete market intelligence |

## Examples

### Find Market Gaps
```
/intel gaps "AI video editing"
```
**Returns:** Ranked unmet needs with demand signals (mentions, upvotes, "would pay" quotes).

### Analyze Competitors
```
/intel competitors Notion
```
**Returns:** Competitive matrix with positioning, pricing, strengths, weaknesses.

### Check Sentiment
```
/intel sentiment "Claude Code"
```
**Returns:** Score (1-10), positive/negative breakdown, trend direction.

### Research Pricing
```
/intel pricing "email marketing SaaS"
```
**Returns:** Price tiers, models, what justifies premium, mistakes to avoid.

### Spot Trends
```
/intel trends "no-code tools"
```
**Returns:** Direction (📈/📊/📉), velocity, inflection points, 6-month forecast.

### Find Pain Points
```
/intel pain "project management"
```
**Returns:** Ranked frustrations with severity, frequency, willingness to pay.

### Full Report
```
/intel full "personal finance apps"
```
**Returns:** Complete market intelligence combining all modes.

## Output Format

Every `/intel` response includes:

- **TL;DR** — One paragraph executive summary
- **Key Findings** — 3-5 insights with evidence and sources
- **Data Points** — Quantified metrics in a table
- **Mode-specific analysis** — Gaps, competitors, sentiment, etc.
- **Confidence Level** — High/Medium/Low based on source quality
- **Research Stats** — Number of sources, total engagement

## How It Works

1. **Parse** — Understand mode and topic from your command
2. **Search** — Run 4-6 targeted WebSearches per mode
3. **Extract** — Pull quotes, numbers, engagement metrics
4. **Synthesize** — Weight sources, identify patterns, quantify
5. **Output** — Structured intelligence with citations

## Why /intel?

| Tool | Focus | Audience |
|------|-------|----------|
| `/last30days` | Prompts & techniques | Creators |
| `deep-research` | Academic research | Researchers |
| **`/intel`** | **Market intelligence** | **Builders, founders** |

## Philosophy

- **Quantify everything** — "23 mentions" not "frequently mentioned"
- **Cite sources** — Every claim links to evidence
- **Be actionable** — Enable decisions, not just awareness
- **Acknowledge uncertainty** — Low confidence = say so

## Requirements

- Claude Code (with WebSearch capability)
- No external API keys needed

## Contributing

PRs welcome! See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — build something great.

---

**Stop guessing. Start knowing.**

Built by [@alexxzay](https://twitter.com/alexxzay)
