# Oriw design system: notes for Claude

This repository is the single source of truth for Oriw's look: `tokens.json` (colours, type, spacing, radius, shadows), components in `components/`, brand rules in `BRAND.md`, and the logo kit in `logo/`.

## Rules for this repo

- Change a token here first; then update the app (`oriw/ui`) and the website (`oriw.app`) in linked pull requests.
- The website is light theme only. The app follows the system's light or dark setting.
- Every colour pair used for text must meet WCAG 2.1 AA contrast; check before adding one.
- Logo rules are in `logo/README.md`: ink plate with a white mark or the reverse, nothing else.

## How we work

This repository uses the **issuewright** plugin from [oriw-app/dev-plugins](https://github.com/oriw-app/dev-plugins), switched on in `.claude/settings.json` and configured in `.claude/issuewright.json`. GitHub issues are the spec; the owner accepts intent, spec and plan; work follows DDD + BDD + TDD with hexagonal architecture and CQS. The full guide is the plugin's `WORKFLOW.md` (the `issuewright` skill). Releases are the milestones in `oriw`; planning happens on the **Oriw Roadmap** project.

## Oriw rules
- **DDD + BDD + TDD, with hexagonal architecture and strict CQS**, as set out in `oriw/docs/ENGINEERING.md` and `oriw/docs/ARCHITECTURE.md`. Here that means acceptance criteria in issues are written as Given / When / Then, design words match the glossary in `oriw/docs/DOMAIN.md`, and every token change comes with a check (such as text contrast) that would fail if the rule broke.
- Never commit secrets. Never put salaries, costs, revenue or customer names in a public repository; they belong in `oriw-company`.
- The repositories are the source of truth: designs in `oriw-design/mocks/`, decisions in the repository they affect. Claude artifacts are previews only.
- Commits are authored by the person running the session; keep the trailers the session adds.

## Things Claude gets wrong

- Nothing recorded yet. Add a line here whenever Claude makes the same mistake twice.
