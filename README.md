# World Cup 2026 Sweepstake

A self-contained single-page sweepstake tracker. No build step, no backend — just one `index.html`.

## What it does
- Draw: enter players, share out all 48 teams evenly
- Players: who has which team, struck out as teams go
- Teams: set how far each team reached, knock teams out, goal tallies
- Fixtures: all 104 matches (UK kick-off times), enter scores, "Today" filter
- Tables: group standings build automatically from scores
- Leaderboard: live points per player
- Prizes: pot/entry-fee split with automatic payouts
- Export PNG cards + snapshot share links

## Deploy to Vercel

### Option A — GitHub (recommended)
1. Create a new GitHub repo (e.g. `world-cup-sweepstake`).
2. Upload `index.html` (Add file → Upload files → Commit).
3. In Vercel: Add New → Project → import the repo → Deploy.
4. Leave all build settings empty/default — it's a static site.
5. Future edits committed to GitHub auto-redeploy.

### Option B — drag & drop
1. vercel.com → new project → deploy a folder.
2. Drag this folder (containing `index.html`) in. Done.

## Notes
- Data is saved in the browser (`localStorage`) and persists once it's on a real `https://` URL.
- It saves per-browser/device — best run from one device you update. Live multi-user sync + auto-pulled scores would need a small backend (Vercel KV + a serverless function holding a football-data API key).
