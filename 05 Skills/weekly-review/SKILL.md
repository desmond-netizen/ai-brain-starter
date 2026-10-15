---
name: weekly-review
description: The weekly operating review. Pulls live numbers, compares them to GOALS.md, reviews the Big 3, applies the board's decay rules, proposes kills, writes the review note and refreshes the CLAUDE.md snapshot. Run once a week, by routine or when the owner says "run the weekly review".
tags:
  - claude
  - skill
---

# Weekly Review

Outputs: `04 Reviews/Weekly Review YYYY-MM-DD.md`, a cleaned board, a fresh snapshot in `CLAUDE.md` and `GOALS.md`, and a short post to the private channel.

## Steps

1. **Pull live numbers.** For every metric in `GOALS.md` "Current Numbers", query its live source and cite the object or report id with a timestamp. Source unreachable: carry the old value, marked `stale since [date]`. Never estimate.
2. **Compare to the milestone.** Change since last week, distance to target, and pace: `gap / weeks left = needed per week` against the actual weekly change. Say plainly whether we are on pace.
3. **Review the Big 3.** For each card:
   - Did it move this week? Evidence only: dated `→` lines, sent messages, payments, commits.
   - Does it still pass the needle-mover test, and is it still something only the owner can drive?
   - Verdict: keep, reframe, or swap. "Done when" met: move it to ✅ Done. Propose a replacement only if it beats the weakest of the three.
4. **Apply decay.** Work the board by column with grep, never whole. 🔴 open past 7 days drops to 🟠. 🟠 untouched 14 days drops to 🟡. Count 🔴 board-wide; over 5, demote the ones least tied to a Big 3 card. Age comes from the latest dated `→` line or the capture date. Log each change as a dated `→` line.
5. **Sweep for money and loose ends.** ⏳ cards with no reply for 7 days: draft a nudge (draft only). 💰 cards untouched 14 days: flag them. Any promise or owed deliverable from this week's email, chat or calls that is not on the board: add it.
6. **Propose kills.** List 3 to 5 cards that fail the needle-mover test or have not moved in 30 days, each with a one-line reason. On the owner's OK, move them to 🪦 Kill List with the reason. The owner can veto any of them.
7. **Archive.** ✅ Done cards older than 30 days move to `Master Kanban - Archive.md`.
8. **Learn from results.** What worked this week, backed by a cited result? If it proves or disproves a tactic, update the owning skill now with a dated `## Changelog` line. Recommend where to double down.
9. **Write the review note** (template below).
10. **Refresh the snapshot.** Update the Snapshot lines and the "Last weekly review" line in `CLAUDE.md`, and the Current Numbers table in `GOALS.md`.
11. **Post** a summary of 8 lines or fewer to the private channel: pace, Big 3 verdicts, kills proposed, top 3 actions for next week.

## Review note template

```markdown
---
tags:
  - claude
  - review
date: YYYY-MM-DD
---

# Weekly Review YYYY-MM-DD

## Numbers
| Metric | This week | Last week | Change | Source (id, timestamp) |
|---|---|---|---|---|

## Pace to milestone
Gap, weeks left, needed per week, actual this week. On pace: yes or no.

## Big 3
1. [Card]: moved / stuck. Evidence. Verdict.

## Board changes
Decayed, archived, added, moved to Waiting.

## Kill list candidates
- [Card]: reason.

## What worked (cited) and where to double down

## Next week: top 3 actions
```

## Changelog

- 2026-10-14: Created.
