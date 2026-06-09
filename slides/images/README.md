# Images

Drop-in slots for slides. Decks reference these paths; add the files and rebuild.

## Already included
- `verizon.png` — Verizon logo (deck 1, door-to-door slide)
- `influence-cover.jpg` — Cialdini *Influence* cover (deck 1, Part 4 divider)

## You need to add (slides reference these; placeholders until added)
| File | Deck | What to capture |
|------|------|-----------------|
| `tesla-roadster-reserve.png` | 1 (Pre-sells) | Screenshot of `tesla.com/roadster/reserve#payment` showing the Roadster + "$5,000 due today". Then add `![bg right:42% fit](images/tesla-roadster-reserve.png)` to that slide. |
| `pabrai-berkshire.jpg` | 3 (Pabrai) | Your photo with Mohnish Pabrai at the Berkshire Hathaway shareholder meeting. |
| `gonupoc-youtube.png` | 7 (gonupoc) | Thumbnail/screenshot of your gonupoc.com YouTube video. |

## Optional upgrade
| File | Deck | Idea |
|------|------|------|
| `liking-kiosks.png` | 1 (Liking) | Two fruit kiosks — one smiling clerk, one frowning — to replace the 😊 emoji. |

After adding a file, rebuild: `npm run pdf --deck=01-sell-anything` (or `npm run all-pdf`).
