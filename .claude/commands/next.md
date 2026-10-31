---
description: Find the next Oriw issue to work on, across the roadmap
---
Find the next issue to work on for Oriw.

1. List open issues in this repository with `gh api "repos/oriw-app/<this repo>/issues?state=open&per_page=100"`. If this is `oriw`, include milestones.
2. Pick using the order in CLAUDE.md: earliest open milestone (by due date, then name), `priority: must-have` before `should-have` before `nice-to-have`, then lowest number. Skip issues assigned to someone else and pull requests.
3. Read the chosen issue in full, including its comments. If the last comment is a handoff, start from its "Next" list.
4. Reply with: the issue number and title, why it's next, its "Done when" list, the latest handoff if any, and a plan that follows `docs/ENGINEERING.md`:
   - the bounded context and glossary words involved (and any new term to add to `docs/DOMAIN.md`),
   - the scenarios to write first in `features/<context>/` (or the existing `@wip` ones to finish),
   - the commands, queries, domain events and ports the change needs,
   - the unit tests to write before the code.
   Ask before starting if the plan changes anything outside this repository.
