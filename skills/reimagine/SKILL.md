---
name: reimagine
description: >-
  Redesign a process, workflow, product, screen, folder structure or agent system from the goal
  backwards, grounded in evidence from the user's own files and history, instead of polishing the
  steps that exist. Use when the user says "reimagine", "/reimagine", "rethink this", "what's the
  simplest model", "this keeps going back and forth", "too much rework", "it's confusing", "make it
  10x faster", "approved on the first try", or states an outcome (often a deliberately absurd target,
  like "5 minutes instead of 2 hours") and leaves the how to you. Also in Portuguese: "reimagina",
  "repensa", "o modelo mais simples", "vai e volta demais", "está confuso". Use it even when the user
  never says "reimagine": whenever they are frustrated with how something works as a whole, keep
  patching the same thing, or ask for a result far beyond what tuning can reach. Not for a known
  bug fix, a small copy or style tweak, or brainstorming with no existing system to look at.
---

# Reimagine

Polishing steps gets you 10%. Reimagining gets you 10x, because it changes the structure that makes
the steps necessary. This skill finds where the friction really comes from, then rebuilds the system
around the goal.

The user's job is to state the **outcome**. Your job is the **how**. If they hand you steps, look
past them to the outcome they serve. This matters because people describe the system they already
have; asked for steps, you would only rearrange it.

Why the evidence-first rule: a redesign built on assumptions fixes the problem you imagined. Every
strong reimagine so far started from a number the user had never seen (7 folder layouts where the
docs promised 1, 91 of 94 scenes redrawn because of one pause change), and that number is what made
the new structure obvious and convincing.

## 0. Pin the goal and the stretch target

Write one line: *"Goal: <outcome>. Target: <number>."*

- Use the user's target even if it looks impossible. An absurd target is a tool: it rules out
  polishing and forces you to delete, merge and reorder. "20 minutes" invites tuning; "5 minutes"
  forces a different system.
- No target given? Set one yourself and say so: time ÷ 10, rework rounds → 1, human stops ≤ 2,
  questions answered at a glance.
- Name the unit of success: one approved video, one entry in two messages, one screen that answers
  one question.
- If the target is literally unreachable (zero errors, instant), keep it as the direction and name
  a reachable number next to it. Design for the stretch target and report the gap honestly in step 6.

## 1. Measure reality before forming an opinion

Evidence first. Read before you propose, and count.

- **The artifacts**: the files, code, docs, rules and the live product (open it, do not imagine it).
- **The history**: past conversations, git log, version folders (v1, v2, v3), review notes,
  "liked / disliked" lists, logs. History tells you where rework actually happened. How to mine it:
  `git log --stat` and dated files for what changed and how often; agent transcripts (for Claude
  Code, `~/.claude/projects/<folder>/*.jsonl`; search them with `rg` or `jq` for the project's name,
  "redo", "wrong", "again", never read whole files); the user's notes or task tracker for
  complaints and decisions. Look for the user's own words of frustration: they mark the loops.
- **The numbers**: rounds per delivery, time per step, how much is redone after each review, how
  many places hold the same rule, what is used and what is never used.
- **Claims vs checks**: list what the docs say is true ("every client has the same folders") and test
  whether anything enforces it. "Written but never verified" is the most common finding.

Use cheap helpers for wide reading when available. Say in one line what you understood before going
deep, so a misread goal gets caught early.

## 2. Find the root causes

For each rework loop, ask "why did this have to be redone?" until the answer is structural, not
"someone made a mistake". Then find the one constraint that limits the whole flow. Improving
anything else is waste until that one moves.

Usual suspects (check every one):

