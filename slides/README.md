# Slides

Marp slide decks for the seven sessions. Slides are intentionally **sparse** (one idea each, ~1 min/slide); the full 45-minute talk-track lives in the **speaker notes** (visible in presenter view and exported into the PPTX notes pane).

## Build

```bash
npm install                 # one-time: installs marp-cli locally
npm run all-pdf             # build every deck → dist/*.pdf
npm run all-pptx            # build every deck → dist/*.pptx (editable in PowerPoint/Google Slides)
npm run watch               # live preview in browser while editing
```

Single deck:
```bash
npm run pdf --deck=01-sell-anything
```

> **Note:** PDF/PPTX export renders through Chromium. A managed copy is auto-installed under `chrome/`. If export errors with "No suitable browser," run with `CHROME_NO_SANDBOX=true` and `CHROME_PATH` set to that binary (the build scripts handle this).

## Decks

| # | File | Title |
|---|------|-------|
| 1 | `01-sell-anything.md` | I Knocked on 500 Doors So You Don't Have To |
| 2 | `02-personal-finance.md` | The Money Waterfall |
| 3 | `03-calculated-risk.md` | Heads I Win, Tails I Don't Lose Much |
| 4 | `04-value-equation.md` | The Only Equation in Business That Matters |
| 5 | `05-incentives.md` | Show Me the Incentive, I'll Show You the Outcome |
| 6 | `06-leadership-under-pressure.md` | You Don't Rise to the Occasion |
| 7 | `07-build-ai-tool-live.md` | How I Cloned Myself With Claude |

Source outlines (the talk content these are built from) live in [`../sessions`](../sessions/).

## Style

- `themes/stef.css` — custom theme. Edit once, every deck updates.
- Slide classes: `lead` (title), `divider` (section break), `statement` (single big line).
