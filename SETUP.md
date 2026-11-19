# Setup instructions for the AI agent

You are setting up the teach-me skill for a new learner. Do the steps in order.
Each step ends with a state you can check. Do not start teaching until step 6 passes.

## 1. Ask the learner four questions

Ask them together, in one message, and wait for the answers.

1. What are you learning toward? (a research question, a class, a paper, a new field)
2. What do you already know well, and where do explanations usually lose you?
   (notation, math, code, jargon, something else)
3. Which tools should worked examples use? (for example Python, R, a
   spreadsheet, none)
4. Where should the Obsidian vault live? Offer `~/Documents/Learning Vault` as
   the default. If they already have a vault, ask for its path and whether to
   put the files in a subfolder.

expect: you have four answers, or the learner has accepted the defaults.

## 2. Install the skill

Copy `SKILL.md` from this repository to the place your agent loads skills from.
For Claude Code that is `~/.claude/skills/teach-me/SKILL.md`. Also copy this
`SETUP.md` next to it. If a `teach-me` skill is already there, stop and ask the
learner before replacing it.

For an agent with no skill folder, add the contents of `SKILL.md` to the file
that agent reads for standing instructions.

expect: the skill file exists at the install path and its first line is `---`.

## 3. Create the vault

Copy everything inside `vault-template/` into the vault path from step 1. Never
overwrite a file that already exists there. The result is:

```
<vault>/
  Learner Profile.md
  Map.md
  Review Log.md
  Bits/
  Topics/
  attachments/
```

expect: all three files and all three folders exist at the vault path.

## 4. Fill in the Learner Profile

Write the four answers from step 1 into `Learner Profile.md`, including the
absolute vault path. Use the learner's own words. Do not add goals or background
they did not state.

expect: `Learner Profile.md` has no `<fill in>` text left.

## 5. Make the skill always available

Add one line to the agent's standing instructions (for Claude Code, the user's
`~/.claude/CLAUDE.md`), after showing the learner the line and getting a yes:

> When I am trying to learn or understand something, follow the teach-me skill.
> My vault is at `<absolute vault path>`.

expect: the line is present, or the learner declined and you told them to start
lessons by saying "teach me".

## 6. Run one bit as a test

Ask the learner for one thing they want to understand today and teach a single
bit under the rules in `SKILL.md`. When they answer correctly, save the bit,
create its topic note, link the topic from `Map.md`, and add its row to
`Review Log.md` with a gap of 1 day.

expect: `Bits/` holds one note, `Topics/` holds one note, `Map.md` links to it,
and `Review Log.md` has one row with tomorrow's date as the next review.

## 7. Tell the learner how to use it

In three lines: say "teach me X" or paste a paper to learn, say "quiz me" to be
tested on the vault, and open the vault folder in Obsidian (free, obsidian.md)
and use graph view to see how the topics connect.
