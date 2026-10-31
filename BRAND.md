# Oriw

Calm, private canvas for thinking together. Oriw is an open-source, local-first whiteboard; its interface stays quiet so the board gets the screen.

**The short version:** a custom look in the spirit of Figma and Linear — dense, neutral, keyboard-first — built on Material-style rigor underneath: colour roles, tonal light and dark themes, state layers, and motion rules. Material's discipline, not its Android look.

## Principles

1. **The board is the hero.** Chrome floats, stays slim, and gets out of the way. No full-height sidebars by default; panels float `space-4` from the window edge on `surface` with `shadow-float`.
2. **One accent per view.** `accent` marks the single most important thing: the active tool, the primary action, the selection. Everything else is `ink`, `ink-muted` and `border`.
3. **Private by design, and say so.** Security states are visible but calm: a `success` pill ("Encrypted · Saved"), never alarm colours for normal states. `warning` is reserved for data leaving the device and approvals.
4. **Keyboard first.** Every tool shows its key. The `/` quick-create menu, Ctrl+K command palette and Ctrl+I agent are always one keystroke away.
5. **AI proposes, people decide.** Agent output appears as a preview (dashed `accent` outline, ghosts at reduced opacity) until applied. Destructive or outbound actions need approval.

## Voice

Plain, short, specific. Sentence case everywhere. Say what happened and what to do: "Backed up 2m ago", "Approval needed", "Agent suggests 2 action items — Tab to accept". No exclamation marks, no emoji, no jargon like "sync conflict resolution engine" in the UI.

## Colour

- **Grounds:** `canvas-bg` for the infinite canvas (with `canvas-dot` grid at `space-5` pitch), `surface` for anything floating, `surface-muted` for inputs and quiet boxes.
- **Text:** `ink` for primary, `ink-muted` for secondary. Both pass 4.5:1 on `surface` in light and dark.
- **Accent:** `accent` fill with `accent-ink` text for primary buttons; `accent-soft` with `accent-soft-ink` for active tools and selected rows.
- **Status:** `success`, `warning`, `danger`, each with a soft background where needed. Status colours always pair with a word or icon, never colour alone.
- **Stickies:** five paper colours (`sticky-yellow`, `-coral`, `-blue`, `-green`, `-lilac`) with `sticky-ink` text in both themes. In dark mode they dim slightly so they don't glare.
- **Presence:** `presence-1…3` for collaborator cursors and selections; `guide` only for snapping lines.

## Type

Inter for everything; JetBrains Mono for agent tool names, links and scopes. Load both from Google Fonts. Scale: `display` 30, `title` 18, `body` 14, `label` 13, `caption` 12, `overline` 11 (uppercase, tracked). Names and buttons use `body-strong`. Never below 11px.

## Layout and shape

- Spacing on a 4px base: `space-1` 4 → `space-8` 32.
- Radii: `radius-md` for controls, `radius-lg` for panels and cards, `radius-xl` for dialogs and the tool dock, `radius-pill` for status and avatars. Sticky notes are square-cornered paper.
- Touch targets ≥ 44px for tools and primary actions; dense 32–36px controls are fine inside panels.
- Elevation is shadow, not colour: `shadow-float` for panels, `shadow-popover` for menus, `shadow-sticky` only on stickies.

## States (the Material part)

Every interactive element uses the same overlay layers: `state-hover` on hover, `state-pressed` while pressed, and a 2px `focus-ring` outline at 2px offset for keyboard focus. Disabled = 40% opacity, no hover. This keeps states consistent across every surface and both themes.

## Motion

Purposeful and short. Durations: 120ms for hover and press, 200ms for panels and menus, 280ms for zoom-to and dialogs. Easing: standard `cubic-bezier(0.2, 0, 0, 1)`; exits use `cubic-bezier(0.3, 0, 1, 1)`. Canvas pan and zoom are never animated on direct input. Respect `prefers-reduced-motion`: replace movement with fades.

## Iconography

Inline SVG, 24px grid, 2px stroke (`currentColor`), round caps and joins, no fills except small dots. Shown at 16–20px. Icon-only buttons always carry an `aria-label` and a tooltip with the shortcut.

## Accessibility

Text 4.5:1 in every theme (3:1 for 24px+ and control borders). Colours that must be told apart also differ in lightness. Full keyboard navigation of the canvas: Tab through objects, arrows to nudge, Enter to edit. Respect OS high-contrast and reduced-motion settings.

## Don't

- Gradients, glows or glassy blurs as decoration.
- Full-height chrome that steals canvas width without a reason.
- More than one filled `accent` button in a panel.
- Material-style FABs, large elevated cards, or Android navigation patterns.
