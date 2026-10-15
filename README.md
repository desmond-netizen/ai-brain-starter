# AI Brain Starter

A Markdown vault that turns Claude Code (or Codex) into the operating brain for a business owner.
One context file, one task board, a few skills and scheduled reports, all built around one habit: delete before you add.

## What's inside

| File or folder | What it does |
|---|---|
| `CLAUDE.md` | The brain. Who you are, Claude's lane and prime directive, the operating algorithm, hard rules, board rules, folder map, projects, routines, snapshot. Loaded every session, so it stays short. |
| `AGENTS.md` | Points Codex at `CLAUDE.md`. |
| `GOALS.md` | The next milestone, current numbers (each with a source and date), the plan, risks. |
| `On Demand Memory.md` | Loaded only when needed: why each rule exists, the routine registry, key IDs and integrations, API notes. |
| `Master Kanban.md` | The only to-do list. Owner-split columns, priority caps, decay rules, a Kill List. |
| `Master Kanban - Archive.md` | Closed cards, moved out so the board stays cheap to read. |
| `05 Skills/` | Repeatable procedures: `setup-interview`, `weekly-review`, `new-project`, and a template for your own. |
| `routines/` | Copy-paste prompts for scheduled runs: morning report, end-of-day report, weekly review. |
| `00 Notes/` `02 Chess Moves/` `03 Projects/` `04 Reviews/` `07 Tools/` `99 Archive/` `Wiki/` | The folder skeleton. Each has a one-line README saying what goes there. |

## How to use

1. Download the ZIP (Code, Download ZIP) and unzip it.
2. Open the folder in Claude Code (`cd ai-brain-starter && claude`) or Codex.
3. Say: **"Read the README and set this up for my business."**
4. Claude runs the setup interview (about 20 minutes, 7 short rounds). It fills `CLAUDE.md`, `GOALS.md` and `On Demand Memory.md`, then seeds the board with your real Big 3.
5. Optional: open the same folder as a vault in Obsidian to read and edit it like notes.

Claude Code reads `CLAUDE.md` automatically every session. Codex reads `AGENTS.md`, which tells it to read `CLAUDE.md`. Skills are found through `CLAUDE.md`; to also get them as slash commands in Claude Code, copy a skill folder into `.claude/skills/`.

After setup, talk to it like a chief of staff:

- "What's on my list?"
- "I just got off a call with a prospect, here's my notes. Capture what I owe."
- "Run the weekly review."
- "Should we build a client portal?" (expect it to push back)

## The core ideas

**The operating algorithm.** Applied in order to every task, process and build: question the requirement (it needs a named owner and must trace to the prime directive), delete it (killed items go to the Kill List with the reason), simplify, accelerate, automate last. Default is deletion, not addition.

**Three needle-movers, max.** The Big 3 column holds at most three cards. Every card must pass one test: "does this materially move us toward the milestone?" Claude recommends killing things, including yours. You can veto.

**One board.** `Master Kanban.md` is the only to-do list. Columns split by owner, so you only see what you personally drive. Every card has one owner and exactly one priority. Red is capped at five. Urgency decays and never renews. Done means done.

**Draft only comms and money.** Claude executes research, builds, notes and board updates on its own, then tells you. It holds two things as drafts for your OK: messages to other people, and anything that moves, spends or commits money.

**Verify money live.** No revenue figure, payment or "X owes us" from memory. Claude pulls it from the live source at the moment of writing and cites the object id, or labels it unverified.

**Skills learn from real results.** When a real result (a closed deal, a campaign number, a call recording) proves or disproves a tactic, the owning skill gets updated that day with a dated changelog line. Never from a hunch.

**Short context, deep memory.** `CLAUDE.md` holds rules in one or two lines each. The story behind every rule lives in `On Demand Memory.md`, read only when needed. The board is worked by column with grep, never loaded whole.

## Routines

The prompts in `routines/` are written for scheduled Claude runs (Claude Code routines, the `/schedule` command, or any cron that runs `claude -p`). Each one posts to a single private chat channel and stays silent when there is nothing to act on. A cloud routine needs the vault in a private git repo it can clone. Record every routine you create in the registry in `On Demand Memory.md`.

Reminders work the same way: schedule a run that checks a state (did the invoice get paid, did the prospect reply) and posts only if action is still needed. Log the reminder on the card.

## Requirements

- Claude Code or Codex.
- Optional: Obsidian, for reading the vault as notes.
- Optional but recommended: connectors (MCP) for your billing system, bank, email, calendar and chat. Without them Claude cannot verify money live and will mark numbers unverified.
- Optional: a private Slack (or similar) channel for routine output.
