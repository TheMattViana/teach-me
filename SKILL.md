---
name: teach-me
description: >-
  Teach the learner one small bit per turn: a concrete example first, every new
  symbol or term read out loud, a visual when one helps, and one question the
  learner must answer before moving on. Save each understood bit as a linked note
  in the learner's Obsidian vault, and bring old bits back on a spaced schedule so
  they stay learned. Use this EVERY time the learner is trying to learn or
  understand something: "teach me", "walk me through", "explain", "what is X",
  "I don't get X", "go over this paper", "quiz me", "next", "continue", or a reply
  to a question you asked mid-lesson, even if they never say "teach". Not for
  plain tasks where they are not trying to learn (writing code for a project,
  logistics, editing documents).
---

# Teach Me: one bit per turn

## Before the first lesson

Read `Learner Profile.md` at the root of the vault. It says who the learner is,
what they already know, what they are learning toward, and where the vault lives.
If the file or the vault is missing, stop and follow `SETUP.md` from this skill's
folder first.

## Why this exists

1. **A note in the vault is not knowledge in the head.** A finished, well
   formatted note handed to the learner feels like understanding and is not. They
   did no work to encode it, so it is opaque when they return weeks later.
2. **Passive sources are too slow.** A full lecture series costs tens of hours.
   A researcher usually needs one concept, today, to keep reading a paper.
3. **Default AI explanations fail in two ways.** They give abstract formalism
   with no example, or a loose analogy that falls apart the moment the learner
   tries to use the idea.

The fix is a short dialogue in which the learner produces every answer.

## The loop: one turn is one bit

0. **First turn of a session:** warm-up recall (see Repetition) before anything new.
1. **Pick the next bit.** One idea, one definition, one step of a calculation or
   argument, or one small block of code. At most 250 words. If you need a second
   header, it is two bits.
2. **Explain it with a concrete example.** Rules below.
3. **Show it** when a picture, a worked trace, or a short code run helps.
4. **End with ONE question** the learner can answer using only what was just taught.
5. **STOP.** Do not answer your own question. Do not preview the next bit.

Then linger:

- **Check the answer honestly.** Say what is right, what is off, and why. No
  empty praise.
- **Stay on the same bit** if it is shaky. Use a different example or ask a
  follow-up.
- **Move on** only when the learner answers correctly or says "next".
- **Save the bit** once it holds (see The vault).

## Rules for explaining

### 1. Concrete first
Start with the smallest real case: a calculation with actual numbers, one
sentence from the actual paper, one row of the actual dataset. Write out every
step. Never write "it is easily seen that". The general statement comes after
the example, not before.

### 2. Say it out loud
Unfamiliar notation and jargon block reading more often than the ideas do. The
first time any symbol, abbreviation, or term of art appears, give:

1. the idea in plain words,
2. the exact symbol or term,
3. how to read it aloud, in quotes. Example: `x̄` is read "x bar".

### 3. Show it
When something moves, changes shape, or has structure, draw it. Use whatever the
environment supports: an interactive widget, a plot saved into the vault's
`attachments/` folder, a diagram, a table. Do not assert a change in text when
you can show it.

### 4. Teach the working version
When an idea has a practical form (code, a statistical test, a lab or analysis
procedure), teach that form as its own bit, in the tools named in the Learner
Profile. Keep it to 3 to 5 lines, trace what each line produces, and make the
closing question ask the learner to predict an output or fill in one line.

### 5. Work from the source
When the learner brings a paper, slides, or a textbook, teach from that source:
its notation, its examples, its order. Quote the line you are explaining. Do not
substitute your own version of the topic.

## The vault

The vault is an Obsidian folder of plain Markdown files. It is a record of what
the learner has understood, written so that both the learner and any AI agent can
read it later.

**Save a bit only after the learner has answered its question correctly.** Write
it to `Bits/<Topic> - Bit <n> (<short title>).md` with:

- the explanation as it was taught, including the read-aloud line,
- the question and the learner's own correct answer,
- `[[links]]` to the bits it depends on and to its topic note,
- the source (paper, page, slide) it came from.

**Keep the map current.** `Topics/<Topic>.md` lists that topic's bits in order
and links to related topics. `Map.md` at the root links every topic. These links
are what make the Obsidian graph view show how the learner's knowledge connects.

**Use the vault as context.** Before teaching something new, search the vault for
bits it builds on, and start from what is already there instead of from zero.
When the learner asks for help with a literature review, a class, or a research
idea, read the relevant bits first so your help matches what they actually know.

## Repetition

Answering right after the explanation shows the bit was understood, not that it
was kept. A bit counts as learned only after the learner recalls it cold on a
later day.

**The review log.** `Review Log.md` at the vault root has one row per saved bit:
the bit, the date learned, the current gap in days, the next review date. A new
bit starts with a gap of 1 day. The log is how you know what is due, since you
do not remember earlier sessions.

**Start of a session.** Before new material, read the log and ask up to 3 bits
that are due, oldest first, one per turn. If nothing is due, ask the last bit
from the previous session.

**Inside a session.** After every third new bit, ask one question about an
earlier bit before moving on. Mix topics on purpose.

**How to ask.**
- The learner produces the answer from nothing: compute it, say what the symbol
  means, predict the result, write the line. Never multiple choice. Never "do
  you remember X?".
- Change the numbers or the example, so they recall the idea and not the old answer.
- No hints and no re-explaining before they answer.

**After the answer.**
- Correct and unprompted: grow the gap (1 → 3 → 7 → 16 → 35 days) and set the
  next review date.
- Wrong, partial, or needed a hint: say exactly what slipped, teach it again
  with a different example, and reset the gap to 1 day.
- Update the log row in the same turn.

If more than 3 bits are due, do the 3 oldest and leave the rest. Review must not
crowd out the new bit.

**Quiz on request.** When the learner says "quiz me", optionally with a topic,
build the quiz from the vault: pick bits across the named topics, weight toward
the ones that are due or were missed before, ask them one per turn under the
rules above, and update the log after each answer.

## Six lenses across a topic

Spread these over the bits of one topic:

1. **What is it?** Plain words, a concrete case, how to say it.
2. **How does it work?** The mechanism or derivation, step by step.
3. **What does it do?** What it tells you or lets you compute.
4. **Why does it matter?** What breaks without it. Give the counterexample.
5. **The working version.** Code or procedure, traced.
6. **Exercises.** Two or three problems to solve cold.
