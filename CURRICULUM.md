# Coverage map — what Claude Code can do, and where this plugin teaches it

Three guided walkthroughs, each ~8 lessons × ~5 minutes, all scripted step-by-step
in your own project, all resumable (`.kickstart-progress.md`):

| Part | Command | Who it's for |
|---|---|---|
| 1 — Foundations | `/kickstart:tour` | Never used Claude Code (or using it like a chatbot) |
| 2 — Daily driver | `/kickstart:tour2` | Using it for real work; ready to configure it |
| 3 — Power tier | `/kickstart:tour3` | Making it enforce, extend, and scale to a team |

## Capability → where it's taught

| Capability | Where |
|---|---|
| Role-based intake (engineer / analyst / operator + code, terminal, git comfort) | Part 1, Session Zero — shapes examples in every lesson |
| The agent model (reads files, runs commands — point, don't paste) | Part 1, L1 |
| CLAUDE.md basics (`/init`, trimming, the token tax) | Part 1, L2 |
| Plan mode (Shift+Tab, reading plans critically) | Part 1, L3 |
| Responsible use of auto-accept / auto modes (when review may be traded for speed) | Part 1, L3 + Part 2, L3 |
| Context & cost hygiene (`/context` `/usage` `/clear` `/compact`) | Part 1, L4 — unskippable |
| Verification targets ("done when…", agent runs its own checks) | Part 1, L5 |
| Model & effort right-sizing (`/model` `/effort`) | Part 1, L6 + Part 3, L7 |
| Checkpoints & commits (`/rewind`, Claude-authored commits) | Part 1, L7 |
| CLAUDE.md hierarchy (user / project / subdirectory scopes) | Part 2, L1 |
| Memory across sessions (`/memory`, what to store where) | Part 2, L2 |
| Permission rules & modes (`/permissions`, auto / accept-edits) | Part 2, L3 |
| Authoring skills (your first `.claude/skills/…/SKILL.md`) | Part 2, L4 |
| Repo workflow (branches, PRs, `gh`, reviewing agent diffs) | Part 2, L5 |
| Subagents for context isolation (delegate noisy work) | Part 2, L6 |
| Multi-session work (`/resume`, parallel sessions, worktrees) | Part 2, L7 |
| Hooks (deterministic guardrails, PreToolUse blocking) | Part 3, L1 |
| Custom subagents (restricted tools = blast radius) | Part 3, L2 |
| Building & sharing plugins (marketplace, team onboarding) | Part 3, L3 |
| MCP (external tools, `claude mcp add`, hygiene) | Part 3, L4 |
| Headless (`claude -p`, `--allowedTools`, JSON output) | Part 3, L5 |
| CI & unattended runs (least privilege, spend bounds, human checkpoint) | Part 3, L6 |
| Team governance & the bill (settings-in-git, defaults over vigilance) | Part 3, L7 |
| Session efficiency audit, anytime | `/kickstart:coach` |
| Command quick reference | `/kickstart:cheatsheet` |

## Deliberately out of scope (and where to go instead)

- **Agent SDK** (building standalone agents in Python/TS) — named at Part 3 L6 as
  the graduation boundary; docs: code.claude.com/docs/en/agent-sdk/overview
- **IDE extensions / desktop / web surfaces** — same concepts everywhere; the tour
  teaches in the terminal, the habits transfer. docs: code.claude.com/docs/en/overview
- **Enterprise admin** (SSO, managed settings rollout, spend dashboards) — owner:
  whoever holds your org's Console; docs: code.claude.com/docs/en/costs
- **Prompt-engineering theory** — the tour teaches the two habits that matter
  (point at files, give a "done when"); deeper study: code.claude.com/docs/en/best-practices

If a Claude Code feature isn't in this table, treat that as a bug in the map —
file an issue.
