# Consent and Privacy Framework

This file defines the consent and privacy requirements for the community platform integration. This section applies **only when the optional Discord/Slack/forum integration is enabled.**

GitHub repository data is public by default and requires no additional consent. Community platform integration has a higher bar.

---

## Why this matters

People treat Discord and Slack differently than GitHub. Even in public servers, members have a reasonable expectation that their messages are conversations — not data inputs to an analysis system. Violating this expectation, even unintentionally, damages the trust that open source communities run on.

The "transparency without surveillance" principle is non-negotiable here.

---

## Requirements — tiered

### Required (non-negotiable)

**1. Community notification**
The community must be informed that the agent is running. At minimum: a pinned message or channel description noting that aggregate patterns are monitored for community health purposes.

Suggested language:
> "This community uses an open source health agent to help maintainers understand community patterns and prevent burnout. It reads aggregate signals from public channels only — no individual messages are stored or attributed. [Link to repo]"

**2. Aggregate patterns only**
The agent reads patterns, not content. No individual's messages are stored, surfaced, or attributed in outputs. The maintainer should never receive an insight like "User X seems frustrated" — only "help channel response rate has declined."

**3. Public channels only**
Only public channels are in scope. Private channels, DMs, and any channel marked private are never read, regardless of bot permissions granted. This must be enforced at the configuration level — not just by policy.

---

### Recommended

**4. Contributing guide transparency**
Add a brief note to the project's contributing guidelines explaining what the agent monitors and why — framed as a tool for the maintainer's sustainability, not surveillance of contributors.

**5. Opt-out mechanism**
Allow community members to opt out of aggregate analysis by using a command (e.g., `/health-optout`) or reacting to a pinned message.

---

### Optional

**6. Public health dashboard**
Some communities choose to make the health signals visible to all members — not just maintainers. This can build trust and shared ownership of community health. Consider it if your community culture supports transparency.

---

## What the agent never does

- Reads or stores private channel content
- Attributes community platform insights to named individuals
- Monitors DMs or direct messages of any kind
- Builds behavioral profiles of individual community members
- Shares community platform data with any third party
- Uses community data to evaluate individual contributors

---

## Setup checklist

Before enabling community platform integration:

- [ ] Pinned notification posted in main community channel
- [ ] Bot permissions scoped to public channels only
- [ ] Contributing guide updated with one-sentence note
- [ ] Opt-out mechanism implemented (if using recommended tier)
- [ ] Maintainer has reviewed this consent framework

---

## Data handling

Community platform data is:
- Processed in real time for pattern detection
- Not stored at the individual message level
- Retained as aggregate weekly snapshots only
- Deletable by the maintainer at any time

The open source nature of this agent means the data handling logic is fully auditable. Maintainers and community members can inspect exactly what is being read and how.
