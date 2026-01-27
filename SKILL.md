---
name: intel
description: Market intelligence in seconds. Research gaps, competitors, sentiment, pricing, trends, and pain points for any market or product. For builders who need business decisions, not just information.
argument-hint: "[mode] [topic]" — modes: gaps, competitors, sentiment, pricing, trends, pain, full
context: fork
agent: Explore
disable-model-invocation: true
allowed-tools: WebSearch, Read, Write, AskUserQuestion
---

# /intel — Market Intelligence in Seconds

Research any market, competitor, or product. Get actionable business intelligence with evidence.

**Use cases:**
- **Gaps**: "gaps AI video editing" → find unmet needs and opportunities
- **Competitors**: "competitors Notion" → map the competitive landscape
- **Sentiment**: "sentiment Claude Code" → quantify what people love/hate
- **Pricing**: "pricing email marketing SaaS" → research pricing strategies
- **Trends**: "trends no-code 2026" → analyze direction and velocity
- **Pain**: "pain project management" → find top frustrations
- **Full**: "full personal finance apps" → complete market intelligence report

---

## CRITICAL: Parse User Input

Before doing anything, parse the user's input:

```
/intel [MODE] [TOPIC]
```

**MODES** (first word after /intel):
- `gaps` → Find market gaps and opportunities
- `competitors` → Competitive landscape analysis  
- `sentiment` → What people love/hate (quantified)
- `pricing` → Pricing strategies and models
- `trends` → Direction, velocity, predictions
- `pain` → Top pain points and frustrations
- `full` → Complete report (all of the above)

**If no mode specified**, default to `full`.

**Store these variables:**
- `MODE = [gaps | competitors | sentiment | pricing | trends | pain | full]`
- `TOPIC = [extracted topic]`

---

## Research Execution

### Step 1: Build Search Queries

Based on MODE, construct targeted searches.

**Mode: GAPS**
Search for unmet needs and opportunities:
```
"{TOPIC}" "I wish" OR "why doesn't" OR "someone should build" site:reddit.com
"{TOPIC}" frustrating OR annoying OR "the problem with" site:reddit.com
"{TOPIC}" "would pay for" OR "shut up and take my money" site:reddit.com
"{TOPIC}" feature request OR missing site:news.ycombinator.com
"{TOPIC}" gaps OR opportunities OR underserved 2025 2026
```

**Mode: COMPETITORS**
Search for competitive landscape:
```
"{TOPIC}" vs OR versus OR alternative OR comparison site:reddit.com
"{TOPIC}" competitors OR "similar to" OR "like X but"
"{TOPIC}" review OR comparison 2025 2026
"{TOPIC}" pricing OR plans site:producthunt.com
best "{TOPIC}" alternatives 2026
```

**Mode: SENTIMENT**
Search for opinions and reactions:
```
"{TOPIC}" love OR hate OR amazing OR terrible site:reddit.com
"{TOPIC}" review honest opinion site:reddit.com  
"{TOPIC}" worth it OR overrated OR underrated
"{TOPIC}" switched from OR switched to OR migrated
"{TOPIC}" complaints OR praise site:twitter.com OR site:x.com
```

**Mode: PRICING**
Search for pricing intelligence:
```
"{TOPIC}" pricing OR price OR cost OR "how much"
"{TOPIC}" pricing strategy OR pricing model
"{TOPIC}" free tier OR freemium OR subscription
"{TOPIC}" expensive OR cheap OR "worth the price"
"{TOPIC}" pricing comparison 2025 2026
```

**Mode: TRENDS**
Search for trend direction:
```
"{TOPIC}" trending OR "on the rise" OR growing 2026
"{TOPIC}" dying OR declining OR "losing steam"
"{TOPIC}" future OR prediction OR "what's next"
"{TOPIC}" news OR announcement OR launch 2026
"{TOPIC}" hype OR bubble OR sustainable
```

