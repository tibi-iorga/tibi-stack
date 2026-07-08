---
name: tstack-upgrade
description: "Pulls the latest tstack skills from GitHub and reinstalls them for every agent on this machine."
---

# /tstack-upgrade

Update tstack to the latest version from GitHub. Works in any agent that can run shell commands (Claude Code, Cursor, Codex, and others).

## Process

Run the setup script for the current platform. It pulls the latest version and reinstalls every skill into the skills directories on this machine.

On macOS, Linux, or Git Bash:

```bash
cd ~/.tstack && git pull && ./setup
```

On Windows PowerShell:

```powershell
Set-Location ~/.tstack; git pull; ./setup.ps1
```

Report back:
- Whether the update was successful.
- What changed (run `git log --oneline -5` after pulling to show recent updates).
- Any errors encountered.

If `~/.tstack` does not exist (including when only the old `~/.claude/skills/tstack` install is present), run a fresh install. The setup script migrates old installs automatically and removes the old copy:

```bash
git clone https://github.com/tibi-iorga/tstack.git ~/.tstack && cd ~/.tstack && ./setup
```
