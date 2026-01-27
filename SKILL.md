# /intel — Market Intelligence in Seconds

Research any market, competitor, or trend. Get actionable intelligence, not just information.

## Commands

```bash
/intel gaps <topic>         # Find market gaps & opportunities
/intel competitors <product> # Competitive landscape analysis
/intel sentiment <topic>    # What people love/hate (quantified)
/intel pricing <category>   # How competitors price
/intel trends <topic>       # Direction + velocity + predictions
/intel pain <category>      # Top pain points people have
/intel full <topic>         # All of the above in one report
```

## How It Works

When the user invokes `/intel <mode> <topic>`:

1. **Search Phase** — Query Reddit, X/Twitter, HN, Product Hunt, Google via web search
2. **Extract Phase** — Pull key data points, quotes, numbers
3. **Analyze Phase** — Identify patterns, quantify sentiment, rank by engagement
4. **Synthesize Phase** — Create actionable output with evidence

## Output Format

Always structure output as:

```markdown
## /intel <mode>: <topic>

### TL;DR
[One paragraph executive summary with the key insight]

### Key Findings
1. [Finding with evidence]
2. [Finding with evidence]
3. [Finding with evidence]

### Data Points
| Metric | Value | Source |
|--------|-------|--------|
| ... | ... | ... |

### Opportunities / Recommendations
- [Actionable item 1]
- [Actionable item 2]

### Sources
- [URL 1] — [key quote]
- [URL 2] — [key quote]
```

## Mode Details

### /intel gaps <topic>
Find what's MISSING in a market. Look for:
- "I wish there was..."
- "Why doesn't anyone build..."
- "The problem with X is..."
- Complaints about existing solutions
- Features people request but don't exist

Output: Ranked list of gaps with demand evidence (upvotes, likes, frequency).

### /intel competitors <product>
Map the competitive landscape:
- Direct competitors (same solution, same market)
- Indirect competitors (different solution, same problem)
- Key differentiators
- Pricing comparison
- Strengths/weaknesses

Output: Competitive matrix with positioning insights.

### /intel sentiment <topic>
Quantify what people think:
- Positive vs negative ratio
- Most praised features/aspects
- Most criticized features/aspects
- Sentiment trend (improving/declining)

Output: Sentiment score (1-10) with breakdown and key quotes.

### /intel pricing <category>
Research pricing strategies:
- Price points in market
- Pricing models (subscription, one-time, freemium, usage)
- What features justify premium pricing
- Common pricing mistakes

Output: Pricing landscape with recommendations.

### /intel trends <topic>
Analyze trend direction:
- Volume of discussion (up/down/flat)
- Key inflection points
- Emerging sub-trends
- Prediction of where it's heading

Output: Trend analysis with timeline and forecast.

### /intel pain <category>
Find the biggest pain points:
- What frustrates people most
- Workarounds people use
- How much they'd pay to solve it
- Frequency of complaints

Output: Ranked pain points with severity and demand.

### /intel full <topic>
Complete market intelligence report combining all modes.
Use when exploring a new market or validating an idea.

## Search Strategy

For each query, search across:

1. **Reddit** — `site:reddit.com "<topic>" [pain words]`
2. **Hacker News** — `site:news.ycombinator.com "<topic>"`
3. **Twitter/X** — Use web search for `site:twitter.com OR site:x.com "<topic>"`
4. **Product Hunt** — `site:producthunt.com "<topic>"`
5. **General** — Broad search for reviews, comparisons, complaints

### Pain/Gap Keywords
- "I wish", "why doesn't", "frustrating", "annoying", "hate"
- "anyone know", "alternative to", "better than"
- "would pay for", "shut up and take my money"
- "the problem with", "my biggest issue"

### Freshness
Default to last 30-90 days unless historical context needed.
Prioritize recent discussions (more relevant to current market).

## Example Usage

**User:** `/intel gaps "AI video editing"`

**Output:**
```markdown
## /intel gaps: AI video editing

### TL;DR
The biggest unmet need is **brand consistency across clips** — creators want AI that remembers their style, fonts, colors, and maintains them across multiple videos. Current tools treat each video as isolated.

### Key Findings
1. **Brand memory is broken** — 23 Reddit posts mention wanting consistent style across videos. "I spend more time re-applying my brand settings than actually editing" (+847 upvotes, r/VideoEditing)

2. **Scene transitions are jarring** — AI generates good individual clips but connecting them smoothly requires manual work. Gap for "AI transition intelligence."

3. **Audio-visual sync still manual** — Beat matching, lip sync, and sound design are poorly automated. "Auto-beat sync is a joke" (ProductHunt comment, +156)

4. **No good "enhance old footage" tool** — Upscaling exists but comprehensive restoration (stabilization + color + noise + sharpening) in one tool is missing.

### Data Points
| Gap | Mentions | Avg Engagement | Willing to Pay |
|-----|----------|----------------|----------------|
| Brand consistency | 23 | 412 upvotes | "$20-50/mo" |
| Smart transitions | 18 | 287 upvotes | "$10-30/mo" |
| Audio-visual sync | 15 | 203 upvotes | "$15-40/mo" |
| Footage restoration | 12 | 178 upvotes | "$30-100 one-time" |

### Opportunities
- Build a "brand memory" layer that sits on top of existing AI video tools
- Transition-focused tool (small scope, quick to build)
- All-in-one footage restoration (clear pricing opportunity)

### Sources
- reddit.com/r/VideoEditing/comments/xyz — "Brand consistency is my nightmare"
- producthunt.com/products/luma/reviews — "Great but forgets my style"
- news.ycombinator.com/item?id=123 — "Beat sync is the missing piece"
```

## Best Practices

1. **Always cite sources** — Every claim needs a link
2. **Quantify when possible** — Upvotes, likes, frequency, dollars
3. **Be specific** — "23 posts" not "many posts"
4. **Actionable > interesting** — Focus on what the user can DO with the info
5. **Acknowledge gaps** — If data is sparse, say so
6. **Time-bound** — Note when data is from (last week vs last year matters)

## Requirements

- Web search capability (built into Claude Code)
- No external API keys required
- Works with any topic

## Installation

```bash
# Clone to your Claude skills directory
git clone https://github.com/unisone/intel-skill.git ~/.claude/skills/intel

# Or just copy SKILL.md to your project
```

---

**/intel** — Stop guessing. Start knowing.
