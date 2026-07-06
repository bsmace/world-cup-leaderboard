# FIFA 2026 Office Pool Leaderboard

## Overview
Dynamic glassmorphism leaderboard page for an internal office World Cup sweepstake. Displays 91 players with their drawn nations and cumulative points across Group Stage + Round of 32.

## Brand Colors
- **Gold** `#FDB824` — trophy glow, champion accent, highlight sheen
- **Teal** `#00929F` — glass edges, accent text, secondary UI elements
- **Background** — dark (`#0A0E1A` → `#111827`) with radial glows

## Rank Layout (Round of 32 standings)
| Position | Players | Points | Display |
|----------|---------|--------|---------|
| 1st | Khaled Gharib | 24 | Single podium card with crown + gold glow |
| 2nd (joint) | Nur Aksari, Isaac Ackom-Mensah, Abdul Wadood | 22 | Shared silver card |
| 3rd | Shinan Zhang | 21 | Bronze card |
| 4th (joint) | Danilo Arba, Rishi Parekh | 20 | Teal-accented tier card |
| 5th | Marissa Canete | 19 | Teal-accented tier card |
| 6th (joint) | Ermelinda Dedej, Yusuf Mahmood, Mohamed Hassan | 18 | Teal-accented tier card |
| 7th+ | Remaining players (17 → 2 pts) | — | Honorable mentions grid, grouped by score descending |

## Features
- Glassmorphism design with blur overlays and gold/teal accents
- Search bar to filter players by name or nation
- Animated count-up numbers
- Confetti animation for champion section
- Player detail modal on click (chit #, per-round breakdown, flag icons)
- Inline emoji flags for all nations
- Fully responsive (mobile-first)
- Dark theme

## Data Source
`FIFA_2026_Chit_Tracking updated.xlsx` → extracted to `data.json`:
- Group Stages: chit #, player name, combined pair, team 1 pts, team 2 pts, total
- Round of 32: adds R32 points per team (3 if advanced, null if not)

## Deploy
Static site → Vercel (git push)

## Out of Scope
- Live score fetching (manual data refresh)
- Authentication
- Backend database