**Mode: PAIN**
Search for pain points:
```
"{TOPIC}" frustrating OR annoying OR painful site:reddit.com
"{TOPIC}" "biggest problem" OR "main issue" OR "worst part"
"{TOPIC}" workaround OR hack OR "how do you deal with"
"{TOPIC}" complaint OR rant OR vent site:reddit.com
"{TOPIC}" broken OR buggy OR unreliable
```

**Mode: FULL**
Run ALL of the above search categories.

### Step 2: Execute WebSearches

Run 4-6 targeted WebSearches per mode (more for `full` mode).

**CRITICAL RULES:**
- Use the user's EXACT terminology — don't substitute based on your knowledge
- Look for SPECIFIC numbers: upvotes, likes, mention counts, prices
- Extract DIRECT QUOTES that support findings
- Note the SOURCE for every data point

### Step 3: Extract Data Points

For each search result, extract:
- **Source**: URL and platform (Reddit, HN, Twitter, blog, etc.)
- **Engagement**: Upvotes, likes, comments (if visible)
- **Key quote**: The most relevant 1-2 sentences
- **Relevance**: How directly it answers the query

---

## Synthesis: Judge Agent

After all searches complete, synthesize findings:

**Weight sources by reliability:**
1. **Reddit/HN** (highest) — real user discussions with engagement metrics
2. **Twitter/X** (high) — real-time sentiment, influencer opinions
3. **Product Hunt** (medium) — launch feedback, early adopter views
4. **Blogs/Reviews** (medium) — detailed analysis but may be biased/sponsored
5. **Company sites** (lowest) — useful for facts, not opinions

**Identify patterns:**
- What appears across MULTIPLE sources? (strongest signal)
- What has highest engagement? (validated interest)
- Any contradictions between sources?
- What's the confidence level? (many sources = high, few = low)

**Quantify everything:**
- Count mentions: "mentioned 12x across sources"
- Sum engagement: "847 total upvotes"
- Calculate ratios: "73% positive, 27% negative"
- Note frequency: "3 new complaints per week"

---

## Output Format

**ALWAYS structure output exactly like this:**

```markdown
## /intel {MODE}: {TOPIC}

### TL;DR
[One paragraph executive summary — the KEY insight a founder needs to know. Be specific and actionable.]

### Key Findings

**1. [Finding title]**
[2-3 sentences explaining the finding with SPECIFIC evidence]
- Source: [URL] — "[direct quote]" (+{upvotes} upvotes)

**2. [Finding title]**
[2-3 sentences with evidence]
- Source: [URL] — "[direct quote]" (+{upvotes})

**3. [Finding title]**
[2-3 sentences with evidence]
- Source: [URL] — "[direct quote]" (+{upvotes})

[Continue for 3-5 findings depending on depth]

### Data Points

| Metric | Value | Source |
|--------|-------|--------|
| [Specific metric] | [Number] | [Where from] |
| [Specific metric] | [Number] | [Where from] |
| [Specific metric] | [Number] | [Where from] |

### {MODE-SPECIFIC SECTION}

[See mode-specific sections below]

### Confidence Level

**{HIGH | MEDIUM | LOW}** — Based on {n} sources with {total engagement} total engagement.

[If LOW: "Limited data available. Consider primary research."]

---
📊 Research complete
├─ Sources: {n} Reddit · {n} HN · {n} Twitter · {n} other
├─ Total engagement: {sum} upvotes/likes
└─ Data freshness: Last 30-90 days

Need deeper analysis on any finding? Just ask.
```

---

## Mode-Specific Output Sections

### For GAPS mode:

```markdown
### Market Opportunities

| Gap | Demand Signal | Willing to Pay | Difficulty |
|-----|---------------|----------------|------------|
| [Gap 1] | {n} mentions, {upvotes} votes | "[quote about paying]" | Low/Med/High |
| [Gap 2] | ... | ... | ... |

### Recommended Action
[1-2 sentences on which gap to pursue and why]
```

### For COMPETITORS mode:

