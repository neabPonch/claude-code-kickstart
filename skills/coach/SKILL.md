---
name: coach
description: Audit the current session for token waste and inefficient Claude Code usage. Use when the user asks about cost, tokens, context, efficiency, why responses got slow or worse, or whether they are "using this right".
---

Audit how this session is being run and give the user 2–3 concrete, prioritized
fixes — with the exact command for each. Be honest and specific; a coach who says
"looks fine!" to a bloated session is teaching an expensive habit.

## What to check (in priority order)

1. **Session shape.** Is this one long marathon spanning several unrelated tasks?
   Are there abandoned approaches, resolved errors, or dead ends still sitting in
   history? → Recommend `/clear` (new task, nothing worth keeping), `/compact` with a
   steering note (mid-task, history matters), or `/rewind` (last approach was a dead
   end). Have them run `/context` and `/usage` to see the numbers themselves.
2. **Chatbot habits.** Has the user been pasting code or logs into messages instead
   of pointing at files/commands? Re-explaining project context that belongs in
   CLAUDE.md? → Show the agent-native alternative for the specific thing they pasted.
3. **Missing verification targets.** Are requests framed as "make it better" instead
   of "done when X passes"? → Rewrite their most recent vague request as a verifiable
   one, as a worked example.
4. **CLAUDE.md tax.** If the project's CLAUDE.md is long (roughly >100 lines), remind
   them every line is loaded in every session — suggest trimming or moving
   rarely-needed content into a skill or linked doc.
5. **Horsepower fit.** Is the work in this session mechanical (renames, boilerplate,
   formatting) while running the top model at high effort — or gnarly while running a
   cheap tier? → Suggest `/model` / `/effort` adjustments for the *next* task, not a
   mid-task switch.

## Output shape

Keep the whole audit under ~20 lines:

- One-line verdict on the session's health.
- The 2–3 fixes, each as: **what's costing you → the command → why it helps.**
- Close with the standing reminder: finished a task → `/clear`. It is the cheapest
  button in the product, and the most underused.

Do not re-read large parts of the project to produce this audit — that would be the
disease posing as the cure. Judge from the conversation itself plus at most a glance
at CLAUDE.md's length.
