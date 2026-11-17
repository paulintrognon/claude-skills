---
name: walkthrough
description: Walk the user step by step through a complex topic until they can make an informed decision. Use when the user wants to validate a decision Claude took, choose between non-obvious options with stakes, or understand a hard problem; when another skill needs the user to decide with full understanding; or propose it before taking a complex, hard-to-reverse decision alone.
---

The user decides; you make sure they decide informed. Everything stays in the conversation: the caller (user or skill) owns what happens next.

Write noob-friendly throughout: short sentences, plain words, every technical term defined the first time it appears, nothing assumed known.

## 1. Frame

One message:
- the mode: **validate** (a decision you took), **choose** (between options), or **understand** (a problem);
- the question in one sentence, and the stakes: what it costs if wrong, how reversible it is;
- for validate and choose: each option in one line, and your recommendation with its main reason;
- the plan: the concepts the decision rests on, in order.

Stop. Done when the user confirms the frame or corrects it.

## 2. Concepts

One concept per message, in the plan's order; split a heavy one into parts. Each: what it is, why it weighs on the decision, one concrete example (the user's real code when there is some, else simplified pseudocode), and a diagram when structure or flow matters. End with one line asking if it is clear, then stop.

Move to the next concept only once the user explicitly says they understood it. A question, a doubt or a reply about something else means not yet: answer it, then ask again.

- Not clear: explain again from another angle or with another example, not the same words.
- The user already knows it: skip, on their word.

Done when the user has explicitly approved or skipped every concept of the plan.

## 3. Decisions and problems

Raise each one right after the concepts it relies on, not all at the end. One per message, then stop: the user challenges it.

- **Choose**: a table of options × criteria (cost, risk, reversibility, what it blocks later), your pick, and what would change your mind.
- **Validate**: the alternatives you rejected and why, and the weakest point of your choice.
- **Understand**: the causes ranked by likelihood, and how to check each.

Verify facts in the code or docs; mark what is an assumption. When the user shows you wrong, drop or revise your point. Done when the user has settled each one.

## 4. Hand back

One line per decision taken or problem understood, plus what is still open. Then return to the caller.

## Diagrams

Mermaid, rendered in a visual widget when the client has one; otherwise an ASCII diagram or a table. Seven nodes at most: split a bigger one.
