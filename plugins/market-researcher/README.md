# Market Researcher Plugin

Deep market research and startup ideation for founders, solopreneurs, and indie hackers.

Researches 20–30+ sources, mines community pain points, runs competitive intelligence, and produces full reports with validated startup ideas — with financial modeling and validation roadmaps.

## Skills

### `market-researcher`

A world-class market researcher, competitive analyst, and startup strategist in one skill.

**Trigger phrases** (auto-activates on any of these):
- "find me a startup idea"
- "research this niche"
- "is there a market for X"
- "what app should I build"
- "validate my idea"
- "what problems can I solve in [space]"
- "give me SaaS ideas"
- "I want to build something in the X space"

Also triggers proactively when you mention wanting to build a product but haven't validated the market yet.

## Research Modes

| Mode | Searches | Output |
|------|----------|--------|
| **Quick Scan** | 8–12 | Summary report, top 3 ideas |
| **Deep Research** *(default)* | 20–30 | Full report, 5–7 ideas, financials, validation roadmap |
| **Ultra Deep** | 30–50 | Everything + ICP profiles, full competitive matrix, GTM strategy |

Use "quick check" or "fast scan" for Quick Scan. Use "intensive", "thorough", or "go deep" for Ultra Deep. Everything else defaults to Deep Research.

## What Gets Researched

- **Community pain points** — Reddit, Indie Hackers, Hacker News, Product Hunt, Twitter
- **Review mining** — G2, Capterra, Trustpilot, App Store, Alternatives.to
- **Market intelligence** — Crunchbase, YC, Google Trends, Exploding Topics
- **SEO & keyword demand** — search volume proxies, competition signals
- **Adjacent signals** — job postings, course sales, newsletter audiences

## Output

Every Deep Research run produces:

1. **Full market research report** — executive summary, landscape, community pulse, ideas, competitive deep dive
2. **5–7 ranked startup idea cards** — problem, customer, competitors, opportunity, pricing, financials, risks, moat
3. **Validation roadmap** — pre-build validation steps for the #1 idea (week-by-week, with copy templates)

Reports are automatically saved to `./market-research/` in the current working directory.

### Gap Types Identified

The skill identifies 8 gap types: Price, Complexity, Niche, Integration, Speed/Quality, Distribution, Workflow, Modern Stack.

## Installation

```bash
# Via Claude Code marketplace (GitHub)
/plugins install https://github.com/rohitagr0310/my-plugins
```

Or add directly to your Claude Code settings:

```json
{
  "plugins": [
    "https://github.com/rohitagr0310/my-plugins/plugins/market-researcher"
  ]
}
```

## Example Usage

```
You: Research the AI writing tools niche — I want to find a gap to build into

Claude: [triggers market-researcher skill, runs 25 searches, returns full report
         with 6 ranked ideas and a validation roadmap for the top pick]
```

```
You: Quick check — is there a market for a Notion-to-podcast converter?

Claude: [Quick Scan mode, 10 searches, focused kill-shot or green-light verdict]
```

```
You: I want to build something in the legal tech space for solo lawyers

Claude: [auto-triggers market-researcher, clarifies builder profile, runs Deep Research]
```

## Templates

The skill ships with reusable output templates in `skills/market-researcher/templates/`:

| File | Purpose |
|------|---------|
| `01-full-market-research-report.md` | Full report scaffold |
| `02-idea-card.md` | Individual idea card format |
| `03-competitive-matrix.md` | Competitor comparison table |
| `04-icp-profile.md` | Ideal Customer Profile template |
| `05-validation-roadmap.md` | Pre-build validation checklist |

## License

MIT — [Rohit Agarwal](https://github.com/rohitagr0310)
