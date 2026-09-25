# Second Brain starter vault

A working [Obsidian](https://obsidian.md) vault, structured PARA, set up so that
[Claude Code](https://docs.claude.com/claude-code) can read it, file into it, and maintain it.

This is the template for **Build a Second Brain That Claude Can Actually Run**. It is empty of
anyone else's content. The structure and the rules are here; what goes in them is yours.

## Use it

You do not need a terminal or a GitHub account. Install Claude Desktop, Obsidian and whatever
service syncs your files (iCloud, OneDrive, Google Drive, Dropbox or Obsidian Sync). In Obsidian,
create an empty vault called `Second Brain` inside the synced location, then quit Obsidian. In
Claude Desktop, open the **Code** tab, choose **Local**, select that folder and paste this:

```
Set up my second brain in this folder. Do the work yourself rather than
telling me how, and check with me before anything you cannot undo.

1. Download the starter vault from
   https://github.com/icarleto/second-brain-starter/archive/refs/heads/main.zip
   and unpack its contents directly into this folder, not into a subfolder.
   Replace the .obsidian settings that are already here. Delete the zip.
2. This vault does not use git. Delete README.md, .gitignore and every
   .gitkeep file, and remove any instruction under .claude about committing
   or pushing.
3. Tell me in two lines what is now in the folder.
```

Then open the folder in Obsidian, install the Dataview and Calendar community plugins, and read
`START HERE.md`.

## What is in it

```
.claude/CLAUDE.md           the rules Claude reads at the start of every session
.claude/skills/vault-setup  an interview that fills those rules in by asking you
.obsidian/                  daily-note folder, date format, template path, preset
0. Dashboards               four starter views to try; delete any you stop opening
00. Inbox                   captured with nowhere to put it yet
1. Journal                  daily notes, and a Processed subfolder
2. Areas                    five starting areas, rename them to yours
3. Projects                 one setup project, delete it when done
4. Resources                reference material
5. Meta                     the daily template and the priority ranking
99. Archive                 finished and dead
```

## One thing that matters more than the rest

**Let the setup interview fill in `CLAUDE.md`.** Once the vault is open, tell Claude
`run the vault setup` and it will ask you what it needs and write its own instructions. That file
is the difference between an assistant that knows your situation and a chat window you re-brief
every session.

## Requires

- Obsidian, with the Dataview and Calendar community plugins
- Claude Code, and a Claude subscription
