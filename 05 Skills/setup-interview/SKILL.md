---
name: setup-interview
description: First-run setup. Interviews the owner in seven short rounds and fills CLAUDE.md, GOALS.md, On Demand Memory.md and the Master Kanban with real answers. Run when CLAUDE.md still has [bracketed placeholders], or when the owner says "set this up for my business".
tags:
  - claude
  - skill
---

# Setup Interview

Goal: about 20 minutes of the owner's time, every placeholder replaced with a real answer, and a board with a real Big 3.

## How to run it

- **Small batches.** 3 or 4 questions per message, never more. Number them so the owner can answer "1. ... 2. ...".
- **Summarize back.** After each round, play it back in 3 to 5 bullets and ask "Right?" Fix it before moving on.
- **Push for numbers.** "About 40 clients" beats "a good number". If the owner doesn't know, write `unknown`, and add a card to find out. Never invent.
- **Sharpen vague answers.** If an answer is fuzzy (especially the prime directive), offer 2 or 3 sharper versions and let the owner pick.
- **Save as you go.** After each round, append the answers to `00 Notes/Setup Answers.md` (tag `claude`). If the session breaks, resume from there.
- **Use what exists.** Before round 1, ask if there is a website, a pitch, a planning doc or old notes to paste in. Pre-fill from it and only ask what's missing.

## Round 0: Check where we are

Look for single-bracket placeholders in `CLAUDE.md`, `GOALS.md` and `On Demand Memory.md` (ignore `[[wiki links]]`). If some sections are already filled, confirm them in one line each and start at the first empty one. Tell the owner: "7 short rounds, about 20 minutes. You can stop anytime and I'll pick up where we left off."

## Round 1: The business and the owner

1. What do you sell, to whom, and how does the money come in?
2. What do you do day to day? What do you love doing, and what do you wish you never touched again?
3. What is the business ultimately for? (freedom, family, a number, an exit: your words)
4. Where do you get in your own way?

Fills: `CLAUDE.md` "Who [Owner name] Is", the title line, business name.

## Round 2: Prime directive and the next milestone

1. Today's numbers: monthly revenue, profit or margin, active clients, cash. Where does each one live?
2. The next milestone: one number and one date.
3. What must not get worse while you chase it? (margin, your hours, quality)
4. If you got 5 hours back every week, what would you spend them on?

Draft the prime directive (a direction plus a constraint) and offer options. Fills: "My Lane and Prime Directive", the needle-mover test wording in "The Operating Algorithm", `GOALS.md` milestone and current numbers (marked "owner-stated, unverified" until round 5).

## Round 3: Rules and what Claude may do without asking

Explain the default first: Claude executes research, builds, notes and board changes on its own, and holds two things as drafts: messages to other people, and anything that moves, spends or commits money.

1. Anything to loosen or tighten in that default?
2. Any standing exceptions? (e.g. a routine allowed to send one specific confirmation email)
3. How should I talk to you? (blunt or gentle, short or detailed, words you hate)
4. Anything I must never touch?

Fills: "Hard Rules". Write one entry per rule in `On Demand Memory.md` "Rule history & rationale" with today's date and the owner's reason.

## Round 4: The team and who owns what

1. Who is on the team, what role, what do they own? (names or roles)
2. Who decides pricing, hiring and refunds?
3. What do you still do yourself that someone else should own?

Fills: owners for 👥 Team cards. Note answers to question 3 as delegate or kill candidates for round 6.

## Round 5: Tools and where the money lives

1. Where is revenue recorded (billing, invoicing, accounting)? Which bank?
2. Email, calendar, chat, call recorder, CRM: which tools?
3. Which of these are connected to me? (check the available connectors; list what is missing)
4. Which private channel should my reports and reminders go to?

If a billing or bank connector is live, pull the round 2 numbers now and replace the owner-stated values, citing source, object or report id, and date. Fills: `On Demand Memory.md` "Key IDs and integrations", the `[billing system]`, `[bank]` and `[private channel]` placeholders in `CLAUDE.md`. Write a note in `07 Tools/` for any integration with non-obvious setup.

## Round 6: Everything in flight

1. List every project, offer, build, hire and promise in flight. All of it; we cut next.
2. For each: who owns it, and what does done look like?

Run the operating algorithm out loud on the list: question each one, then recommend what to kill, with a one-line reason. The owner vetoes. Survivors get the `new-project` skill (only the ones big enough to need a folder) and a line in "Projects, one line each". Killed items become 🪦 cards with the reason.

## Round 7: Seed the board

1. Delete the fictional example cards from `Master Kanban.md`.
2. Propose the Big 3: at most three, each passing the needle-mover test and drivable only by the owner. The owner picks.
3. Every other surviving item becomes one card in the right column, with one priority, one owner icon, and a "Done when".
4. Anything owed that came up in the interview (unsent proposals, unpaid invoices, promised deliverables) becomes a card, 💰 where money is involved.
5. Write the `GOALS.md` plan: the gap math, then 3 to 5 moves mapped to the Big 3.

## Write and report

1. Write the final `CLAUDE.md`, `GOALS.md`, `On Demand Memory.md` and `Master Kanban.md`. Delete each `<!-- guidance -->` comment once its section is filled, and delete the setup check line at the top of `CLAUDE.md`.
2. Check for placeholders again. Anything still unknown gets listed for the owner and a card.
3. Show a diff summary: per file, what got filled and what is still open (`git diff --stat` if the folder is a git repo).
4. Close with next steps: which routine in `routines/` to schedule first, and the first action on Big 3 #1.

## Changelog

- 2026-10-14: Created.
