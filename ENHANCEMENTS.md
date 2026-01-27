# /intel Enhancement Roadmap

Based on meta-research using /intel itself.

## Problem: AI Research Tools Give Summaries, Not Insight

**Current gap:** Most AI tools aggregate search results but don't change how users think about markets.

**Enhancement for /intel:**
- Add "So What?" section to every output — explicit strategic implications
- Add "Contrarian Take" — what the data might be missing
- Add "If This Then That" — conditional recommendations

## Problem: Data Quality Concerns

**Current gap:** Users don't trust AI-generated market data.

**Enhancement for /intel:**
- Show source diversity score (how many independent sources?)
- Flag single-source claims explicitly
- Add "Verification Suggested" tags for weak signals
- Show recency of sources (last 30 days vs 6 months old)

## Problem: Too Many Tools, No Curation

**Current gap:** Users want fewer, better tools.

**Enhancement for /intel:**
- Add `/intel recommend [problem]` mode — curated tool suggestions
- Add `/intel stack [category]` — recommended tool combinations
- Focus on being THE research skill, not one of many

## Problem: Silent Failures in Skills

**Current gap:** Skills fail silently, users don't know why.

**Enhancement for /intel:**
- Add verbose mode: `/intel gaps "topic" --verbose`
- Show which searches succeeded/failed
- Explain confidence score reasoning
- Surface when rate limits affect results

## New Modes to Add

### `/intel validate [idea]`
Quick idea validation combining gaps + competitors + pain:
- Is there a real problem?
- Are there existing solutions?
- What's the differentiation opportunity?

### `/intel stack [category]`
Tool stack recommendations for a category:
- "What tools do successful [category] companies use?"
- Curated, opinionated recommendations

### `/intel watch [topic]`
Set up ongoing monitoring:
- Generate a one-time report
- Suggest what to track going forward
- Output could feed into Clawdbot cron jobs

## Output Enhancements

### Add "Strategic Implications" Section
```markdown
### Strategic Implications
- **If building:** [specific advice]
- **If investing:** [specific advice]  
- **If competing:** [specific advice]
```

### Add "Confidence Breakdown"
```markdown
### Confidence Breakdown
| Factor | Score | Why |
|--------|-------|-----|
| Source diversity | 8/10 | 5 independent sources |
| Recency | 7/10 | 80% from last 90 days |
| Engagement signals | 6/10 | Limited upvote data |
| **Overall** | **7/10** | |
```

### Add "What This Misses"
```markdown
### Limitations & Blind Spots
- Enterprise users underrepresented (don't post publicly)
- Survivorship bias (failed products not discussed)
- Geographic bias (English-language sources only)
```

## Technical Improvements

1. **Retry logic** — If search fails, try alternative queries
2. **Source deduplication** — Don't count same source twice
3. **Quote verification** — Flag if quote seems paraphrased
4. **Structured output option** — `/intel gaps "topic" --json`

## Competitive Moat

What makes /intel defensible:
1. **7 modes** — More comprehensive than /last30days
2. **No API keys** — Lower friction than competitors
3. **Business focus** — Not just prompts, actual decisions
4. **Self-improving** — Using itself to get better

## Next Version Targets

### v1.1
- [ ] Add "Strategic Implications" section
- [ ] Add "Confidence Breakdown" table
- [ ] Add `/intel validate` mode
- [ ] Improve error messaging

### v1.2
- [ ] Add `/intel stack` mode
- [ ] Add `--verbose` flag
- [ ] Add `--json` output option
- [ ] Add source recency tracking

### v2.0
- [ ] Add `/intel watch` mode (monitoring)
- [ ] Multi-language support
- [ ] Custom source configuration
- [ ] Integration with note-taking tools
