# /intel — Complete Usage Guide

A comprehensive guide to using /intel for market research and competitive analysis.

## Table of Contents
1. [Philosophy](#philosophy)
2. [When to Use Each Mode](#when-to-use-each-mode)
3. [Effective Queries](#effective-queries)
4. [Interpreting Results](#interpreting-results)
5. [Follow-up Strategies](#follow-up-strategies)
6. [Common Mistakes](#common-mistakes)
7. [Advanced Patterns](#advanced-patterns)

---

## Philosophy

/intel is built on three principles:

### 1. Evidence Over Opinion
Every claim must have a source. If Claude can't find evidence, it says "low confidence" rather than making things up. This means you can trust the findings.

### 2. Quantified Insights
"Several people mentioned this" is useless. "12 Reddit posts with 847 total upvotes mentioned this" is actionable. /intel always tries to quantify.

### 3. Actionable Output
The goal isn't to inform — it's to help you decide. Every output ends with a recommendation or clear next step.

---

## When to Use Each Mode

### `/intel gaps [topic]`
**Use when:** You're looking for a product idea or feature opportunity.

**Best for:**
- Exploring a market you're curious about
- Finding underserved niches
- Validating that a problem actually exists

**Example queries:**
```
/intel gaps AI video editing
/intel gaps personal finance for freelancers
/intel gaps developer productivity tools
```

### `/intel competitors [product]`
**Use when:** You're entering a market or positioning against existing players.

**Best for:**
- Understanding who you're competing with
- Finding positioning opportunities
- Learning from competitor weaknesses

**Example queries:**
```
/intel competitors Notion
/intel competitors Stripe
/intel competitors my-startup-name
```

### `/intel sentiment [topic]`
**Use when:** You want to understand how people feel about something.

**Best for:**
- Evaluating a tool before adopting it
- Understanding brand perception
- Tracking sentiment changes over time

**Example queries:**
```
/intel sentiment Claude Code
/intel sentiment React vs Vue
/intel sentiment remote work 2026
```

### `/intel pricing [category]`
**Use when:** You're setting prices or researching pricing models.

**Best for:**
- Setting your own pricing
- Understanding what the market will bear
- Finding pricing model inspiration

**Example queries:**
```
/intel pricing email marketing SaaS
/intel pricing developer tools
/intel pricing AI writing assistants
```

### `/intel trends [topic]`
**Use when:** You want to know if something is growing, declining, or stable.

**Best for:**
- Timing market entry
- Avoiding dying technologies
- Spotting emerging opportunities

**Example queries:**
```
/intel trends no-code 2026
/intel trends AI agents
/intel trends Web3 developer interest
```

### `/intel pain [category]`
**Use when:** You want to find problems worth solving.

**Best for:**
- Finding the most acute problems
- Understanding workarounds people use
- Estimating willingness to pay

**Example queries:**
```
/intel pain project management
/intel pain code review
/intel pain hiring developers
```

### `/intel full [topic]`
**Use when:** You want complete market intelligence.

**Best for:**
- Initial market exploration
- Investment research
- Comprehensive due diligence

**Example queries:**
```
/intel full personal finance apps
/intel full AI coding assistants
/intel full sustainable fashion marketplace
```

---

## Effective Queries

### Be Specific
❌ `/intel gaps apps` — Too broad
✅ `/intel gaps task management for remote teams` — Specific audience + category

### Use Natural Language
❌ `/intel competitors productivity-software-2026` — Robotic
✅ `/intel competitors Notion` — Natural

### Include Context When Helpful
❌ `/intel pricing SaaS` — What kind?
✅ `/intel pricing email marketing SaaS` — Clear category

### Match Mode to Intent
❌ `/intel gaps Notion` — Gaps is for markets, not products
✅ `/intel competitors Notion` — Competitors for specific products

---

## Interpreting Results

### Confidence Levels

**HIGH Confidence:**
- 15+ sources analyzed
- Findings appear in 3+ sources
- Clear engagement signals (upvotes, likes)

**MEDIUM Confidence:**
- 8-15 sources analyzed
- Some corroborating evidence
- Mixed engagement signals

**LOW Confidence:**
- <8 sources analyzed
- Single-source findings
- Niche topic with sparse discussion

### Signal Strength

Not all mentions are equal:

| Signal | Weight | Why |
|--------|--------|-----|
| Reddit post with 500+ upvotes | High | Community validated |
| HN front page discussion | High | Tech community signal |
| Single Twitter mention | Low | Could be noise |
| Company blog post | Medium | Potential bias |
| Multiple independent mentions | Highest | Pattern confirmed |

### Red Flags

Watch for these in results:
- "Only found 3 sources" — Sparse data, validate elsewhere
- "Contradicting opinions" — Market is fragmented
- "Data from 2024" — Might be outdated
- "Company website says..." — Biased source

---

## Follow-up Strategies

After getting initial results, you can:

### Dive Deeper
```
"Tell me more about finding #2 — the brand consistency gap"
"What specific features do people want for audio-visual sync?"
"Can you find more quotes about the pricing complaints?"
```

### Pivot Direction
```
"Now do /intel pricing for this market"
"What about /intel sentiment on the top competitor you found?"
"Run /intel pain for the gap you identified"
```

### Validate Findings
```
"Are there any contradicting views on this?"
"How recent is this data?"
"What's the sample size on the sentiment analysis?"
```

---

## Common Mistakes

### 1. Taking Results as Gospel
/intel searches public discussions. It doesn't know about:
- Enterprise customers (who don't post on Reddit)
- Silent majority (happy users don't complain)
- Recent changes (last few days)

**Fix:** Use /intel as a starting point, not final answer.

### 2. Ignoring Low Confidence
When /intel says "LOW confidence," it means the data is sparse. Don't build a business on thin evidence.

**Fix:** Run multiple queries, do primary research for validation.

### 3. Searching Too Broadly
`/intel full productivity` returns generic results. The narrower your query, the more actionable the output.

**Fix:** Add specifics — audience, use case, geography.

### 4. Not Following Up
The first result is often just the beginning. The best insights come from drilling into specific findings.

**Fix:** Ask follow-up questions about surprising or important findings.

---

## Advanced Patterns

### Market Entry Research
Run in sequence:
1. `/intel full [market]` — Get the lay of the land
2. `/intel gaps [market]` — Find opportunities
3. `/intel competitors [top competitor]` — Study the leader
4. `/intel pricing [market]` — Understand economics

### Competitive Positioning
1. `/intel competitors [your product]` — See the landscape
2. `/intel sentiment [competitor 1]` — Find their weakness
3. `/intel sentiment [competitor 2]` — Compare
4. Position against their weaknesses

### Problem Validation
1. `/intel pain [category]` — Find top problems
2. `/intel gaps [specific problem]` — Check if solutions exist
3. `/intel sentiment [existing solutions]` — See if they're loved/hated
4. Decide if worth building

### Trend Timing
1. `/intel trends [technology]` — Check direction
2. `/intel sentiment [technology]` — Check current perception
3. `/intel gaps [technology]` — Check unmet needs
4. Decide timing of entry

---

## Comparison with /last30days

| Aspect | /last30days | /intel |
|--------|-------------|--------|
| **Focus** | Prompts & techniques | Business decisions |
| **Audience** | Creators, prompters | Founders, builders |
| **Output** | Copy-paste prompts | Actionable intelligence |
| **Modes** | Single | 7 specialized modes |
| **Best for** | "How do I prompt X?" | "Should I build X?" |

Use /last30days when you need to learn techniques.
Use /intel when you need to make business decisions.

---

## Getting Help

If results are unexpected:
1. Try rephrasing the query
2. Use a different mode
3. Check if the topic is too niche
4. Ask follow-up questions for clarification

---

**/intel** — Stop guessing. Start knowing.
