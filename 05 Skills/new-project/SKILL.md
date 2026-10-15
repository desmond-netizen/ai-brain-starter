---
name: new-project
description: Creates 03 Projects/<Name>/ with its own short CLAUDE.md and adds one line to the root CLAUDE.md. Use when the owner starts a new project, offer, client engagement or build.
tags:
  - claude
  - skill
---

# New Project

1. **Test it first.** Does it pass the needle-mover test? If not, say so and offer a 🗄️ Backlog card instead. The owner can override.
2. **Get five answers** (ask only for what's missing): name, what it is, how it serves the milestone, one owner, done when.
3. **Create** `03 Projects/<Name>/CLAUDE.md`:

```markdown
---
tags: [claude, project]
created: YYYY-MM-DD
---
# <Name>
**What:** [one line]
**Why:** [how it moves the prime directive or the milestone]
**Owner:** [one name]
**Done when:** [a test anyone can check]
**Status:** active, YYYY-MM-DD
**Where the work lives:** [docs, repos, channels, folders]
```

4. **Add one line** to root `CLAUDE.md` under "Projects, one line each": `` - **<Name>** (`03 Projects/<Name>/`): [what it is and how it serves the prime directive]. ``
5. **Add the first card** to the board if the project has a next action.
6. **Tell the owner** what was created, in two lines.

Closing a project: set Status to done or killed with the date, move the folder to `99 Archive/`, remove its line from `CLAUDE.md`.

## Changelog

- 2026-10-14: Created.
