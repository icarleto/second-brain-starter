---
name: vault-setup
description: Run the first-time setup interview for this vault. Asks the user about themselves, their areas and how they want to be spoken to, then fills in the blanks in .claude/CLAUDE.md, renames the Area notes, and updates anything that referenced the old names. Use when the user asks to set up the vault, says they are new here, or when CLAUDE.md still contains FILL IN markers.
---

# Vault setup interview

Fill in this vault's `CLAUDE.md` by **asking**, not by guessing. When this finishes there should be
no `FILL IN` markers anywhere and the Areas should be the user's own.

## Before you start

Check `.claude/CLAUDE.md` for `FILL IN`. If there are none, say so and ask whether they want to
revise what is there instead of running the whole interview again.

## How to run the interview

**Ask a few questions at a time, not all of them at once, and not one at a time.** A wall of
fifteen questions gets abandoned; one question per message is tedious. Three or four related ones
per turn is right.

**Take what they give you and move on.** If somebody answers a question briefly, that is their
answer. Do not push for more detail on personal subjects. You can always ask again later, and a
setup interview that feels like an interrogation is one they will not finish.

**Write as you go, not at the end.** After each group of answers, edit `CLAUDE.md`. If they walk
away halfway through, what they already told you should be saved.

## What to ask

### 1. Who they are

- Their name, and what they do for work.
- What they are actually trying to build or change right now. The real answer, not a job title.
- Whether money is tight, comfortable, or in debt. Say plainly that this changes the advice you
  give, because it does, and that is why you are asking.
- Who else is affected by their decisions. Partner, children, business partners.
- Anything they are trying to quit, start, or hold themselves to.

The last two are the ones people skip. **Ask them once, accept a short answer or a refusal, and do
not ask twice.** Note in `CLAUDE.md` what they chose not to say, so a later session knows it was
asked rather than forgotten.

### 2. How they want to be spoken to

Offer concrete options rather than asking them to describe a tone in the abstract, which nobody
can do cold. Something like:

- Direct and unsentimental, or warmer and more encouraging?
- Should you push back when you think they are wrong, or assume they have already decided?
- Short answers by default, or the reasoning as well?

Write their answer as instructions to yourself, in the second person, not as adjectives. "Tell me
when you think I am wrong, even if I did not ask" is usable. "Be direct" is not.

### 3. Their Areas

The vault ships with five: Family, Professional, Home, Discipline, Creation. Show them the list
and explain what each currently covers, then ask what to rename, merge, or replace.

**Push back gently if they want more than six.** The list being closed is what makes filing
decidable, and an open list has no filing rule at all. Explain that when something does not fit it
is nearly always a Project inside an existing Area. If they still want a sixth or seventh after
hearing that, it is their vault. Do it and say you have noted the reasoning.

### 4. Their first projects

Ask what they are actually working on right now. Two or three is plenty.

For each one, use the Areas versus Projects test from `CLAUDE.md`: what would make them stop
working on it specifically? Nothing means it belongs in an Area log. A deliverable or a date means
it is a Project. "It starts running without me" also means it is a Project, with a process finish
line.

**This is the most useful part of the interview**, because it teaches the distinction on their own
work rather than on an example. Do it out loud: say which shape you think each one is and why, and
let them correct you.

## What to change

1. **`.claude/CLAUDE.md`** — replace every `FILL IN` block with their answers. Delete the bracketed
   prompts. Keep the structure and every rule that is already there; you are filling blanks, not
   rewriting the file.
2. **`2. Areas/*.md`** — rename the files to their areas, update the `# Heading` and the `area:`
   frontmatter inside each, and fill in the one-line description of what belongs there. Delete the
   "Rename or replace this area" paragraph once it is theirs.
3. **`0. Dashboards/2. Areas Dashboard`** — the Untriaged Tasks query lists the five default tag
   names. Update it to match their actual areas, or that view silently reports nothing useful.
4. **`3. Projects/`** — create a note for each project they named, using the same structure as
   `Set Up This Vault`.
5. **`5. Meta/Priority Ranking`** — add a row per project, in the order they say matters. Row order
   is the ranking; there is no number column.

**Step 3 is the one that gets forgotten.** Renaming an Area without updating that query leaves a
dashboard that looks fine and reports nothing, which is worse than one that is visibly broken.

## When you are done

Commit the changes. Then tell them, briefly:

- Which Areas they now have
- Which projects were created
- That the next thing to do is write today's daily note badly and ask you to process it

Do not summarise the interview back to them. They were there.

## What not to do

- **Do not invent answers for anything they skipped.** A blank you leave marked is honest; a
  plausible guess about somebody's marriage or money is not, and it will sit in your system prompt
  being quietly wrong for months.
- **Do not delete or rewrite the hard stops** in `CLAUDE.md`, or any of the working rules. They are
  not personalisation.
- **Do not ask about anything you do not need.** This interview exists to fill specific blanks. If
  you find yourself asking a question that does not map to one, stop.
