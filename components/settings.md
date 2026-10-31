# Settings patterns

How settings screens are built, as used in `mocks/settings/`.

| Pattern | Use it for | Rules |
| --- | --- | --- |
| **Section card** | A group of related settings | Title (16 px, bold) and an optional one-line description. White card, 14 px radius, 1 px border. |
| **Row** | One setting | Name (14 px, semibold) on the left, a one-line explanation under it when the name isn't enough, the control on the right. Rows wrap on narrow screens. |
| **Switch** | On or off, applied at once | A real `button` with `role="switch"` and `aria-checked`. Accent colour when on. Never use a switch for something that needs a confirm step. |
| **Segmented control** | Two to four short choices | Buttons with `aria-pressed` in a group with an `aria-label`. Labels of one to three words. |
| **Select** | Five or more choices, or long labels | A real `select` with a label. |
| **Choice card** | A choice that needs explaining, such as the anonymous data level | Radio inputs in a `fieldset`; each card lists exactly what the choice means. Mark the default with a pill. |
| **Status pill** | A current state (Connected, Basic, Only when you share) | Green for safe or private, neutral grey for informational, amber for waiting. Never red for a normal state. |
| **Danger button** | Actions that destroy data | Red text on white with a red border; always followed by a confirm dialog that names what will be lost. |

Writing rules:

- Say what the setting does, not how it works. "Lock when the computer sleeps", not "Session invalidation on suspend".
- Explain consequences where they matter: what leaves the computer, what can't be undone.
- Defaults favour privacy and safety; the explanation says why when that isn't obvious.
