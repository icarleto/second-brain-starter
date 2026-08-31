# Second Brain starter vault

A working [Obsidian](https://obsidian.md) vault, structured PARA, set up so that
[Claude Code](https://docs.claude.com/claude-code) can read it, file into it, and maintain it.

This is the template that accompanies **Build a Second Brain That Claude Can Actually Run**. It is
empty of anyone else's content. The structure, the rules and the dashboards are here; what goes in
them is yours.

## Use it

Do not clone this repository. Make your own from it, so your vault is private and its history is
yours:

```bash
gh repo create my-vault --template icarleto/second-brain-starter --private --clone
```

Then open that folder in Obsidian with **Open folder as vault**, and read `START HERE.md`.

## What is in it

```
.claude/CLAUDE.md    the rules Claude reads at the start of every session
0. Dashboards        four live views: home, areas, projects, journal
00. Inbox            captured with nowhere to put it yet
1. Journal           daily notes, and a Processed subfolder
2. Areas             five starting areas, rename them to yours
3. Projects          one setup project, delete it when done
4. Resources         reference material
5. Meta              the daily template and the priority view
99. Archive          finished and dead
```

## Two things that matter more than the rest

**Keep this folder out of OneDrive, iCloud Drive, Dropbox and Google Drive.** Cloud sync and git
both replicate the same folder and neither can see the other. They fight, quietly, and the way it
surfaces is a file silently reverting or a commit recording a stale copy. Put the vault somewhere
like `C:\Vault` or `~/Vault` and let git handle versions and other machines.

**Fill in `.claude/CLAUDE.md` properly.** It is the difference between an assistant that knows your
situation and a chat window you have to re-brief every session. Two honest paragraphs there change
the quality of everything downstream.

## Requires

- Obsidian, with the Dataview and Calendar community plugins
- Claude Code, and a Claude subscription
- Git, and the GitHub CLI for the command above
