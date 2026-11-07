# Tariff Wars — a VRG game

Open your deals, the highest tariff wins. A card game for four seats: play against the AI or host a table for friends online.

**Play it free:** https://play.vrg.li/play/tariff-wars/

Free to copy, remix and republish under [LICENSE.md](LICENSE.md). The one condition: keep a
visible "A VRG game" credit linking to https://play.vrg.li.

## Fork it

1. Click **Fork** at the top of this page (or download the ZIP from the green **Code** button).
2. Clone your fork: `git clone https://github.com/<you>/tariff-wars.git`
3. Open `game/index.html` from any static server, for example
   `cd tariff-wars/game && python3 -m http.server 8000`, then visit http://localhost:8000.

## What is in here

- `game/` is the browser client: plain HTML, CSS and JavaScript, nothing to build.
- `relay/` is the multiplayer table server (a Cloudflare Durable Object over plain WebSockets); the client expects it at `/mp-socket`. Without it, solo play against the AI still works.

## Inside the Play site and on its own

On https://play.vrg.li the game runs fully inside the Play site, which adds a few shared
scripts from the site root (`/vg.js` play statistics, `/nick.js` player name, `/env.js`)
plus sign-in, saved progress and the leaderboard. Standalone, the game works without them: those
requests simply 404 and the game skips them.

More VRG games: https://github.com/vrgli/games