| Pattern | Sign |
|---|---|
| Rules born at review time | each delivery produces new rules after the human sees it |
| Scattered or contradictory sources | the same rule in 3 files, with different values |
| Expensive before cheap | the costly step (render, generation, build) runs before the cheap decision (rhythm, layout, numbers) |
| One actor, many jobs | the AI understands, calculates, decides and writes in one pass |
| Guard on top of guard | patches that catch the error after it happens |
| Built twice | two systems doing the same job; parts used zero times |
| From scratch every time | approved pieces never became reusable parts |
| Agent blind spot | the agent can't hear, see or run something, so the human becomes the QA |
| Unenforced claims | docs promise an invariant that nothing checks |

## 3. Cut in the right order

Draft the one-sentence thesis of the new system first (see step 4), then cut the current system
against it. Apply these strictly in order. Optimizing something that should not exist is the most
common mistake.

1. **Question every requirement.** Who asked for it, and why? Before cutting, find the reason it
   exists (Chesterton's fence). Keep legal and safety obligations; challenge habits.
2. **Delete.** Steps, files, checks, versions, options. If nothing ever needs to be added back, you
   did not delete enough. Write each cut as one row: *what goes, why it existed, why that reason no
   longer holds*.
3. **Simplify** what survives: one source of truth, one job per unit.
4. **Reorder: cheap first.** Every decision moves to the cheapest format that can show it (text, a
   still frame, a low-res preview, a shown calculation) before anything expensive runs.
5. **Automate last.** Turn each human rejection into a check that runs on its own.

## 4. Design the new system

The proposal must contain:

- **A one-sentence thesis.** Example: "Decide everything in the cheap format, build only from
  approved parts, and let a robot check before the human does."
- **A single source of truth**, machine-readable where possible, that the checks read.
- **One job per unit**: one question per screen, one task per actor, one purpose per folder.
- **A library of approved parts** instead of new work each time.
- **Gates**: where the human stops (2 at most) and what each stop costs them in minutes.
- **The feedback loop**: every rejection becomes an automated check, not just a note.
- **What goes away**, listed explicitly.
- **What stays** and why, so the user sees you kept what works.
- **A success metric** that can be measured on the next delivery.
- **A migration path** in small stages. The first stage is the one with the highest leverage that
  can be used right away.

## 5. Pre-mortem

Before presenting, write the three most likely ways the new design fails in practice (adoption,
edge cases, hidden dependencies). Fix them or name them.

## 6. Deliver

- Show the structure concretely: a table, a tree, a flow or a mockup. Never only prose.
- Scale the length to the problem. When space is tight, compress prose, never the evidence, the
  list of cuts or the pre-mortem.
- Put the diagnosis first, with the evidence and numbers that back it.
- Be honest about the target: "5 minutes is not reachable; 20 is, through X; the gap is Y."
- Say what you did not verify.
- **Change nothing before the user's OK.** A reimagine moves the user's own system, and they often
  know a reason you could not see; acting first turns a good proposal into rework.
- End with one decision for the user: usually "start with stage 1?".

## Adapting to the domain

- **Process or pipeline**: map the steps with time and cost, and look for loops and the bottleneck.
- **Screen or dashboard**: list the questions the user must answer at a glance; one question per
  view; the verdict before the detail. Function before decoration.
- **Agent or bot**: separate understanding, calculating, deciding and writing; show the calculation
  to the human; ask only when an error is expensive, assume (and show) when it is cheap.
- **Folders or knowledge base**: one tree, one machine-readable spec, and checks at every entry point
  (merge, commit, audit).

## Anti-patterns

- Proposing tools before diagnosing. Which tool to use comes last.
- Adding another rule or guard to fix a problem the rules created.
- Generic advice with no number from the user's own reality.
- Rewriting everything at once. Stage it.
- Role-playing a famous person instead of reading the evidence.

## Worked examples

Read `references/cases.md` before step 4 the first time you use this skill, or whenever you are
unsure how concrete the proposal should be. It holds five real cases (video pipeline, finance
dashboard, chat bot, folder structure, node editor) with what was measured, the diagnosis, the move
and how the user reacted.
