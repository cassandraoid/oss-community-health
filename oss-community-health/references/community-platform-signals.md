# Community Platform Signals

This file defines signals readable from Discord, Slack, and other community platforms. This integration is **optional** — it requires explicit opt-in and setup by the maintainer.

See `consent-framework.md` for required consent and privacy practices before enabling.

---

## Why community platform signals matter

GitHub tells you what people do. Community platforms tell you how people feel.

Someone can be closing PRs at a normal rate while privately expressing frustration in a support channel. A new contributor can submit a great first PR and then quietly disappear because nobody welcomed them in the community chat. These signals are invisible in repository data alone.

---

## Discord signals

### New member welcome rate
**What it is:** Percentage of new server members who receive a welcome message from an existing member within 24 hours of joining.
**Healthy range:** 60%+ for active communities.
**What it means when low:** New members arrive to silence. This is the community equivalent of a PR that gets no response — it signals that showing up doesn't matter.

### Time-to-first-response in help channels
**What it is:** Time between a question posted in #help or equivalent channel and first substantive response.
**Healthy range:** Under 4 hours during active periods.
**What it means when rising:** Questions are going unanswered. Members start to feel the community isn't functional for getting help, which drives them to alternatives (or away entirely).

### Channel activity distribution
**What it is:** Spread of activity across channel types — transactional (#help, #bugs) vs. non-transactional (#general, #ideas, #showcase, #random).
**Healthy pattern:** Non-transactional channels have meaningful activity — people sharing what they're building, discussing ideas, casual conversation.
**What it means when skewed toward transactional only:** The community has become purely functional. People come to get help and leave. The social fabric that creates belonging and retention is absent.
**Note:** Activity in #showcase and #ideas is a leading indicator of community vitality not visible in GitHub at all.

### Sentiment shift over time
**What it is:** Aggregate tone of community conversation — are messages getting shorter, more clipped, more frustrated, or less exploratory over time?
**How to read it:** Compare rolling 4-week windows. Shortening message length and decreasing expressiveness often precede community decline.
**Weight:** Medium. Directional change over 8+ weeks is meaningful. Short-term shifts are noise.

### Response concentration
**What it is:** Percentage of responses in help channels coming from the same small group of people.
**Healthy range:** Top 3 responders doing less than 60% of total responses.
**What it means when high:** Same bus factor risk as GitHub — a small group is carrying the community support load. These people burn out, step back, and the community loses its responsiveness overnight.

---

## Slack signals

### Unanswered question rate
**What it is:** Percentage of questions posted in public channels that receive no response within 24 hours.
**Healthy range:** Under 15%.
**What it means when high:** The community isn't functioning as a support resource. Members learn quickly that asking doesn't work, and stop engaging.

### Thread engagement depth
**What it is:** Average number of replies in threaded conversations.
**Healthy pattern:** Substantive threads with 3+ replies indicating genuine discussion.
**What it means when declining:** Conversations are becoming shallower — quick answers replacing discussion, or questions getting no follow-up.

### Contributor overlap with GitHub
**What it is:** Percentage of active GitHub contributors who are also active in Slack.
**What it means:** High overlap suggests an integrated community. Low overlap suggests two separate populations — code contributors who don't engage socially, and community members who don't contribute code. Both are fine, but worth understanding.

---

## Cross-platform signal correlation

The most powerful insights come from reading GitHub and community platforms together.

| GitHub signal | Community signal | Combined insight |
|---|---|---|
| Active contributor | Going quiet in Discord | Early disengagement signal — visible weeks before it shows in commit data |
| Good first PR submitted | No welcome in community channel | Strong predictor of non-return even if PR gets merged |
| Maintainer response time rising | Tone shortening in channels | Burnout confirmation across both surfaces |
| Same 2 people reviewing everything | Same 2 people answering everything | Bus factor risk confirmed — it's systemic, not just technical |
| No new GitHub contributors in 60 days | #introductions channel quiet | Community discovery problem, not just a code contribution problem |
| PR hostility spike | Negative sentiment in #general | Culture problem, not an isolated incident |

---

## Platforms supported

| Platform | Signal access | Notes |
|---|---|---|
| Discord | Public channels only | Via Discord bot with read-only permissions |
| Slack | Public channels only | Via Slack app with message read scope |
| Discourse | Public threads | Via Discourse API |
| GitHub Discussions | Public discussions | Already in repo data layer |
| Matrix | Public rooms | Via Matrix client API |

Private channels, DMs, and threads are never in scope regardless of technical access.
