# COOS Auditorium Count

Sunday attendance counting tool for the Church of Our Saviour main auditorium
(Singapore) — 主日华语崇拜 2:00pm · Sunday Chinese Service.

**Open it:** https://davidowh.github.io/coos-attendance-count/

## How it works

An usher counts one section of the auditorium with a hand clicker, types that
single number into the app, and the app totals everything up. Twelve sections,
twelve numbers, grouped into three passes:

| Pass | Where | Sections | Seats |
|-----:|-------|---------:|------:|
| 1 | From the Level 2 balcony rail | 5 | 632 |
| 2 | Walk down — under the balcony | 4 | 204 |
| 3 | Back upstairs — Level 2 | 3 | 340 |
| | **Whole auditorium** | **12** | **1176** |

## Seat figures

Every section capacity is the sum of per-row seat counts read off *Floor Plan
of Main Auditorium* (updated 2022-08-25): **Level 1 836 + Level 2 340 = 1176**,
reconciling exactly with the totals printed on that plan. Note there is no row
I (too easily read as a 1) — J follows H; row U appears only in the right-side
block.

If the chairs are ever re-laid out, the per-row figures in `BLOCKROWS` inside
`index.html` are the single place to update.

## Privacy

No attendance data is stored in this repository or sent anywhere. Counts live
in the browser's own local storage on whichever phone did the counting, and
leave it only when someone exports the CSV or copies the WhatsApp summary.

## Notes

- Single self-contained HTML file. No build step, no dependencies to install.
- Works offline once loaded. Fonts come from Google Fonts and fall back to
  system faces when there's no connection.
- Bilingual 中文 / English, switchable in the top-right corner.
