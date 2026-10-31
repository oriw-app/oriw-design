# AgentStep

One row in the AI agent's step log, showing a board tool call and its state.

Stack rows in an `o-panel` with no padding. Three states: **done** (`o-step--done`, `success` check), **running** (`o-step--running`, `accent-soft` row, `accent` dot) and **to do** (`o-step--todo`, grey mark). The tool name uses `code` (JetBrains Mono) in `accent-soft-ink`; the description is one line in `ink-muted`, truncated with an ellipsis.

Only one row runs at a time. Steps that need approval (deletes, data leaving the device) stop the log and show an approval card in `warning-soft` beneath the running row.
