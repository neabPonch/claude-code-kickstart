# Claude Code Kickstart

A guided, hands-on introduction to [Claude Code](https://code.claude.com) — an AI
agent that works in your repository: it reads your code, runs your commands, and
verifies its own work. This plugin teaches you to use it **well**: eight short
interactive lessons, in your own project, with a running emphasis on not wasting
tokens (your organization pays for them).

## Install (4 steps, ~5 minutes)

Every command below is typed into a **terminal**. Mac: press `Cmd+Space`, type
`Terminal`, press Enter. Windows: Start menu → type `PowerShell` → Enter.

**1. Install Claude Code** — copy-paste ONE of these (match your machine) and
press Enter:

```bash
# macOS / Linux / WSL
curl -fsSL https://claude.ai/install.sh | bash
```

```powershell
# Windows PowerShell
irm https://claude.ai/install.ps1 | iex
```

✅ **Check it worked:** close the terminal, open a new one, type `claude --version`.
You should see a version number. If you see "command not found", opening a fresh
terminal window usually fixes it; if not, run `claude doctor` or see the
[setup docs](https://code.claude.com/docs/en/setup).

**2. Go to a project.** In the terminal, `cd` into a code project you actually work
on — the tour teaches best on your real code:

```bash
cd path/to/your/project
```

(No project handy? Any empty folder works — the tour will offer to generate a tiny
practice project.)

**3. Start Claude Code and sign in.** Type:

```bash
claude
```

First run opens your browser to log in — choose your **company Claude account**
(Console/SSO) when prompted; ask your team lead if you're unsure which option is
yours. ✅ **Check it worked:** you're back in the terminal looking at a chat-style
input box.

**4. Install this plugin.** You're now *inside* Claude Code — everything from here
is typed into that input box at the bottom, like a chat message. Type each line and
press Enter (approve the confirmation prompts):

```
/plugin marketplace add neabPonch/claude-code-kickstart
```

```
/plugin install kickstart@claude-code-kickstart
```

✅ **Check it worked:** type `/kickstart` — the input box should suggest the
kickstart commands. Then start the tour:

```
/kickstart:tour
```

From here the tour drives: one step at a time, it tells you exactly what to type
and what you should see. You can stop anytime and resume later.

## What you get

| Command | What it does |
|---|---|
| `/kickstart:tour` | **Part 1 — foundations** (start here): agent vs chatbot, CLAUDE.md, plan mode, **context & cost hygiene** (the unskippable lesson), verification, model right-sizing, checkpoints. |
| `/kickstart:tour2` | **Part 2 — daily driver**: CLAUDE.md hierarchy, memory, permission policy, authoring your first skill, branch/PR workflow, subagents, multi-session work. |
| `/kickstart:tour3` | **Part 3 — power tier**: hooks, custom subagents, building your own plugin, MCP, headless automation, CI, team cost governance. |
| `/kickstart:coach` | Ask anytime "am I using this efficiently?" — audits your current session and gives concrete fixes. |
| `/kickstart:cheatsheet` | The quick-reference card: session commands, modes, and the five cost commandments. |

Each part is ~8 lessons × ~5 minutes, scripted step-by-step in your own project;
stop anytime, resume anytime. [CURRICULUM.md](CURRICULUM.md) maps every Claude Code
capability to the lesson that teaches it.

## FAQ

**I'm not an engineer — is this for me?** Yes. The tour starts with a short intake
(your role, how comfortable you are with code, the terminal, and git) and adapts:
analysts get data-and-SQL-flavored examples, operators get file-and-report
automation, and nothing assumes prior terminal or git knowledge.

**Do I need a project?** A real one you know is best — the tour adapts to it. If you
don't have one handy, the tour generates a practice project matched to your role
(a mini-app, a data analysis, or a file-automation task).

**How much will the tour itself cost?** The plugin is static text — installed but
idle it adds ~440 tokens to a session (measured with `claude plugin details
kickstart`), and each tour part's instructions are ~4–6k tokens loaded only when
you invoke it. A full eight-lesson run is a normal interactive session — typically
on the order of a few hundred thousand tokens (single-digit dollars) depending on
your project and how deep you go. Lesson 4 alone, applied for a week, pays that back.

**Can I stop mid-tour?** Yes — progress is saved to `.kickstart-progress.md` in your
project. Run `/kickstart:tour` again anytime to resume.

**Something's broken.** `claude doctor` diagnoses install issues; see the
[troubleshooting docs](https://code.claude.com/docs/en/troubleshooting). For plugin
issues: `/plugin` shows what's installed and enabled.

**Where do I learn more?** [RESOURCES.md](RESOURCES.md) — a short, ordered reading
path into the official docs.
