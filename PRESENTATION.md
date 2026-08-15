# Presenter runbook — 10 minutes, 300 people, recorded

Audience: mostly never used Claude Code; company pays the API bill. The one message
that must land: **this is an agent, not a chatbot — and the habits in Lesson 4 are
the difference between a force multiplier and a money fire.**

## Pre-flight (day before + hour before)

- [ ] Demo repo chosen: small, real, familiar to you, with a fast test suite and a
      known small bug or easy change staged. Nothing confidential on screen.
- [ ] Pre-warmed session: `claude` already signed in on the demo machine; run the
      demo beats once end-to-end the night before AND record that run as the
      **fallback clip** (conference wifi + live LLM = plan for failure).
- [ ] Terminal font huge (24pt+), light-on-dark, prompt shortened.
- [ ] Plugin published: repo public, `<your-github-username>` placeholders in
      README/RESOURCES replaced, install flow re-tested from a clean machine.
- [ ] `/clear` run right before walking on stage (start from an empty session).
- [ ] Slides: install slide (3 commands), resources slide (from RESOURCES.md), five
      cost commandments slide (from the cheatsheet skill).

**Crowd-control note:** do NOT ask 300 people to install during the talk — 300
simultaneous installs on venue wifi is a support incident, not a demo. Show the
install live yourself; the audience does it after, from the slide and the recording.

## Timeline

### 0:00–1:30 — What it is, and the expensive way to get it wrong

- One sentence: "Claude Code is an AI agent that works *in your repo* — it reads
  files, runs commands, and checks its own work."
- The anti-pattern, named explicitly: using it like a chat bot — pasting code into
  messages, re-explaining the project every time, one endless session. "That's the
  most expensive possible way to use this, and it also gives the worst results.
  Ten minutes from now you'll know the five habits that avoid it."

### 1:30–6:30 — Live demo (the beats, with exact keystrokes)

1. **Point, don't paste** (~1 min). In the demo repo: ask a real codebase question —
   "where do we handle retry logic, and what's the backoff?" Narrate while it works:
   "I pasted nothing. It's reading only what it needs."
2. **Plan mode** (~2 min). Press **Shift+Tab** → plan mode. Request the staged small
   change. When the plan appears: "This plan cost cents. If it's wrong, I fix it
   *here* — not after it's written the wrong code." Approve; let it implement.
3. **Verify, don't vibe** (~1 min). The request included "done when the tests pass" —
   show it running the tests itself. "I didn't check its work. I made it check its own."
4. **The meter** (~1 min). Run `/context` — "this is the context window; it's the
   meter that's always running." Run `/usage` — show the session's actual spend.
   Then run `/clear`: "Task's done. This is the cheapest button in the product, and
   the most underused. Five clean sessions beat one marathon — on cost AND quality."

### 6:30–8:30 — The kickstart plugin (install shown live, done later)

- Install slide up. Type, live:
  `/plugin marketplace add <your-github-username>/claude-code-kickstart`
  `/plugin install kickstart@claude-code-kickstart`
- Run `/kickstart:tour` and let it play its opening — the greet + "your project or a
  practice one?" beat sells the whole thing in 20 seconds.
- The pitch, verbatim if you like: "This is an eight-lesson guided tour that runs in
  *your* project and adapts to *you*. Do one lesson with your coffee each morning;
  it saves your place. It will not let you skip the cost lesson. And when you outgrow
  it, Parts 2 and 3 are already installed — same plugin takes you from first session
  to building your team's own hooks, plugins, and CI automation."

### 8:30–10:00 — Resources + close

- Resources slide (4 links). "Quickstart today, best-practices after your first week."
- Five cost commandments slide. Read them once, straight:
  1. Point, don't paste. 2. Plan before you build. 3. Give every request a "done
  when". 4. Finished → `/clear`. 5. Right-size the model.
- Close: "The tool is already good. The bill and the results both come down to
  habits — and the tour teaches the habits. `/kickstart:tour`. Go."

## Q&A ammunition

**"Is the tour's 'adaptive learning' another AI service we're paying for?"**
No — and this is deliberate. The tutor *is* Claude Code, driven by a plugin skill: a
few pages of static markdown, loaded only when invoked. There's no server, no second
API bill, no per-user infrastructure — tutoring happens inside the session the
learner is already running, so a full tour costs single-digit dollars per person,
once. A hosted adaptive-learning app would add infrastructure and per-seat billing
to reproduce what the product already is. And the tour's centerpiece lesson teaches
the context-hygiene habits that pay back its own token cost within days.

**"What stops people from burning money anyway?"** Habits (this talk), visibility
(`/usage`, `/context`, and Console spend dashboards), and `/kickstart:coach` — anyone
can ask "am I using this efficiently?" and get an audit of their live session.

**"Does it work on Windows?"** Yes — PowerShell installer on the install slide;
everything else is identical.

**"What about our code going to Anthropic?"** Point at your org's existing agreement
(Console/enterprise terms); Claude Code sends what the session needs to the API under
that agreement — same data path as any approved API usage. Defer specifics to
whoever owns the vendor relationship. (Check this framing with them *before* the talk.)

## Failure modes

| If… | Then… |
|---|---|
| Wifi/API dies mid-demo | Play the pre-recorded fallback clip; narrate over it live. |
| Demo takes a weird turn | Let it — narrate honestly ("this is real"), then `/rewind` or `/clear`. Authenticity beats polish; a recovered surprise is the best plan-mode ad there is. |
| Running long | Cut beat 3 (verification) from the demo — it's re-taught in the tour. Never cut beat 4 (`/context`//`usage`//`clear`). |
| Someone asks price specifics | "Depends on plan and usage — that's the Managing Costs link; your lead has the dashboard." Don't improvise numbers on stage. |
