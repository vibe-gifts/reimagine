# reimagine

[Português](README.md) · **English** · [Español](README.es.md)

**A skill that makes your AI agent redesign a process from the goal backwards, instead of patching the steps.**

Polishing steps gets you 10%. Reimagining gets you 10x, because it changes the structure that makes those steps necessary.

You state the outcome you want, ideally an absurd one ("I want this video done in 5 minutes, not 2 hours"). The agent reads your files and history, finds where the back-and-forth really comes from, and hands you a new system. It changes nothing before your OK.

## Why an absurd target works

"20 minutes" invites the agent to tune what exists. "5 minutes" forces it to delete, merge and reorder. The absurd target is a tool: it rules out patching. If the target is truly impossible, the skill says so honestly and shows how far you can get, and how.

Ask for the **outcome**, not the steps. Whoever describes steps describes the system they already have, and the agent will only rearrange it.

## What it does

1. **Pins the goal and the target** in one line. No target given? It sets one and tells you: time ÷ 10, one round of fixes, at most 2 stops for you.
2. **Measures reality before forming an opinion.** It reads the files, git history, past conversations and old versions, and counts: how many rounds, how much was redone, where the time goes. The most common finding is "written down, but nothing checks it".
3. **Finds the structural root causes.** Rules born only at review time, sources that contradict each other, expensive work before cheap decisions, one actor doing four jobs, guard on top of guard, the same thing built twice, everything made from scratch each time.
4. **Cuts in the right order.** Questions every requirement (and finds out why it exists before cutting), deletes, simplifies, puts cheap before expensive, and only then automates.
5. **Designs the new system:** a one-sentence thesis, a single source of truth, one job per unit, approved parts instead of new work, every rejection turned into an automatic check, the list of what goes away, and a measurable target.
6. **Runs a pre-mortem:** the 3 most likely ways the new design fails.
7. **Delivers and waits:** the structure as a table, tree or mockup, what was not verified, and a single decision for you.

It works for processes and production pipelines, screens and dashboards, bots and AI agents, and folder structures. It is not for fixing a known bug or a small copy tweak.

## Installation

**Claude Code:** in the message box, type:

```
/plugin marketplace add vibe-gifts/reimagine
/plugin install reimagine@reimagine
```

In the Claude desktop app (Code tab), click **+** next to the message box, then **Plugins** and **Add marketplace**. Enter `vibe-gifts/reimagine` and click **Add plugin**.

**Codex or another agent:** download this repository (**Code** button → **Download ZIP**), unzip it and point the agent to the `skills/reimagine` folder.

Then just ask:

> reimagine how we publish blog posts. Today it takes 3 days and goes back and forth a lot. Goal: a post live in 1 hour, approved on the first try.

## Good to know

- **It only proposes.** Nothing in your project changes before your OK.
- It replies in your language.
- The `skills/reimagine/evals` folder holds 3 test cases in the `claude plugin eval` format.

## License

MIT
