# Skills

A skill is a written procedure for work that repeats: a review, a report, a proposal, a client onboarding. Each one is a folder with a `SKILL.md`. Claude finds them through the Skills section of `CLAUDE.md` and follows the steps when a task matches. To also use them as slash commands in Claude Code, copy the folder into `.claude/skills/`.

| Skill | When |
|---|---|
| `setup-interview/` | First run. Fills the templates from the owner's answers. |
| `weekly-review/` | Once a week. Numbers, Big 3, decay, kills, snapshot. |
| `new-project/` | A new project, offer or build starts. |
| `skill-template/` | Copy this to write your own. |

## Writing a skill

Write one after you have done the same task by hand twice. Copy `skill-template/`, keep the steps short and concrete, and name the output. Add it to the Skills line in `CLAUDE.md`.

## Skills learn from real results

A skill gets better only from evidence. When a real result (a call recording, a payment, campaign data, a client reply) proves or disproves a tactic in a skill, update that skill the same day and add a dated line to its `## Changelog`, citing the result:

```
- 2026-02-03: Moved the price anchor before the case study. Source: 3 of 4 calls closed after the switch (call recordings of Jan 20, 22, 27, 30).
```

Never change a skill from a hunch, a blog post or "this feels better". No cited result, no change.
