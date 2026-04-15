# Contributing to OSS Community Health Agent

This skill is built on the belief that the hardest problems in open source are human, not technical. Contributions that make it better at reading, interpreting, and acting on those human signals are welcome.

---

## Current contribution priorities

### 1. Discord bot integration (most wanted)

The skill currently works as an advisory layer — it helps maintainers think through community health problems. The next major milestone is making it proactive: a Discord bot that reads public channel signals and feeds them automatically to the skill.

**What it needs to do:**
- Join a Discord server with read-only permissions on public channels only
- Track the signals defined in `references/community-platform-signals.md`:
  - New member welcome rate
  - Time-to-first-response in help channels
  - Channel activity distribution (transactional vs non-transactional)
  - Response concentration (are the same 2–3 people answering everything?)
  - Sentiment patterns over time
- Aggregate into a structured weekly snapshot — never individual messages, only patterns
- Output in a format Claude can interpret using the skill

**Consent requirements are non-negotiable.** Any bot implementation must follow the framework in `references/consent-framework.md` — community notification, public channels only, aggregate patterns only, opt-out mechanism.

**Stack:** Node.js or Python preferred. Discord.js or discord.py are both fine.

If you're interested in building this, open an issue tagged `discord-bot` before starting so we can align on the data schema.

---

### 2. Slack integration

Same pattern as the Discord bot but for Slack workspaces. Signals are defined in `references/community-platform-signals.md`. Same consent requirements apply.

---

### 3. Signal framework improvements

The signals in `references/signal-framework.md` are a starting point, not a complete picture. If you maintain an open source project and notice patterns the framework misses — or gets wrong — open an issue or submit a PR with proposed additions.

Especially useful: real-world calibration of the healthy ranges. The current benchmarks are based on observed patterns but more data makes them better.

---

### 4. Output template refinements

The tone and framing in `references/output-templates.md` matter enormously. If you've used the skill and found language that lands better with real maintainers — or language that doesn't — open an issue. Small wording changes have outsized impact on whether an insight actually gets acted on.

---

### 5. New platform support

Community platforms beyond Discord and Slack worth adding:
- GitHub Discussions (partially covered by repo data already)
- Discourse forums
- Matrix / Element
- Reddit communities

If your community lives somewhere not covered, open an issue describing the platform and what signals would be meaningful there.

---

## How to contribute

1. Open an issue before starting significant work — alignment first saves everyone time
2. Fork the repo and create a branch
3. Make your changes
4. Submit a pull request with a clear description of what changed and why
5. Reference the relevant signal, interpretation, or consent framework in your PR description

---

## What this project is not looking for

- Vanity metric tracking (stars, forks, follower counts)
- Individual contributor surveillance or profiling
- Features that require private channel access
- Anything that violates the consent framework in `references/consent-framework.md`

---

## Philosophy

This skill was designed from the outside in — starting with the human systems failures that make open source unsustainable, and working backward to the signals that predict them.

Contributions should follow the same logic: start with the human problem, then design the signal or feature that addresses it. A contribution that makes one maintainer's Monday morning easier is worth more than a technically impressive feature that nobody uses.

---

## Questions

Open an issue. Tag it `question`. No question is too basic — if you're confused about something, the documentation probably needs to be clearer.
