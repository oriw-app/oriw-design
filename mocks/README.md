# Mocks

Screen designs for the Oriw app. Each screen is a plain HTML file you can open in a browser, plus a PNG of it. These files are the source of truth; any copy on a Claude canvas or elsewhere is only a preview.

## Settings

| Screen | HTML | Picture |
| --- | --- | --- |
| General: appearance, canvas, accessibility, language, updates, help | [general.html](settings/general.html) | [general.png](settings/general.png) |
| AI and agents: models, permissions, context, spending limit, other AI apps (MCP) | [ai-and-agents.html](settings/ai-and-agents.html) | [ai-and-agents.png](settings/ai-and-agents.png) |
| Privacy and security: what leaves the computer, anonymous data levels, locking, sharing, connections | [privacy-and-security.html](settings/privacy-and-security.html) | [privacy-and-security.png](settings/privacy-and-security.png) |

Decisions shown in these screens:

- **AI is optional and off-switchable.** One switch removes the agent, suggestions and connections from other AI apps.
- **Private jobs default to the model on this computer** (suggestions, summaries); the agent uses the model the user picks.
- **Deletes always ask.** Sending board content to a cloud model asks each time and shows which frames.
- **Other AI apps connect through the built-in MCP server**, off by default, only from the same computer, approved per app, read-only unless allowed (oriw#25).
- **Anonymous data has three levels:** Off, Basic (default: crash and stability reports, no ID) and Full (adds feature use and speed, with a resettable random ID). Board content, names, emails and IP addresses are never sent. Users can review each report before it's sent and see a log of everything sent.

Screens for the board editor, boards home, sharing and live sessions are still on the design canvas; they move here as each one is finalised.

## Updating a mock

Edit the HTML, then regenerate its PNG at 1440 px wide (full page) and commit both in the same pull request. Use tokens from `tokens.json` and the patterns in `components/settings.md`.
