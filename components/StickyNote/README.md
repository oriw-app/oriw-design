# StickyNote

The paper note at the heart of every board, in five colours with selected and AI-ghost states.

Default size 180 × 120 (grid-snapped; users resize freely). Text `body` in `sticky-ink` on every colour and theme; author and votes go in an `o-meta` line at the bottom. Square corners and `shadow-sticky` make it read as paper.

- Colour meaning is a convention, not a rule: yellow default, coral problems, blue actions, green wins, lilac ideas.
- **Selected** (`o-sticky--selected`): 2px `accent` outline at 3px offset, plus resize handles drawn by the canvas.
- **Ghost** (`o-sticky--ghost`): an AI suggestion not yet accepted — 55% opacity with a dashed `accent` outline. Tab accepts, Esc dismisses.

On the canvas, collaborators' selections use their `presence-*` colour instead of `accent`.
