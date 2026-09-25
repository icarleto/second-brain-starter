---
name: vault-setup
description: Run the first-time setup interview for this vault. Asks the user about themselves, their areas and how they want to be spoken to, then fills in the blanks in .claude/CLAUDE.md, renames the Area notes, and updates anything that referenced the old names. Use when the user asks to set up the vault, says they are new here, or when CLAUDE.md still contains FILL IN markers.
---

# Vault setup interview

Fill in this vault's `CLAUDE.md` by **asking**, not by guessing. When this finishes there should be
no `FILL IN` markers left in `CLAUDE.md` and the Areas should be the user's own. The "Current state"
blank in each Area note stays: the user fills that in next, one Area at a time, by asking you to
interview them about it.

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
- What they want to call you. A name is optional, and "no name" is a fine answer. It fills the
  assistant-name blank in `CLAUDE.md`.
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

### 4. What they are working on

Ask once what they are working on right now, and say plainly that "nothing yet" is a good answer.
Projects are not phase one. They come later, out of what the user writes in their journal over the
next few weeks.

Do not create project notes or add rows to `5. Meta/Priority Ranking` during setup. If they name
something, add it as a dated entry in the Notes/Log of the Area it belongs to, and tell them that if
it keeps coming up in their journal it will be worth making a project.

## What to change

1. **`.claude/CLAUDE.md`**: replace every `FILL IN` block with their answers, including the
   assistant name. Delete the bracketed prompts. Keep the structure and every rule that is already
   there; you are filling blanks, not rewriting the file. The worked task-tagging example under
   "Task tagging" uses the default `#home` and `#creation` tags: change them to two of their own
   Area tags so the example points at something real.
2. **`2. Areas/*.md`**: rename the files to their areas, update the `# Heading` and the `area:`
   frontmatter inside each, and fill in the one-line description of what belongs there. Update the
   area name in the Projects query and the tag in the Open tasks query and its caption. Delete the
   "Rename or replace this area" paragraph once it is theirs. Leave "Current state" blank.
3. **`0. Dashboards/2. Areas Dashboard`**: the Untriaged Tasks query lists the five default tag
   names. Update it to match their actual areas, or that view silently reports nothing useful.
4. **Anything else that names an old Area.** `3. Projects/Set Up This Vault` carries
   `area: "[[Creation]]"` and `#creation` tags, and `5. Meta/Priority Ranking` has a Creation row.
   If Creation was renamed or replaced, point those at one of their Areas.

**Steps 3 and 4 are the ones that get forgotten.** Renaming an Area without updating the queries
that name it leaves a view that looks fine and reports nothing, which is worse than one that is
visibly broken.

## When you are done

Tell them, briefly:

- Which Areas they now have
- That the next thing to do is describe each Area's current state, one at a time, by asking you to
  interview them about it
- And to write today's daily note badly, then ask you to process it

Do not summarise the interview back to them. They were there.

## What not to do

- **Do not invent answers for anything they skipped.** A blank you leave marked is honest; a
  plausible guess about somebody's marriage or money is not, and it will sit in your system prompt
  being quietly wrong for months.
- **Do not delete or rewrite the hard stops** in `CLAUDE.md`, or any of the working rules. They are
  not personalisation.
- **Do not ask about anything you do not need.** This interview exists to fill specific blanks. If
  you find yourself asking a question that does not map to one, stop.
