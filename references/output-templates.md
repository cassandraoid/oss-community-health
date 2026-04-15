# Output Templates

This file defines how to structure, frame, and deliver insights. The format matters as much as the content — a good insight delivered badly won't be acted on.

---

## Core output structure

Every insight follows this four-part structure:

```
**[Signal name] — [Tier indicator]**
Source: [GitHub / Community / GitHub + Community]

[What the signals show — 2–3 sentences, friction-framed]

**Why it matters:** [Human systems implication — 1–2 sentences]

**Suggested action:** [One concrete next step]

**Watch for:** [What to monitor over the next 4 weeks]
```

---

## Tier indicators

Use these consistently so maintainers learn the visual language:

- 🟡 **Watch** — Directional change beginning, monitor
- 🟠 **Act** — Pattern established, needs attention within 2 weeks  
- 🔴 **Urgent** — Acute risk, flag immediately
- 🟢 **Positive** — Health signal improving, worth acknowledging

---

## Sample outputs by signal type

### Onboarding friction (Tier 2)

```
🟠 First-time contributors stalling at first review
Source: GitHub

Over the past 6 weeks, 8 of 11 first-time contributors submitted a PR but received 
no response within 7 days. Of those, 7 have not returned. The drop-off is happening 
at the review stage, not the submission stage — people are getting in the door but 
losing momentum waiting to hear back.

**Why it matters:** The first contribution experience sets the tone for everything 
that follows. A week of silence reads as indifference, even when it isn't.

**Suggested action:** Add a simple acknowledgment comment to new contributor PRs 
within 48 hours — even "Thanks for this, reviewing soon" significantly reduces 
drop-off. Consider assigning a designated first-PR reviewer for one month as a test.

**Watch for:** First-time return rate in the next 30 days.
```

### Contributor concentration (Tier 2)

```
🟠 Review capacity concentrated in a single point of failure
Source: GitHub

Over the past 8 weeks, one contributor has closed 68% of issues, reviewed 74% of 
PRs, and responded to 80% of new comments. This concentration is a sustainability 
risk — if this person steps back for any reason, response times will collapse 
across the board.

**Why it matters:** This is also an early burnout signal. People carrying 
disproportionate load often don't realize how unsustainable it is until they 
hit a wall.

**Suggested action:** Explicitly invite 2–3 active contributors into a reviewer 
role this week. A direct message saying "I've noticed you've been active and 
engaged — would you be open to taking on some review responsibilities?" is usually 
well received.

**Watch for:** Whether the concentration ratio shifts over the next 30 days.
```

### Maintainer burnout — cross-platform (Tier 3)

```
🔴 Maintainer showing compounding load signals across GitHub and Discord
Source: GitHub + Community

Over the past 6 weeks: average response length in GitHub reviews has shortened 
by 40%, response time has increased from 2 days to 6 days, and activity in the 
Discord #general channel has dropped from daily to twice weekly. These signals 
together — not individually — suggest early-to-mid stage burnout.

**Why it matters:** This pattern, left unaddressed, typically precedes a 
maintainer going quiet entirely. The project doesn't need more from this person 
right now — it needs to reduce what it's taking from them.

**Suggested action:** Before anything operational, consider a direct and private 
check-in — not about the project, about the person. "I wanted to check in — how 
are you actually doing?" opens more than any process change will.

**Watch for:** Whether any of the three signals stabilize or continue declining.
```

### Community vitality — positive (Tier 1)

```
🟢 Non-transactional channel energy increasing
Source: Community

Activity in #showcase and #ideas has increased 40% over the past 4 weeks. 
Members are sharing work in progress, asking speculative questions, and having 
conversations that go beyond immediate needs. This kind of energy is a leading 
indicator of community vitality — invisible in GitHub data entirely.

**Why it matters:** Communities with active non-transactional spaces retain 
contributors longer. People stay for the belonging, not just the code.

**Suggested action:** Amplify this momentum — a monthly showcase thread or 
a low-lift "what are you building?" prompt in #general can accelerate what's 
already happening organically.

**Watch for:** Whether engagement in these channels sustains or was a one-time spike.
```

---

## Tone guide

| Not this | But this |
|---|---|
| Your community is failing | New contributors are losing momentum at onboarding |
| This is a serious problem | This pattern is worth addressing in the next two weeks |
| You need to fix your onboarding | One change to your review response time could meaningfully improve retention |
| This person is burning out | This person is showing patterns consistent with high load |
| Your Discord is dead | Non-transactional channel activity has declined significantly |

**Voice:** Direct, warm, non-alarmist. The maintainer is a person doing their best under real constraints. Every output should feel like it's coming from a thoughtful advisor who respects their capacity, not a dashboard flagging errors.

**Length:** Keep each insight to under 150 words. Maintainers are busy. If you can't say it in 150 words, you haven't synthesized it enough.

**Frequency:** Surface maximum 3 insights per weekly digest. More than 3 creates overwhelm and reduces the chance any of them get acted on.
