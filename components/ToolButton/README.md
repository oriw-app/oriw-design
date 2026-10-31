# ToolButton

Icon-only 44px buttons for the canvas tool dock and floating toolbars.

Place them in an `o-dock` (bottom tool dock, `radius-xl`) or an `o-panel`. The active tool gets `is-active`: `accent-soft` background with `accent` icon — the only accent in the dock besides the Agent button.

Every ToolButton needs an `aria-label` that includes its shortcut ("Sticky note (N)") and a tooltip showing the same. Icons: 20px inline SVG, 2px stroke, `currentColor`. Use an `o-kbd` hint for keys next to text buttons (for example "Agent Ctrl I").

The consumer provides the icon, label and shortcut.
