# OSS Community Health Agent

An agent skill for Claude and other AI agents that helps open source maintainers understand the human health of their community, not just its activity metrics.

**Core thesis:** GitHub tells you what people do. Community platforms tell you how people feel. You need both to understand what's actually happening inside your community.

---

## Install

```
npx skills add cassandra/oss-community-health
```

---

## What this skill does

When installed, this skill gives Claude deep expertise in reading, interpreting, and acting on open source community health signals — across both repository data and community platforms (Discord, Slack, forums).

It is not a dashboard. It is an interpretation layer. It takes signals and turns them into human-readable insight, framed for the person most capable of acting on it: the maintainer.

**Signal coverage:**
- Contributor retention and first-time contributor experience
- Maintainer burnout patterns (early, mid, and late stage)
- Bus factor risk and contributor concentration
- Onboarding friction points
- Community platform health (optional integration)
- Cross-platform signal correlation

**Interpretation principles:**
- Trend over snapshot — 4–8 week directional change, not single-week spikes
- People before numbers — always connect data to human reality
- Friction, not failure — frame as where momentum is stuck, not what's broken
- Transparency without surveillance — aggregate patterns, never individual attribution
- Action, not just observation — every insight paired with one concrete next step

---

## Relationship to CHAOSS / Augur

This skill does not compete with [CHAOSS](https://chaoss.community/), [Augur](https://github.com/chaoss/augur), or GrimoireLab. Those projects are excellent data infrastructure — they collect and visualize metrics.

This skill is the interpretation layer on top. Where they output dashboards, this outputs language, judgment, and recommendations framed for a maintainer, not a data scientist.

---

## Usage examples

Once installed, the skill triggers automatically on relevant queries:

> "My first-time contributor return rate feels low. How do I figure out where people are dropping off?"

> "I'm worried about burning out. I'm the only one reviewing PRs and answering Discord questions. What are the signals I should watch?"

> "Someone submitted a really substantial PR two weeks ago and I haven't had time to review it. What should I do?"

> "Our Discord has been quieter lately. Is that a health signal or just normal ebb and flow?"

> "I want to set up community health monitoring for my project. Where do I start?"

> "How do I think about bus factor in an open source community — not just in the codebase?"

> "I want to enable Discord monitoring for community health signals. What are the consent requirements?"

---

## Reference framework

The skill loads contextually from six reference files:

| File | Contents |
|---|---|
| `references/signal-framework.md` | GitHub signals — definitions, healthy ranges, interpretation guidance |
| `references/community-platform-signals.md` | Discord/Slack/forum signals, cross-platform correlation |
| `references/interpretation-logic.md` | How to read patterns, severity tiers, burnout signal guide |
| `references/output-templates.md` | Output structure, tone guide, sample insights |
| `references/consent-framework.md` | Privacy requirements for community platform integration |

---

## Community platform integration

Discord, Slack, and forum integration is **optional**. It requires explicit opt-in and community notification.

The integration reads aggregate patterns from public channels only. No individual messages are stored or attributed. See `references/consent-framework.md` for full requirements.

---

## Design philosophy

This skill was designed from the outside in — starting with the human systems failures that make open source unsustainable, and working backward to the signals that predict them.

The hardest problems in open source aren't technical. They're human: invisible labor, concentrated load, unwelcoming first experiences, maintainers burning out quietly. None of those show up cleanly in a GitHub activity graph. This skill is an attempt to make them visible — and actionable — before they become crises.

Built on the insight that contribution is compound: every person who has a good first experience and returns is an asset that grows. Every person who leaves after a bad first experience is a loss that compounds too.

---

## Contributing

This skill is itself open source. Contributions to the signal framework, interpretation logic, and output templates are welcome.

If you use this skill and notice patterns it misses or insights it gets wrong — open an issue. The goal is for this to get better with use.

---

## About

Designed by [Cassandra](https://github.com/cassandraoid) — human systems designer, DevRel strategist, and open source contributor. Built on years of thinking about contribution economics, invisible labor, and what makes communities sustain.

---

## License

MIT
