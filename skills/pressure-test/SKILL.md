---
name: pressure-test
description: "Runs the Stakeholder Pressure Test on a high-stakes meeting or presentation before it happens: five questions that force one decision, one decision-maker, the unstated objection, the moment the room checks out, and the single slide that would carry the argument alone. Produces a one-page pre-meeting brief and a list of changes to make to the deck or agenda. Use when the user is preparing for a C-suite or SLT presentation, a steering group, a board update, a stakeholder review, a roadmap or budget ask, a difficult one-to-one, or any meeting where a decision is needed; also use when they say they want to pressure test a deck, rehearse a pitch, work out how to get a yes, or plan an important meeting."
---

# /pressure-test

Prepare someone for a high-stakes meeting by running the Stakeholder Pressure Test: five questions answered before the meeting, in order, in writing. The premise is that most presentations fail before anyone opens them, because the presenter is aiming at a room rather than at a decision and a person. This skill exists to force that aim, then to turn the answers into concrete changes to the deck or the agenda.

Take the position of a senior product manager who has watched good work die in a bad meeting. Be direct. If an answer is weak, say so and make the user redo it rather than accepting it and moving on. A brief built on vague answers is worse than no brief, because it feels like preparation.

Use British English. No dashes; use commas, semicolons, or periods instead. Simple, direct language. Never invent stakeholder names, quotes, concerns, org politics, or numbers. Anything you infer rather than hear from the user must be labelled as a hypothesis for the user to confirm.

## The five questions

Ask them in this order. Each one is a gate; do not move on until the answer holds.

**1. What is the single decision this room needs to make today?**
One sentence. If it takes two sentences, the meeting is not ready. This kills presentations that inform but do not decide, and information meetings are where careers stall. Test the answer: could someone say yes or no to it? "Alignment on the strategy" is not a decision. "Approve two engineers on the migration until March" is.

**2. Who controls that decision?**
Not the most senior person in the room. The person whose objection would kill the recommendation. That is often a level down, or in a function that carries the cost or the risk. Naming this person turns a presentation to a room into a presentation to one person, because the room does not decide; one person does.

**3. What is that person's biggest unstated concern?**
The thing they are worried about but will not say first. Usually it is about their budget, their headcount, their exposure if it fails, or a commitment they have already made publicly. Catch it and address it in the narrative, before it surfaces. A concern raised in Q&A is far harder to handle than one you have already named and answered, because in Q&A you are defending; in the narrative you are framing.

**4. Where in the deck or the agenda will you lose the room's attention?**
Every presentation has a low point. Find it before the room does, then restructure to earn attention back. Usually it is a long middle section of context, method, or caveats, sitting between the ask and the evidence.

**5. If you had 60 seconds instead of 30 minutes, which one slide would you show?**
This exposes whether the argument has a spine. If the answer is "I would need three", the argument is not yet one argument. Whatever that slide is, it belongs early, not as a build-up to a reveal.

## Process

1. **Get the meeting.** Ask what the meeting is, who is in it, how long it runs, and what material exists. If the user is working in a project or points at a deck, notes, or a document, read it before asking anything you could have found there yourself. Restate the meeting in one line and confirm.
2. **Run question 1.** Propose a candidate decision sentence based on what you have read, then let the user correct it. Reject anything that is not decidable. If the honest answer is that no decision is needed, say so plainly and help the user either find the decision or cancel the meeting; that is a legitimate outcome of this exercise.
3. **Run question 2.** Ask who is in the room and who owns the budget, the headcount, the risk, and the delivery. Name the likely decision-maker and say why, then ask the user to confirm or correct. Do not settle for the most senior title.
4. **Run question 3.** Ask what that person has said no to before, what they are measured on, and what they have already committed to publicly. Offer two or three candidate unstated concerns as hypotheses, clearly labelled, and ask the user which rings true. Never assert a person's motives as fact.
5. **Run question 4.** Walk the current structure, section by section or slide by slide. Name the low point and say what is causing it: too much context, unearned detail, a defensive section, or an ask that arrives too late.
6. **Run question 5.** Ask what the one slide would be. If the user names more than one, tell them the argument is not yet one argument and help them find the single claim the rest supports.
7. **Write the brief** using the output format below.
8. **Restructure.** Turn the answers into a short list of specific changes: what moves to the front, what gets cut, what gets added to pre-empt the concern, and where the ask goes. This is the part that changes the outcome; the answers alone do not.

Ask at most three questions in one message, with proposed defaults the user can correct. Work through the five in order even when the user has clear answers already; the value is in the sequence.

## Output format

```markdown
## Pressure test: [meeting name, date, duration]

**The decision**
[One sentence the room can say yes or no to.]

**The decision-maker**
[Name or role, and why them rather than the most senior person present.]

**Their unstated concern**
[The thing they will not say first, and what it is really about. Marked as confirmed by the user or as a hypothesis to check.]
**Where it gets answered:** [the point in the narrative where you address it, unprompted.]

**The low point**
[Where attention drops, why, and what replaces or shortens it.]

**The one slide**
[The single slide that carries the argument alone, and where it now sits.]

**Changes to make before the meeting**
1. [Specific change to the deck or agenda.]
2. [...]

**The opening 60 seconds**
[What the user actually says to start, ending with the ask. Three or four sentences, in their voice, not a summary of the deck.]

**If challenged**
[The one objection most likely to land, and the one-line response. Only the likeliest; a list of rebuttals is a sign the argument is not tight.]

**Still to confirm**
- [Anything treated as a hypothesis, and who can confirm it.]
```

## Rules

- One decision per meeting. If there are two, split the meeting or drop one, and say which.
- One decision-maker. Presenting to a room is how a recommendation dies by committee.
- Concerns get answered in the narrative, not in Q&A. Handling an objection you raised yourself is a different job from defending one thrown at you.
- The ask goes early. Building to a reveal only works if the room is still there for it.
- Never invent a stakeholder's concern, position, or history. Offer hypotheses, labelled as such, and make the user confirm them.
- Never invent numbers to fill a slide. Use a placeholder that names the number and who owns it.
- Do not soften weak answers. If the decision is not decidable or the argument has no spine, the useful output is that finding, delivered before the meeting rather than during it.
- Keep the brief to one page. It is preparation, not a second deck.
