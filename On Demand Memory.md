---
tags:
  - claude
  - memory
---

# On Demand Memory

<!-- Not loaded every session. Claude reads the section it needs: when a rule needs explaining, a routine needs managing, or an integration needs an ID. Never store secrets here. -->

## Rule history & rationale

One entry per rule in `CLAUDE.md`: when it was set, what happened, why it exists, and any exception granted. CLAUDE.md keeps the rule in one line; the story lives here.

Format: **[Rule name] ([YYYY-MM-DD]).** [What happened]. [Why the rule fixes it]. [Exceptions: who granted, when].

Example (fictional): **Verify every money claim (2025-03-02).** Claude put a client refund on the board from memory; the refund never happened and the owner nearly apologized for it. Every figure now cites a live object id or is marked unverified.

- [First real entry]

## Routine registry

| Routine | Schedule (timezone) | Runs where | ID | Posts to | Prompt | Status |
|---|---|---|---|---|---|---|
| Morning Report | Weekdays [07:00] [tz] | [cloud routine, scheduled task, cron] | [id] | [private channel] | `routines/morning-report.md` | [active] |
| End-of-Day Report | Weekdays [18:00] [tz] | [ ] | [id] | [private channel] | `routines/eod-report.md` | [active] |
| Weekly Review | [Sunday 18:00] [tz] | [ ] | [id] | [private channel] | `routines/weekly-review.md` | [active] |

When a routine is paused or killed, keep the row and change Status, with the date and the reason.

## Key IDs and integrations

| System | What it holds | How Claude reaches it | Key IDs (channel, account, folder) |
|---|---|---|---|
| [Billing] | Revenue, invoices, subscriptions | [connector name] | [ ] |
| [Bank] | Cash, transactions | [connector name] | [ ] |
| [Email] | Client and prospect threads | [connector name] | [ ] |
| [Calendar] | Meetings | [connector name] | [ ] |
| [Chat] | Team, private report channel | [connector name] | [private channel id] |
| [Call recorder] | Sales and client call transcripts | [connector name] | [ ] |
| [CRM] | Pipeline | [connector name] | [ ] |

Secrets (API keys, tokens) live in `.env` (ignored by git) or in the tool's own config, never in the vault.

## API notes

Quirks, limits and gotchas learned the hard way. One dated line each.

- [YYYY-MM-DD] [System]: [quirk] → [workaround].
