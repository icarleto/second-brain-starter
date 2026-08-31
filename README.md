# Second Brain starter vault

A working [Obsidian](https://obsidian.md) vault, structured PARA, set up so that
[Claude Code](https://docs.claude.com/claude-code) can read it, file into it, and maintain it.

This is the template for **Build a Second Brain That Claude Can Actually Run**. It is empty of
anyone else's content. The structure, the rules and the dashboards are here; what goes in them is
yours.

## Use it

**You do not need to run these commands yourself.** Get Claude Code running in the Claude desktop
app, make sure you have a GitHub account, and paste it this:

```
Set up my second brain vault for me. Run the commands yourself rather than
telling me to, and check with me before anything you cannot undo.

1. Check whether git and the GitHub CLI are installed on this machine, and
   install whichever is missing.
2. Sign me in to GitHub with `gh auth login`, and tell me what to click.
3. Create a private repository called my-vault from the template
   icarleto/second-brain-starter, and clone it to C:\Vault on Windows or
   ~/Vault on macOS. It must NOT go inside OneDrive, iCloud Drive, Dropbox
   or Google Drive.
4. Tell me which folder to open in Obsidian when you are done.
```

Then open that folder in Obsidian with **Open folder as vault**, install the Dataview and Calendar
community plugins, and read `START HERE.md`.

If you would rather run it yourself, the one command is:

```bash
gh repo create my-vault --template icarleto/second-brain-starter --private --clone
```

## What is in it

```
.claude/CLAUDE.md           the rules Claude reads at the start of every session
.claude/skills/vault-setup  an interview that fills those rules in by asking you
.obsidian/                  daily-note folder, date format, template path, preset
0. Dashboards               four live views: home, areas, projects, journal
00. Inbox                   captured with nowhere to put it yet
1. Journal                  daily notes, and a Processed subfolder
2. Areas                    five starting areas, rename them to yours
3. Projects                 one setup project, delete it when done
4. Resources                reference material
5. Meta                     the daily template and the priority ranking
99. Archive                 finished and dead
```

## Two things that matter more than the rest

**Keep this folder out of OneDrive, iCloud Drive, Dropbox and Google Drive.** Cloud sync and git
both replicate the same folder and neither can see the other. They fight, quietly, and it surfaces
as a file silently reverting or a commit recording a stale copy over newer work. Put the vault
somewhere like `C:\Vault` or `~/Vault` and let git handle versions and other machines.

**Let the setup interview fill in `CLAUDE.md`.** Once the vault is open, tell Claude
`run the vault setup` and it will ask you what it needs and write its own instructions. That file
is the difference between an assistant that knows your situation and a chat window you re-brief
every session.

## Requires

- Obsidian, with the Dataview and Calendar community plugins
- Claude Code, and a Claude subscription
- A GitHub account
