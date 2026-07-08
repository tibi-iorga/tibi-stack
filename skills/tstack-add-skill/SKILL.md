---
name: tstack-add-skill
description: "Adds a new skill to the tstack library. Drafts the SKILL.md following tstack conventions, saves it to the repo, updates the README and version, then pushes and reinstalls so the skill is available in every agent. Use when the user wants to create, add, or contribute a skill to tstack."
---

# /tstack-add-skill

Add a new skill to the tstack library. The library is the git repository; a skill only exists once it is committed there. Tool-specific skill folders (`~/.claude/skills/`, `~/.cursor/skills/`, `~/.agents/skills/`) are build output that setup overwrites, so never write the new skill there directly.

Use British English in all conversation with the user. No dashes; use commas, semicolons, or periods instead.

## Step 1: locate the repo

Work in the first of these that exists:

1. The current workspace, if it is a tstack checkout (look for `skills/` and `AGENTS.md` at the root).
2. `~/.tstack`.

If working in `~/.tstack`, run `git -C ~/.tstack pull` first so you branch from the latest version. If neither location exists, tell the user to install tstack first and stop.

## Step 2: understand the skill

Ask the user for whatever is missing. You need:

- What the skill does and what a finished run produces.
- When it should trigger; concrete phrases or situations.
- The category: Product and Strategy, Councils, Communications, Voices, or Maintenance.
- Any framework, structure, or voice it should follow.

Ask at most three questions in one message. Do not interrogate; propose defaults and let the user correct them.

## Step 3: draft the skill

Read two or three existing skills in `skills/` from the same category and match their shape. Then create `skills/<skill-name>/SKILL.md` with:

**Frontmatter**
- `name`: lowercase letters, numbers, and hyphens only; must match the folder name exactly; max 64 characters.
- `description`: one or two sentences covering what the skill does and when to use it. Agents choose skills by this field alone, so include trigger phrases and situations, not just a summary. Max 1024 characters.

**Body**
- Open with a one-paragraph statement of the job and the point of view the skill takes.
- Restate the house rules inline, since most agents load a skill without any other tstack context: British English; no dashes, use commas, semicolons, or periods instead; simple, direct language; senior product manager tone; never invent data, quotes, or metrics, flag assumptions instead.
- Give a numbered process, then an explicit output format in a fenced block if the skill produces a document.
- End with rules or constraints that keep the output honest.
- Keep the whole file under 500 lines. Skills must be opinionated; a skill that hedges is not worth invoking.

Show the draft to the user and iterate until they approve it.

## Step 4: register and ship

Once approved:

1. Add a row for the skill to the matching category table in `README.md`.
2. Bump the minor version in `VERSION` (for example 1.3.0 to 1.4.0) so existing installs get the upgrade notice.
3. Commit with a message like `Add /<skill-name> skill for <purpose>` and push to `main`.
4. Reinstall locally so the skill is immediately available: run `./setup` (macOS, Linux, Git Bash) or `./setup.ps1` (Windows PowerShell) from the repo root.

Report back: the skill name, where it was saved, the new version, and a reminder that other machines pick it up via `/tstack-upgrade`.

## Rules

- Never install the new skill only to a tool directory; the repo is the source of truth.
- Never push without the user having seen and approved the draft.
- If a skill with the same name already exists, show it and ask whether to revise it instead.
