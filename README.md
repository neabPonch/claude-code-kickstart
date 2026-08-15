# Claude Code Kickstart

A guided, hands-on introduction to [Claude Code](https://code.claude.com) — an AI
agent that works in your repository: it reads your code, runs your commands, and
verifies its own work. This plugin teaches you to use it **well**: eight short
interactive lessons, in your own project, with a running emphasis on not wasting
tokens (your organization pays for them).

## Install (3 steps, ~3 minutes)

**1. Install Claude Code** (skip if you have it — check with `claude --version`):

```bash
# macOS / Linux / WSL
curl -fsSL https://claude.ai/install.sh | bash
```

```powershell
# Windows PowerShell
irm https://claude.ai/install.ps1 | iex
```

**2. Sign in.** Open a terminal **in a project you work on** and run:

```bash
claude
```

On first run it walks you through login — use your **company Claude account**
(Console/SSO) when prompted. Ask your team lead if you're not sure which option
applies.

**3. Install this plugin.** Inside the Claude Code session, type:

```
/plugin marketplace add <your-github-username>/claude-code-kickstart
/plugin install kickstart@claude-code-kickstart
```

<!-- PUBLISH NOTE: replace <your-github-username> above (and in PRESENTATION.md)
     with the actual GitHub owner before making this repo public. -->

Then start the tour:

```
/kickstart:tour
```

## What you get

| Command | What it does |
|---|---|
| `/kickstart:tour` | The guided tour: 8 lessons × ~5 minutes, in your own project. Stop anytime; it resumes where you left off. |
| `/kickstart:coach` | Ask anytime "am I using this efficiently?" — audits your current session and gives concrete fixes. |
| `/kickstart:cheatsheet` | The quick-reference card: session commands, modes, and the five cost commandments. |

The tour covers: working with an agent instead of a chatbot, `CLAUDE.md`, plan mode,
**context & cost hygiene** (the unskippable lesson), verification-driven requests,
model/effort right-sizing, checkpoints & git, and where to go next.

## FAQ

**Do I need a project?** A real one you know is best — the tour adapts to it. If you
don't have one handy, the tour offers to generate a tiny practice project.

**How much will the tour itself cost?** The plugin is static text — installed but
idle it adds ~240 tokens to a session (measured with `claude plugin details
kickstart`), and the tour's instructions are ~3.6k tokens loaded only when you invoke
it. A full eight-lesson run is a normal interactive session — typically
on the order of a few hundred thousand tokens (single-digit dollars) depending on
your project and how deep you go. Lesson 4 alone, applied for a week, pays that back.

**Can I stop mid-tour?** Yes — progress is saved to `.kickstart-progress.md` in your
project. Run `/kickstart:tour` again anytime to resume.

**Something's broken.** `claude doctor` diagnoses install issues; see the
[troubleshooting docs](https://code.claude.com/docs/en/troubleshooting). For plugin
issues: `/plugin` shows what's installed and enabled.

**Where do I learn more?** [RESOURCES.md](RESOURCES.md) — a short, ordered reading
path into the official docs.
