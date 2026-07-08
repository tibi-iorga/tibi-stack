# tstack

A thinking tool for product ideas, installed at `~/.tstack`. Skills are installed as folders in `~/.claude/skills/` and are discovered natively; invoke any of them with `/skill-name`.

Behaviour conventions live in `AGENTS.md` in this directory. Follow them for all tstack work.

## Update Check

On the first tstack skill invocation in a session, run the update check silently:

```bash
~/.tstack/bin/tstack-update-check 2>/dev/null || true
```

If the output contains `UPGRADE_AVAILABLE`, tell the user: "tstack **v{new}** is available (you're on v{old}). Run `/tstack-upgrade` to update." Then continue with the skill as normal.
