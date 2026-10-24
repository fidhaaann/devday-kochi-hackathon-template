# Change log

Record each meaningful project change during the event, newest first. Update this file in the same commit as the change. Use a real timestamp with timezone, for example `YYYY-MM-DDTHH:MM:SS+05:30`.

## Event build log

## 2026-10-24T21:00:00+05:30 — Imported Tancode VS Code extension scaffold and Milestone 1

- Changed: Added the Tancode project into this template repository: `package.json`, `package-lock.json`, `tsconfig.json`, `src/extension.ts`, `src/analysis.ts`, `src/explanationPanel.ts`, `scripts/preflight.js`, `.npmrc`, `.vscode/launch.json`, `.vscode/tasks.json`, `.vscodeignore`, `.env.example`; merged Tancode ignore rules into `.gitignore`; filled the README project overview and run steps.
- Why: Consolidate the Tancode project (developed in `fidhaaann/Tancode-`) into the hackathon template repository so this repo is the project workspace. Note: the extension predates the event window — imported post-event per repository owner request, not built from scratch at the event.
- Validation: `npm ci` clean install, `npm run compile`, `npm run typecheck` all pass on Node 20; analyzer smoke-tested on sample TypeScript/Python documents. Interactive Extension Development Host (F5) test not run — no desktop VS Code in the build environment.
- Limitations: Rule-based explanations only (no AI). F5/webview verification and `SUBMISSION.md` participant details remain for the repository owner.

## Template setup — 10 October 2026

- Changed: Added the event README, rules, agent guide, change log, AI usage record, submission checklist, Git ignore rules, and pull request checklist.
- Why: Give participants a consistent starting point for event rules, basic coding patterns, documented changes, and regular commits.
- Validation: Checked local Markdown links, event detail consistency, required documents, and diff whitespace before publishing.
- Limitations: Documentation scaffolding only; no participant project, application, or working demo is included. GitHub publication and template status are verified separately after creation.
