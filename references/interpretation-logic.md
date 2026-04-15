# Interpretation Logic

This file defines how to turn raw signals into human-readable insight. The gap between data and insight is where this skill lives.

---

## The core interpretive shift

Most community health tools ask: **what happened?**
This skill asks: **what does it mean for the people inside this community?**

Every signal needs to pass through a human systems lens before it becomes an output. The question is never just "response time went up" — it's "whose time, toward whom, in what context, and what does that tell us about the humans involved?"

---

## Signal interpretation rules

### Rule 1: Confirm the trend
Before surfacing anything, confirm it's a trend, not a spike.
- Minimum 3 consecutive weeks of directional movement, OR
- A 4-week rolling average moving consistently in one direction
- Exception: severe single events (hostile incident, core contributor disappearing) warrant immediate flagging

### Rule 2: Find the person
After confirming a trend, ask: is a specific person or group the focal point?
- Contributor concentration signals almost always implicate 1–2 specific people
- Response time deterioration often implicates one overloaded maintainer
- Onboarding drop-off often implicates one friction point in the review process

When a person is implicated, the framing shifts from operational to relational. The recommendation changes accordingly — from "add a label" to "check in with this person."

### Rule 3: Assess severity
Three tiers:

**Tier 1 — Watch:** Directional change beginning. Not urgent. Include in weekly digest.
- First-time return rate starting to decline
- Channel activity becoming more transactional
- PR review latency creeping upward

**Tier 2 — Act:** Pattern established. Needs attention within 2 weeks.
- First-time return rate below 20%
- One person doing 70%+ of work across multiple functions
- Questions going unanswered 25%+ of the time
- Maintainer tone shift sustained over 3+ weeks

**Tier 3 — Urgent:** Acute risk. Flag immediately.
- Core contributor gone quiet with no explanation
- Hostile incident in public channels
- High-effort contribution ignored for 2+ weeks
- Maintainer showing multiple simultaneous burnout signals

### Rule 4: Check for compounding signals
Single signals are informative. Compounding signals are diagnostic.

Examples of dangerous combinations:
- Rising response time + declining message length from maintainer + contributor concentration high = **burnout imminent**
- No new contributors in 60 days + low welcome rate in Discord + onboarding docs outdated = **discovery and welcome failure**
- High PR review latency + first-time return rate low + no good-first-issue labels = **structural onboarding gap**

When signals compound, escalate the severity tier.

### Rule 5: Frame as friction
Convert every observation into a friction statement before writing the output.

| Raw observation | Friction framing |
|---|---|
| First-time return rate is 12% | New contributors are losing momentum before making a second contribution |
| Response time up 3x | Contributors are waiting longer than expected for acknowledgment |
| One person doing 80% of reviews | Review capacity is concentrated in a single point of failure |
| #help channel 40% unanswered | Members are asking questions that aren't getting through |
| Core contributor went quiet | A key relationship in the community may need attention |

Never use: failing, broken, dying, abandoned, toxic (unless describing a specific incident).
Always use: stuck, friction, concentrated, declining, at risk, slowing.

### Rule 6: Pair with action
Every output must end with one specific, low-effort action.

The action should be:
- Something the maintainer can do alone, within an hour
- A step toward addressing the friction, not a full solution
- Concrete enough that the maintainer doesn't have to think about what to do next

Good actions:
- "Add a comment to the top 3 unanswered PRs acknowledging them"
- "Pin a welcome message in #introductions explaining the three best ways to get involved"
- "Add a good-first-issue label to 5 issues this week"
- "Schedule a 20-minute check-in with [contributor name]"
- "Add one sentence to the contributing guide about what happens after a PR is submitted"

Bad actions:
- "Improve your onboarding process" (too vague)
- "Hire a community manager" (not actionable for a solo maintainer)
- "Redesign your contribution workflow" (too large)

---

## Reading maintainer burnout signals

This deserves special attention because it's the most consequential pattern and the hardest to see from the outside.

Early signals (Tier 1):
- Response length shortening gradually
- Less encouragement language in reviews ("looks good" replacing "great work on this, I have a few thoughts")
- Slower response to non-urgent issues
- Less activity in community channels

Mid-stage signals (Tier 2):
- Response time deteriorating across the board
- Template-style responses replacing personalized ones
- Fewer proactive posts (no release announcements, no call for contributors)
- Starting to miss their own stated response time commitments

Late signals (Tier 3 — act immediately):
- Going quiet without explanation
- Short, closed-ended responses to previously engaging contributors
- Direct expressions of frustration in public channels
- Contributor concentration ratio spiking (everyone waiting for the one person who's overwhelmed)

When you see Tier 2 or 3 maintainer burnout signals, the recommendation is always relational first: does this person have support? Do they have co-maintainers? Do they know it's okay to step back temporarily?

---

## What not to surface

Some things generate signals but should not be surfaced as insights:

- **Individual contributor activity levels** — whether a specific person is contributing more or less is their business, not a community health insight
- **Private channel or DM patterns** — never in scope
- **Speculation about reasons** — surface the pattern, not a theory about why
- **Comparisons to other projects** — "your response time is worse than react/vue/svelte" is not helpful
- **Vanity metrics moving downward** — fewer stars, fewer forks, lower traffic are not community health signals
