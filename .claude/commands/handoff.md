---
description: Record progress on the current issue so the next session can continue
---
Write a handoff for the issue this session worked on (ask which, if it isn't clear from the branch name).

1. Summarise from this session and `git log`/`git status` on the current branch:
   - **Done:** what changed, with commit or pull request links.
   - **Next:** the remaining steps, in order, specific enough to start without re-reading the code.
   - **Blocked or decisions needed:** anything waiting on a person, with their name if known.
   - **How to check:** commands to build and test what exists.
2. Make sure work in progress is committed and pushed to the issue's branch first.
3. Post it as a comment on the issue: `gh api -X POST repos/oriw-app/<repo>/issues/<n>/comments -f body=...`, starting with the heading "Handoff".
4. Tick any "Done when" boxes now met by editing the issue body, and say which ones you ticked.
