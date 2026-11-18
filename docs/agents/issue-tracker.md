# Issue tracker: GitHub

Issues and specs for this repo live as GitHub issues in `HBhgs178/-` (https://github.com/HBhgs178/-). Use the `gh` CLI for all operations.

## Conventions
- **Create an issue**: `gh issue create --title "..." --body "..."`. Use a heredoc for multi-line bodies.
- **Read an issue**: `gh issue view <number> --json number,title,body,labels,comments`.
- **List issues**: `gh issue list --state open --json number,title,body,labels,comments` with appropriate `--label` and `--state` filters.
- **Comment on an issue**: `gh issue comment <number> --body "..."`
- **Apply / remove labels**: `gh issue edit <number> --add-label "..."` / `--remove-label "..."`
- **Close**: post the explanation with `gh issue comment <number> --body "..."`, then `gh issue close <number>`.
- Infer the repo from `git remote -v`; `gh` does this automatically when run inside a clone.
- File issues only into this user's own repo (`HBhgs178/-`). Never file into `mattpocock/skills` (the repo these skills come from). Before the first `gh issue create` of a session, check the target with `gh repo view --json nameWithOwner` and confirm with the user if it is not their repo.

## Environment notes
- Installed `gh` is version 2.4.0 (old). Native sub-issue and blocked-by commands are not available; use fallback body lines: `Part of #<parent>` and `Blocked by: #<n>`.
- The stored token carries the `repo` scope only; `gh auth status` may warn about a missing `read:org` scope. That warning does not block issue/PR operations on this personal repo.

## Pull requests as a triage surface
**PRs as a request surface: no.** (Set to `yes` if this repo treats external PRs as feature requests.)

## When a skill says "publish to the issue tracker"
Create a GitHub issue.

## When a skill says "fetch the relevant ticket"
Read it as in **Read an issue** above.