```markdown
### Competitive Landscape

| Competitor | Positioning | Pricing | Strengths | Weaknesses |
|------------|-------------|---------|-----------|------------|
| [Name 1] | [1-line positioning] | [price] | [strength] | [weakness] |
| [Name 2] | ... | ... | ... | ... |

### Positioning Opportunity
[Where is there room in the market?]
```

### For SENTIMENT mode:

```markdown
### Sentiment Breakdown

**Overall Score: {1-10}/10** ({positive}% positive, {negative}% negative, {neutral}% neutral)

**Most Praised:**
1. [Feature/aspect] — mentioned {n}x positively
2. [Feature/aspect] — mentioned {n}x positively

**Most Criticized:**
1. [Feature/aspect] — mentioned {n}x negatively  
2. [Feature/aspect] — mentioned {n}x negatively

**Sentiment Trend:** {Improving | Stable | Declining} over last 90 days
```

### For PRICING mode:

```markdown
### Pricing Landscape

| Tier | Price Range | Common Model | Example |
|------|-------------|--------------|---------|
| Budget | $X-Y/mo | [model] | [product] |
| Mid-market | $X-Y/mo | [model] | [product] |
| Premium | $X-Y/mo | [model] | [product] |

**What justifies premium pricing:**
- [Feature 1]
- [Feature 2]

**Pricing mistakes to avoid:**
- [Mistake 1] — "[quote]"
```

### For TRENDS mode:

```markdown
### Trend Analysis

**Direction:** {📈 Growing | 📊 Stable | 📉 Declining}
**Velocity:** {Rapid | Moderate | Slow}
**Confidence:** {High | Medium | Low}

**Key Inflection Points:**
- [Date]: [What happened]
- [Date]: [What happened]

**Emerging Sub-trends:**
1. [Sub-trend] — [evidence]
2. [Sub-trend] — [evidence]

**6-Month Forecast:**
[1-2 sentences predicting where this is heading]
```

### For PAIN mode:

```markdown
### Pain Point Rankings

| Rank | Pain Point | Severity | Frequency | Would Pay to Fix |
|------|------------|----------|-----------|------------------|
| 1 | [Pain] | {1-10} | {n}/week | "[quote]" |
| 2 | [Pain] | {1-10} | {n}/week | "[quote]" |

**Current Workarounds:**
- [Pain 1]: People currently [workaround]
- [Pain 2]: People currently [workaround]

**Biggest Opportunity:**
[Which pain point has highest severity + frequency + willingness to pay]
```

### For FULL mode:

Include ALL of the above sections, organized as:
1. TL;DR (synthesis of everything)
2. Market Gaps
3. Competitive Landscape  
4. Sentiment Overview
5. Pricing Intelligence
6. Trend Direction
7. Top Pain Points
8. Overall Recommendation

---

## Quality Checklist

Before outputting, verify:

- [ ] **Every claim has a source** — URL or platform cited
- [ ] **Numbers are specific** — "23 posts" not "many posts"  
- [ ] **Quotes are direct** — actual words from sources
- [ ] **Confidence is stated** — high/medium/low with reasoning
- [ ] **Actionable** — founder can make a decision from this
- [ ] **Fresh data** — prioritized recent discussions (30-90 days)
- [ ] **No hallucination** — only report what sources actually say

---

## Context Memory

After research completes, remember for this conversation:
- **MODE**: {mode}
- **TOPIC**: {topic}
- **KEY FINDINGS**: Top 3-5 insights
- **SOURCES**: The URLs and quotes you found

**You are now an EXPERT on this topic.**

For follow-up questions:
- Answer from your research (don't re-search)
- Cite the sources you found
- Offer to dive deeper on any finding

Only do new research if user asks about a DIFFERENT topic.

---

## Examples

**User:** `/intel gaps "AI video editing"`

**User:** `/intel competitors Notion`

**User:** `/intel sentiment "Claude Code"`

**User:** `/intel pricing "email marketing SaaS"`

**User:** `/intel trends "no-code tools"`

**User:** `/intel pain "project management"`

**User:** `/intel full "personal finance apps"`

---

**/intel** — Stop guessing. Start knowing.
