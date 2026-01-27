# /intel

> Market intelligence in seconds. For builders who need answers, not just information.

<p align="center">
  <img src="assets/intel-banner.png" alt="Intel Skill" width="600">
</p>

## What is this?

A Claude Code skill that turns market research from hours into seconds.

While `/last30days` helps you find **prompts that work**, `/intel` helps you find **products to build**.

## Commands

| Command | What it does |
|---------|--------------|
| `/intel gaps <topic>` | Find market gaps & opportunities |
| `/intel competitors <product>` | Competitive landscape analysis |
| `/intel sentiment <topic>` | What people love/hate (quantified) |
| `/intel pricing <category>` | How competitors price |
| `/intel trends <topic>` | Direction + velocity + predictions |
| `/intel pain <category>` | Top pain points people have |
| `/intel full <topic>` | Complete market intelligence report |

## Quick Start

```bash
# Clone to your Claude skills directory
git clone https://github.com/unisone/intel-skill.git ~/.claude/skills/intel
```

Then in Claude Code:
```
/intel gaps "AI video editing"
```

## Examples

### Find Market Gaps
```
/intel gaps "personal finance apps"
```
Returns: Ranked list of unmet needs with demand evidence (upvotes, frequency, "would pay" signals).

### Analyze Competitors
```
/intel competitors "Notion"
```
Returns: Competitive matrix, positioning, pricing comparison, strengths/weaknesses.

### Check Sentiment
```
/intel sentiment "Claude Code"
```
Returns: Sentiment score (1-10), love/hate breakdown, trend direction.

### Research Pricing
```
/intel pricing "email marketing SaaS"
```
Returns: Price points, models, what justifies premium, common mistakes.

### Spot Trends
```
/intel trends "AI agents"
```
Returns: Volume direction, inflection points, emerging sub-trends, forecast.

### Find Pain Points
```
/intel pain "project management"
```
Returns: Ranked frustrations with severity and demand.

## How It Works

1. **Search** — Queries Reddit, HN, Twitter, Product Hunt, Google
2. **Extract** — Pulls quotes, numbers, engagement metrics
3. **Analyze** — Identifies patterns, quantifies sentiment
4. **Synthesize** — Creates actionable intelligence with evidence

No external API keys needed. Uses Claude Code's built-in web search.

## Why /intel?

| Tool | Focus | Best For |
|------|-------|----------|
| `/last30days` | Prompts & trends | Creators, prompters |
| `deep-research` | Academic research | Researchers |
| **`/intel`** | Market intelligence | **Builders, founders** |

## Philosophy

- **Quantify everything** — "23 posts" not "many posts"
- **Cite sources** — Every claim has a link
- **Be actionable** — Focus on what you can DO
- **Be honest** — If data is sparse, say so

## Requirements

- Claude Code (any version with web search)
- No API keys needed

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — build something great.

---

**Stop guessing. Start knowing.**

Built by [@alexxzay](https://twitter.com/alexxzay)
