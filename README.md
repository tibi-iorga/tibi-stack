# tstack

A thinking tool for building ideas. Slash commands for the kind of reasoning that usually only comes from experience.

---

## What it is

Good intuition is what is left over after you have thought through the same kind of problem many times. That is what experience actually is. tstack lets you run that kind of thinking on demand, against whatever idea is in front of you, instead of waiting for the reps to accumulate.

Each skill is a structured way of thinking, packaged as an [Agent Skill](https://agentskills.io) that works in whatever coding agent you already use: [Claude Code](https://claude.ai/code), [Cursor](https://cursor.com), OpenAI Codex, GitHub Copilot, and anything else that implements the open standard. You type `/sowhat` and get the So What ladder run five levels deep on whatever you paste in. You type `/carmack` and get a Carmack-voice critique of your draft. You type `/mentor-review` and get the same idea reviewed by six different operators in sequence. The skills are opinionated. They are not trying to be neutral.

---

## What it solves

Four failure modes when you are thinking through an idea on your own. Each one has a few skills aimed at it.

**Shallow takes.** You stop at the first plausible answer instead of pushing deeper.
Run `/sowhat`, `/office-hours`, `/ai-moat`.

**Single perspective.** You only see from your own seat. You miss what an engineer, a CEO, a designer, or a customer would say.
Run `/mentor-review`, `/pm-review`, `/strategy-review`, `/design-council`.

**Vague writing.** Your draft hedges where it should commit, and commits where it should hedge.
Run `/carmack`, `/exec-email`, `/release-notes`.

**Unstructured ideas.** You have a feeling, not a memo. Nothing concrete for anyone, including you, to react to.
Run `/1pager`, `/strategy-memo`, `/prd`, `/instrumentation`.

**Borrowed understanding.** You can repeat the argument but you could not defend it under questioning.
Run `/socratic-quiz`.

---

## Setup

**Option 1: paste this into your agent**

Open Claude Code, Cursor, Codex, or any agent that can run shell commands, and paste the following message into the chat:

```
I want to install tstack from https://github.com/tibi-iorga/tstack. Please run the setup script:

git clone https://github.com/tibi-iorga/tstack.git ~/.tstack && cd ~/.tstack && ./setup

On Windows PowerShell, run ./setup.ps1 instead of ./setup.

Then confirm how many skills were installed.
```

The agent will clone the repo and run setup for you.

**Option 2: run it yourself**

macOS, Linux, or Git Bash:

```bash
git clone https://github.com/tibi-iorga/tstack.git ~/.tstack && cd ~/.tstack && ./setup
```

Windows PowerShell:

```powershell
git clone https://github.com/tibi-iorga/tstack.git "$HOME/.tstack"; Set-Location "$HOME/.tstack"; ./setup.ps1
```

Requirements: Git and an agent that supports [Agent Skills](https://agentskills.io) (Claude Code, Cursor 2.4+, OpenAI Codex, GitHub Copilot, Gemini CLI).

The setup script clones the repo to `~/.tstack`, then installs each skill as `<skills-dir>/<skill-name>/SKILL.md` in `~/.agents/skills/` (the cross-tool location) plus the tool-specific directories it finds on your machine (`~/.claude/skills/`, `~/.codex/skills/`). If you have an older tstack install at `~/.claude/skills/tstack`, setup migrates it and removes the old copy so skills are not registered twice. Restart your agent after setup.

---

## Skills

### Product and Strategy

| Skill | What it does |
|---|---|
| `/office-hours` | YC-style reality check on an idea. Brutal honesty on demand, market, and whether it is worth pursuing. |
| `/1pager` | Creates a structured one-pager from context: problem, hypothesis, goals, scope, risks. |
| `/prd` | Asks clarifying questions then generates a full PRD saved to /tasks. |
| `/strategy-memo` | Generates a concise strategy memo: problem, vision, principles, goals, solution, non-priorities. |
| `/sowhat` | Runs the So What framework five times in sequence, forcing progressively deeper insight from any observation. |
| `/instrumentation` | Walks through building a metric tree: business outcomes, product outcomes, leading indicators. |
| `/ai-moat` | Stress tests an idea's defensibility when AI compresses software costs to zero, then recommends pivots toward durable moats. |
| `/ooda` | Decomposes a human role or workflow into OODA sub-functions, classifies which AI absorbs today and which stay irreducibly human, then points to where durable value accrues. |
| `/uk-medical-device-check` | Checks whether a software feature would be classified as a UK medical device under MHRA / UK MDR 2002, and how to stay out of scope. |

### Councils

Multi-perspective reviews where different lenses run in sequence to surface blind spots.

| Skill | What it does |
|---|---|
| `/strategy-review` | Stress-tests a strategy from three angles: devil's advocate, SWOT, then bear/bull/base scenarios. |
| `/pm-review` | Reviews a PRD from three seats: engineering feasibility, executive business value, user researcher empathy. |
| `/mentor-review` | Gets POV and recommendations from Marc Andreessen, Andy Grove, Jack Welch, Clayton Christensen, Brian Chesky (Airbnb), and Travis Kalanick (Uber). |
| `/design-council` | Generates fundamentally different design approaches to the same problem (different interaction paradigms, mental models, design patterns), then combs the chosen direction for consistency issues. |

### Communications

| Skill | What it does |
|---|---|
| `/release-notes` | Generates honest, customer-facing release notes answering the seven key questions. |
| `/impact-story` | Turns survey data and usage metrics into a polished internal impact story for leadership. |
| `/exec-email` | Drafts a strategic executive email: context, insights, recommendation, one clear ask. |
| `/money-stories` | Turns a proposal or roadmap item into a Mironov-style money story for SLT: three numbers, two known and one estimated, multiplied into an order-of-magnitude outcome. |
| `/pressure-test` | Runs the Stakeholder Pressure Test on a meeting before it happens: one decision, one decision-maker, the unstated objection, the low point, the one slide. Produces a pre-meeting brief and the changes to make. |

### Voices

Single-voice reviews and rewrites in the style of a specific operator or writer.

| Skill | What it does |
|---|---|
| `/carmack` | Carmack-voice critique. Either edits a draft for clarity, honesty, and concreteness, or reviews a concept through a first-principles, what-do-you-actually-know lens. |

### Learning

| Skill | What it does |
|---|---|
| `/socratic-quiz` | Guides you to understanding one question at a time instead of explaining. Adapts to your level, never hands over the answer, ends with what you demonstrated and what to explore next. |

### Maintenance

| Skill | What it does |
|---|---|
| `/tstack-upgrade` | Pulls the latest skills from GitHub. |
| `/tstack-add-skill` | Adds a new skill to the library: drafts it to convention, updates the README and version, pushes, and reinstalls everywhere. |

---

## License

MIT. See [LICENSE](LICENSE). Use it, fork it, change it, ship your own version.

## Credits

`/socratic-quiz` is adapted from the skill of the same name in [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools), MIT licensed, Copyright (c) 2025 Prasad Chalasani.
