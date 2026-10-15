---
tags:
  - claude
  - kanban
---

# Master Kanban

> **The rules (read before writing to this board)**
>
> - **One board.** This is the only to-do list. "My list" means this file. Never read it whole: work it by column with grep or sed, and insert new cards directly under the column heading.
> - **Routing by owner.** 🎯 Big 3 and 🔥 My Desk are the owner's view: only what the owner personally drives. Everything the team owns lives in 👥 Team, where Claude tracks and flags it. Claude's recurring work lives in 🤖 Standing Ops.
> - **The test.** A Big 3 or My Desk card must pass: "does this materially move us toward the milestone, AND is it something only the owner can do?"
> - **Priority: exactly one per live card.** 🔴 Urgent (serves a named Big 3 card AND breaks or leaks money within 7 days; names the Big 3 and the due date; hard cap 5 board-wide) · 🟠 High (real money or a dated commitment this week) · 🟡 Medium (the default) · ⚪ Low (nothing breaks if it never happens).
> - **Urgency decays, never renews.** 🔴 open past 7 days drops to 🟠. 🟠 untouched 14 days drops to 🟡. Closed cards carry no priority icon.
> - **Owner icons.** 👤 owner · 🤖 Claude · 🤝 owner decides, Claude executes · 👥 team · ♻️ standing. **Flags:** 💰 money · ⏳ waiting.
> - **Card format.** `- [ ] [priority] [owner] [flags] **[Outcome, in one sentence].** [Context, source, due date]. **Done when:** [a test anyone can check].` Updates go underneath as dated `→` lines. Never rewrite history on a card; append.
> - **Status is live.** Sent for review or waiting on a reply: the card moves to ⏳ Waiting / Blocked at once, and back when they respond.
> - **Done = done.** A card the owner moved to ✅ Done never comes back. Closed cards older than 30 days move to [[Master Kanban - Archive]].
> - **Proactive capture.** Any owed deliverable, unanswered proposal, commitment or money opportunity Claude finds becomes a card immediately, deduped, and Claude says what it added.
>
> The cards below are fictional examples for "Acme Plumbing". The setup interview replaces them.

## 🎯 The Big 3 (HARD CAP: 3)

- [ ] 🟠 👤 💰 **#1: Sign 40 households to the annual maintenance plan before winter.** Recurring revenue smooths the slow months and every plan customer is first in line for replacement jobs. Source: [[GOALS.md]] plan, move 1. **Done when:** 40 active plans, verified in the billing system (count and report id cited). 👤 owner sells to past customers; 🤖 Claude drafts the offer email and builds the list of past customers from the last 24 months of invoices.
→ 2026-01-12: List built, 312 past customers. Offer email drafted, waiting on owner's OK.

## 🔥 My Desk (only what the owner personally touches this week)

- [ ] 🔴 👤 💰 **Approve the reminder to the property manager with two unpaid invoices before Friday.** Both invoices are past 45 days (INV-1042, INV-1057, example ids). Serves Big 3 #1 (cash to fund the plan launch). Draft is in email drafts. Due: Fri 2026-01-16.

## 👥 Team

- [ ] 🟡 👥 **Office manager: confirm every plan customer has a spring tune-up booked.** Owner: office manager. **Done when:** every active plan shows a booked date in the scheduling tool.

## 🤖 Standing Ops

<!-- Claude's recurring work: the morning report, end-of-day report, weekly review, inbox sweeps. One card per routine, ♻️ 🤖. -->

## ⏳ Waiting / Blocked

- [ ] 🟡 🤝 ⏳ 💰 **Commercial maintenance proposal for a 6-building apartment complex: waiting on the property manager.** Sent 2026-01-08 (owner approved the draft). Claude drafts a nudge on 2026-01-15 if there is no reply. **Done when:** signed or declined.

## 🗄️ Backlog / Someday

<!-- Honest list: most of these won't happen. A card leaves only by beating one of the Big 3. -->

## 🪦 Kill List

- [x] 🤖 **Build a custom booking app.** → 🪦 Killed 2026-01-05. Reason: fails the needle-mover test. The existing scheduling tool already books jobs; the build would cost two months of the only technical person's time and adds no revenue. Add back only if online bookings become a top-3 lead source.

## ✅ Done

<!-- Closed cards, newest first, no priority icon. Older than 30 days: move to Master Kanban - Archive.md. -->
