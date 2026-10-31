# Oriw logo

The mark is a ring with a centre point: a board seen from far away, and the one idea you are focused on.

| File | Use |
| --- | --- |
| `oriw-icon.svg`, `png/oriw-icon-*.png` | App icon for Windows and Linux, plus favicons (16 to 1024 px) |
| `oriw-icon-macos.svg`, `png/oriw-icon-macos-1024.png`, `png/oriw.icns` | macOS app icon, drawn on Apple's 824 px plate with a shadow |
| `png/oriw.ico` | Windows icon (16 to 256 px in one file) |
| `png/apple-touch-icon.png` | iPhone and iPad home-screen icon for the website (180 px) |
| `oriw-avatar.svg`, `../github/oriw-org-avatar-500.png` | GitHub organisation avatar (full bleed, GitHub rounds the corners) |
| `github/oriw-social-preview-1280x640.png` | Repository social preview card |
| `oriw-wordmark.svg`, `oriw-wordmark-white.svg` | Mark plus name, for light and dark backgrounds; text is outlined, no font needed |
| `oriw-glyph.svg` | Ring and dot only, uses `currentColor` for inline UI |
| `favicon.svg` | Website favicon |

For the Tauri app, run `cargo tauri icon logo/png/oriw-icon-1024.png` to generate every platform size.

## Rules

- Ink `#1d1d1f` plate with a white mark, or the reverse. No other colours, gradients or effects on the mark.
- Keep clear space equal to the dot's diameter on every side.
- Do not stretch, rotate, outline or add text inside the plate.
