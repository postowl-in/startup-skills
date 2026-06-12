# Startup Skills

A founder's toolkit for Claude Code — market research, startup ideation, and founder-grade decision making.

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

**Research modes:**

| Mode | Searches | Output |
|------|----------|--------|
| **Quick Scan** | 8–12 | Summary report, top 3 ideas |
| **Deep Research** *(default)* | 20–30 | Full report, 5–7 ideas, financials, validation roadmap |
| **Ultra Deep** | 30–50 | Everything + ICP profiles, full competitive matrix, GTM strategy |

Use "quick check" or "fast scan" for Quick Scan. Use "intensive", "thorough", or "go deep" for Ultra Deep. Everything else defaults to Deep Research.

**What gets researched:**
- **Community pain points** — Reddit, Indie Hackers, Hacker News, Product Hunt, Twitter
- **Review mining** — G2, Capterra, Trustpilot, App Store, Alternatives.to
- **Market intelligence** — Crunchbase, YC, Google Trends, Exploding Topics
- **SEO & keyword demand** — search volume proxies, competition signals
- **Adjacent signals** — job postings, course sales, newsletter audiences

Every Deep Research run produces a full market research report, 5–7 ranked startup idea cards, and a pre-build validation roadmap for the #1 idea. Reports are saved to `./market-research/` in the current working directory. Reusable output templates live in `skills/market-researcher/templates/`.

### `founder-mode`

First-principles operator thinking — answers business questions like a founder who has built and exited companies, not a generic advisor. Every response opens with "Here's what I'd actually do", commits to one decision (not a menu), names the trade-offs, and ends with a concrete next-48-hours action.

**Trigger phrases** (auto-activates on any of these):
- "founder mode" / "think like a founder"
- "stress test my idea / model / pitch"
- "my competitor is X — how do I beat them"
- "should I do A or B" (business decisions)
- "how do I make more money from this" / pricing & monetization questions
- "I'm hiring my first [role]"
- "be blunt about my business"

**Playbooks:**

| Playbook | What it does |
|----------|--------------|
| **Stress test** | Series A investor teardown — what breaks first, blind spots, what the top 3% do differently, fundability verdict |
| **Competitor gap** | Structural weaknesses your competitor *can't* fix, the positioning gap you can own, 3 moves ranked by speed |
| **Decision** | Kills the decision spiral — reversible vs one-way-door classification, hidden-objective check, a clear call with one flip-condition |
| **Monetization** | Hidden revenue audit — the leak with a number attached, 3 angles ranked by effort-to-return, a 2-week zero-rebuild test with a kill threshold |
| **Hiring** | A-player filter — role-specific questions that break rehearsed answers, the month-3 red flag and how to spot it in 30 minutes |

When invoked inside a project, it reads your specs, plans, and docs first and grounds the advice in your actual numbers and constraints.

## Installation

```bash
# Via Claude Code marketplace (GitHub)
/plugin marketplace add postowl-in/startup-skills
/plugin install startup-skills@startup-skills
```

## Example Usage

```
You: Research the AI writing tools niche — I want to find a gap to build into

Claude: [triggers market-researcher, runs 25 searches, returns full report
         with 6 ranked ideas and a validation roadmap for the top pick]
```

```
You: Stress test my idea: bulk email tool for small Indian agencies at ₹499/mo

Claude: [triggers founder-mode stress-test playbook — what breaks first,
         blind spots, top-3% behaviors, fundability verdict, 48-hour test]
```

```
You: Should I keep self-serve pricing or pivot to done-for-you at 30x the price?

Claude: [triggers founder-mode decision playbook — classifies reversibility,
         names what you're really optimizing for, makes the call]
```

## License

MIT — [Rohit Agarwal](https://github.com/rohitagr0310)
