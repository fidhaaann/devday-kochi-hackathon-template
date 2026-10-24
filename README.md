# DevDay Exchange Community Hackathon: Kochi

A repository template for participants at the 10–11 October 2026 hackathon. It contains event rules and documentation scaffolding; build your project from scratch at the event.

**[Event and registration on Luma](https://luma.com/z10nz8gp)** · **[Event rules](RULES.md)** · **[Agent instructions](AGENTS.md)**

## Event details

| Detail | Information |
| --- | --- |
| Venue | JAIN University, Kochi |
| Location | [Open the venue map](https://maps.app.goo.gl/Eme7gR7NDXSNRANu5) |
| Rooms | 2008 and 2009 |
| Check-in | 10 October 2026, 6:00 PM IST |
| Kick-off | 10 October 2026, 6:30 PM IST |
| Wrap-up | 11 October 2026, by 10:00 AM IST |
| Participation | Solo or a team of up to 4 participants |
| Theme | Open — build anything you like |

Keep your approved Luma QR code ready for entry, and bring your laptop and charger. Eligible checked-in participants will receive Codex credits and OpenAI API credits.

## Use this template

1. Select **Use this template → Create a new repository** on GitHub. Create your own project repository and clone it.
2. Read [RULES.md](RULES.md) and [AGENTS.md](AGENTS.md) before building. Begin project implementation at the event.
3. Fill in the project overview below as you build. Use any suitable language or framework, keeping the implementation simple.
4. Record meaningful changes in [CHANGELOG.md](CHANGELOG.md) and your Codex usage in [AI_USAGE.md](AI_USAGE.md). Commit after completed milestones; aim for a meaningful checkpoint about every 30 minutes.
5. Complete [SUBMISSION.md](SUBMISSION.md) with your code repository, short project description, and working demo. Follow submission instructions announced by the organizers.

This template has no application code or required technology stack. The documentation and commit cadence are repository workflow guidance; the event participation rules are in [RULES.md](RULES.md).

## Project overview — complete during the event

- **Project name:** Tancode
- **Short description:** A lightweight, local-first VS Code extension that explains the active source file — a concise summary, key declarations, and expandable detail — to help developers learn technical concepts while vibe coding without spending coding-agent credits. Imported from [fidhaaann/Tancode-](https://github.com/fidhaaann/Tancode-).
- **Team:** TODO — participant names and GitHub handles; maximum 4 members.
- **Working demo:** Local demo via the VS Code Extension Development Host — see "Run the project" below.
- **Technology stack:** TypeScript, VS Code Extension API (native webview panel), npm, `tsc`. No runtime dependencies; dev-only `typescript`, `@types/vscode`, `@types/node`.

### Run the project

1. Prerequisites and versions: Node.js 20+ and desktop VS Code 1.90+. `.npmrc` sets `engine-strict=true`, so an older Node fails fast.
2. Dependency installation: `npm ci` from the repository root.
3. Environment setup: none required. `.env.example` documents placeholder variables (`TANCODE_MODEL_ENDPOINT`, `TANCODE_MODEL`) reserved for a future local model runtime — no code reads them; copy to `.env` only if experimenting.
4. Start the project: `npm run compile`, then press F5 in VS Code to launch the Extension Development Host. In that window, open a source file and run `Tancode: Explain Current File` from the Command Palette. The `Tancode` panel opens beside the editor and follows the active tab.
5. Run checks or tests: `npm run typecheck`. `npm run watch` rebuilds on change.

### Current status

- Working features: `Tancode: Explain Current File` opens a `Tancode` webview panel beside the editor; it displays the active file's name/language, a generated summary, detected declarations (functions, classes, interfaces, components) for 15 languages, imports, and an expandable "More detail" section. It updates on tab switches and re-analyzes on edits. `Tancode: Hello World` remains as a sanity check.
- Known limitations: explanations are deterministic rule-based heuristics (line-based declaration patterns), not AI — they identify structures, they don't truly interpret behavior. Interactive webview verification on a desktop VS Code is pending; only compile/typecheck were run in the build environment. No AI model, selected-code explanations, or error explanations yet (roadmap).
- Libraries, APIs, and public datasets used: only the VS Code Extension API (`@types/vscode`); no external services.

See [AI_USAGE.md](AI_USAGE.md) for AI assistance and [CHANGELOG.md](CHANGELOG.md) for the development record.
