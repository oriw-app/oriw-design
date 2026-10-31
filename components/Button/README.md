# Button

Text buttons for actions in panels, dialogs and toolbars, in four variants.

- **Primary** (`o-btn o-btn--primary`): the one main action of a panel or dialog. At most one per panel.
- **Secondary** (`o-btn--secondary`): the alternatives next to a primary.
- **Ghost** (`o-btn--ghost`): low-emphasis actions inside floating toolbars.
- **Danger** (`o-btn--danger`): destructive actions such as "End session for everyone" or the agent's Stop.

Height 36px (40–44px for a dialog's footer actions). Label in `body-strong`, sentence case, a verb first ("Back up now", not "Backup"). Hover and press use the shared state layers; keyboard focus shows a 2px `focus-ring`. Disabled: the `disabled` attribute, 40% opacity.

The consumer provides the label and any 16px icon (left of the label).
