# Signal Framework — GitHub Repository Signals

This file defines the signals the agent reads from GitHub, what they mean, and how to weight them.

---

## Quantitative signals

### Time-to-first-response on new issues
**What it is:** Time between issue opened and first comment from anyone (not just maintainers).
**Healthy range:** Under 48 hours for active projects, under 1 week for smaller ones.
**What it means when rising:** Contributors feel unheard. First-time contributors are most sensitive to this — silence reads as rejection.
**Weight:** High. One of the strongest predictors of contributor return rate.

### First-time contributor return rate
**What it is:** Percentage of contributors who make a second contribution within 60 days of their first.
**Healthy range:** 30–50% for active projects.
**What it means when low:** Something in the first-contribution experience is creating friction. Could be slow review, no acknowledgment, confusing feedback, or feeling unwelcome.
**Weight:** Highest. This is the most direct measure of whether your community is growing or leaking.

### Contributor concentration ratio
**What it is:** Percentage of total work (issues closed, PRs reviewed, comments made) done by the top 2–3 contributors.
**Healthy range:** Top 3 doing less than 60% of total work.
**What it means when high:** Bus factor risk. If those people step back, the project stalls. Also a leading indicator of maintainer burnout — the people doing everything are usually the people burning out.
**Weight:** High for sustainability assessment.

### PR review latency
**What it is:** Time from PR opened to first review from a maintainer.
**Healthy range:** Under 1 week for active projects.
**What it means when rising:** Contributors are waiting. Long waits demotivate contribution, especially for first-timers who submitted something they're proud of.
**Weight:** Medium-high. Important but context-dependent (project size, maintainer bandwidth).

### Issue close rate vs open rate
**What it is:** Ratio of issues closed to issues opened over a rolling 4-week period.
**Healthy range:** Close rate at or above open rate (ratio ≥ 1.0).
**What it means when declining:** Issue debt is accumulating. Maintainers are falling behind, which creates visible signs of project neglect.
**Weight:** Medium. Use as a secondary indicator, not a primary one.

---

## Qualitative signals

### Sentiment drift in issue and PR threads
**What to look for:** Shift in emotional tone over time — more terse responses, more frustrated language, less encouragement, shorter acknowledgments.
**How to read it:** Compare tone from 3 months ago vs. now. Increasing terseness from maintainers often indicates overwhelm. Increasing frustration from contributors often indicates unmet expectations.
**Weight:** High when combined with quantitative signals.

### Language patterns indicating friction
**What to look for:** Phrases like "I've mentioned this before," "still no response," "is this project still maintained?" These are explicit signals of contributor frustration.
**Also watch for:** Contributor-to-contributor conflict in threads, repeated questions about the same undocumented things, new contributors apologizing excessively (sign of an unwelcoming culture).
**Weight:** Medium. Individual instances are noise; patterns across multiple threads are signal.

### Tone shift in maintainer responses
**What to look for:** Decreasing response length, more closed-ended replies, less encouragement on contributions, increasing use of template-style responses.
**What it means:** A maintainer showing these patterns is often in early burnout. They're still showing up but with diminishing capacity.
**Weight:** High. Act on this early — it's much easier to prevent burnout than recover from it.

### First-time contributor experience quality
**What to look for:** Did the contributor receive a welcoming response? Was their PR reviewed with encouragement? Were they pointed to contributing guidelines?
**Healthy pattern:** First-time contributors receive acknowledgment within 48 hours, clear feedback, and at least one encouraging comment.
**Weight:** Highest for retention prediction.

---

## Structural signals

### Non-code contribution visibility
**What to look for:** Are documentation updates, issue triage, community support, and onboarding work being acknowledged and attributed?
**Why it matters:** These contributions are disproportionately done by underrepresented contributors. When they're invisible, those contributors feel invisible too.
**How to assess:** Check whether non-code PRs receive the same quality of review as code PRs. Check whether triage work appears in contributor acknowledgments.

### Bus factor assessment
**What to look for:** Single points of failure in contributor roles. Is there only one person who reviews security PRs? Only one person who responds to Discord questions?
**Healthy pattern:** At least 2–3 people capable of performing each critical function.
**Risk signal:** Any critical function where one person has done 80%+ of the work in the last 90 days.

### Onboarding drop-off points
**What to look for:** Where in the contribution journey do new contributors disappear? Common drop-off points:
- After submitting a first issue (no acknowledgment)
- After submitting a first PR (no review within 7 days)
- After receiving first review feedback (unclear or discouraging)
- After first contribution merged (no "what's next" guidance)

### Knowledge concentration
**What to look for:** Critical project knowledge that only lives in one person's head. Indicators: recurring questions about the same undocumented things, contributors tagging the same person repeatedly, CODEOWNERS file with single ownership across most paths.

---

## Risk signals

### Extended period without new contributors
**Threshold:** No new first-time contributors in 60+ days for a project with regular activity.
**What it means:** The project has stopped attracting new blood. Could indicate discoverability issues, reputation concerns, or an unwelcoming first impression.

### Core contributor going quiet
**What to look for:** A previously highly active contributor whose activity has dropped 70%+ over 4 weeks without explanation.
**How to respond:** Do not surface this publicly. Flag it privately to the maintainer as a relationship worth checking in on.

### Spike in issue hostility
**What to look for:** Sudden increase in aggressive, dismissive, or hostile language in issues — either from contributors toward maintainers, or maintainers toward contributors.
**Weight:** Urgent. Toxic incidents have an outsized effect on community perception and contributor retention.

### High-effort contributions with no acknowledgment
**What to look for:** Large PRs, detailed issue write-ups, or substantial documentation contributions that received no response within 2 weeks.
**What it means:** The contributor invested significant effort and heard nothing. This is one of the most reliable predictors of a contributor never returning.
