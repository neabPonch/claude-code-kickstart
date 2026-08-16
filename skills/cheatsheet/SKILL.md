---
name: cheatsheet
description: Print the Claude Code quick-reference card — session commands, modes, and cost habits. Use when the user asks what commands exist, how to do something basic in Claude Code, or wants the kickstart reference.
---

Print the reference card below verbatim (adjusting nothing but formatting for the
terminal), then stop. If the user asked about one specific command, print only the
relevant section plus one sentence of guidance.

## Claude Code quick reference — the kickstart card

**Session hygiene (the money commands)**

| Command | What it does | When |
|---|---|---|
| `/clear` | Wipe the session, start fresh | Finished a task; two failed attempts at the same fix |
| `/compact` | Summarize history to free context (steer it: `/compact keep the test failures`) | Mid-task, long session, history still matters |
| `/rewind` | Roll code + conversation back to a checkpoint | Last approach was a dead end |
| `/context` | Show what's filling the context window | Session feels slow or off — look before you clear |
| `/usage` | Show what this session has spent | Curiosity and accountability |

**Fitting the tool to the task**

| Command / key | What it does |
|---|---|
| **Shift+Tab** | Cycle permission modes — plan mode = explore & propose before touching anything |
| ⚠ auto-accept / auto mode | Only for mechanical work on a **clean branch** with a **verification target**. While learning: manually approve, always. |
| `/model` | Switch model (big model for gnarly work, cheap for mechanical) |
| `/effort` | Reasoning depth: low for boilerplate, high for hard problems |
| `/init` | Generate the project's CLAUDE.md (then trim it — every line is a per-session tax) |
| `/memory` | Edit CLAUDE.md / memory files |
| `/resume` | Reopen an earlier conversation |

**Kickstart**

| Command | What it does |
|---|---|
| `/kickstart:tour` | Part 1 — foundations (start here) |
| `/kickstart:tour2` | Part 2 — daily driver: skills, permissions, PRs, subagents |
| `/kickstart:tour3` | Part 3 — power tier: hooks, plugins, MCP, headless, CI |
| `/kickstart:coach` | Audit this session for token waste |
| `/plugin` | Manage plugins & marketplaces |

**The five cost commandments**

1. Point, don't paste — the agent reads files; stop shipping code through the chat box.
2. Plan before you build — redirecting a plan costs cents; redirecting code costs the code twice.
3. Give every request a "done when" — verified beats plausible.
4. Finished a task → `/clear` — five clean sessions beat one marathon.
5. Right-size the model and effort — save the big gun for problems worthy of it.
