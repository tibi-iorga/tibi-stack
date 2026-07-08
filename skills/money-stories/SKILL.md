---
name: money-stories
description: "Turns a product proposal, roadmap item, or initiative into a money story for senior leadership, following Rich Mironov's Money Stories framework: three numbers, two known and one estimated, multiplied into an order-of-magnitude business outcome. Use when a PM is pitching to SLT or executives, defending a roadmap, writing a business case, justifying an initiative, or asks how to communicate the value of product work in the language of money."
---

# /money-stories

Help a product manager turn a piece of product work into a money story: a short, executive-ready explanation of how the work makes or protects money. Based on Rich Mironov's "Money Stories: Communicating the Value of Product Work". The premise: product managers talk about features, executives talk about revenue. Do not bring a backlog to a gunfight; bring one story about money.

Use British English. No dashes; use commas, semicolons, or periods instead. Simple, direct language. Senior product manager tone. Never invent data or metrics; every known number must come from the user or their documents, and the estimated number must be labelled as a guess.

## The framework

A money story has **no more than three numbers: two you know, one you estimate.** Connect them with multiplication only. The goal is not accuracy; it is order of magnitude. Count the digits: is this a five-figure idea or a seven-figure idea? Within a factor of six is good enough to make a prioritisation argument.

Every story fits one of these types. Pick one; do not blend them.

1. **Internal cost savings.** Hours or spend removed. (People affected x time saved x cost of time.)
2. **Upsell or expansion revenue.** Installed base x upcharge x estimated take rate.
3. **New customer acquisition.** Deals lost to a gap x average sale price x share we believe would really have bought.
4. **Volume or usage growth.** Transactions x value per transaction x estimated uplift.
5. **Retention or churn reduction.** Customers at risk x annual value x share we believe the work saves.
6. **Market entry or expansion.** Reachable segment x expected price x estimated penetration.

Frame the finished story in one of two sentence shapes:

- "We have [problem]. If we [solution], then we will [result]."
- "We can [derive benefit] by [focus area to fix], which can [result]."

## Process

1. **Review the context.** If the user is working in a project, read the relevant material: the PRD, roadmap item, proposal, or whatever they point at. If they only give a sentence, work from that. Restate the piece of work in one line and confirm you have understood it.
2. **Identify the audience and the decision.** Which SLT members, and what do they need to decide: fund it, keep it on the roadmap, stop interrupting the team, or drop something else.
3. **Pick the story type.** Say which of the six types fits and why. If two could fit, pick the one closest to how this business actually makes money and say what you rejected.
4. **Find the three numbers.** Identify the two known numbers and where the user can get them (finance, sales ops, analytics). Identify the one number that must be estimated and propose a range for the user to react to, clearly labelled as a guess. If the user does not have the known numbers to hand, still build the full story, using bracketed placeholders that name the number and its likely owner, for example [number of active customers, from sales ops]. Never substitute an invented value for a placeholder.
5. **Do the maths.** Multiply, show the working, and give the result as a range, not a point. State the digit count plainly. Only do this once real numbers are in; if placeholders remain, leave the formula unresolved and skip the digit count rather than compute on guesses.
6. **Draft the story** using the output format below.
7. **Stress-test it.** Name the assumption most likely to be challenged in the room and how the user should respond when it is.

Ask clarifying questions whenever the work, the audience, or the numbers are unclear; at most three at a time, with proposed defaults the user can correct.

## Output format

```markdown
## Money story: [name of the work]

**The story**
[One sentence in one of the two frames, with the range in it, or placeholders if numbers are still missing. This is the line to say in the meeting.]

**Story type:** [one of the six]
**Audience:** [who, and the decision needed]

**The maths**
[known number] x [known number] x [estimated number, labelled as estimate] = [range]
Source of known numbers: [where each comes from]
This is a [N]-digit story.

**Saying it to SLT**
[Two to four sentences expanding the story in the language of money. No feature lists, no process talk, no story points. End with the ask.]

**Most likely challenge**
[The assumption that will be attacked, and the one-line response.]

**To firm up before the meeting**
- [Number or fact to verify, and who owns it.]
```

## Rules

- Three numbers maximum, multiplication only. If the story needs a fourth number, it is two stories; pick one.
- Two numbers known, one estimated. Never present the estimate as a fact.
- Placeholders are fine; fake numbers are not. A placeholder names the missing number and who owns it. A result computed from placeholders is a fake number.
- Ranges, not points. Spurious precision destroys credibility with executives.
- One story per piece of work. A list of stories is a backlog wearing a costume.
- No product or process language in the final story: no sprints, story points, refactors, or tech debt. Translate everything into money or time.
- Bring humility. The story exists to start an argument about three visible inputs, not to win it in advance. Consensus beats being the smartest person in the room.
