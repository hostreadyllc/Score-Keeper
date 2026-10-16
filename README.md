# Score Keeper

A scoreboard for 26 sports, each scored by its own rules. It is a plain web app with no build step and no outside dependencies: fonts and icons are bundled, and a service worker keeps it working offline. You can install it on a phone like an app.

## Sports

| Group | Sports | What it tracks |
| --- | --- | --- |
| Field | Soccer, American Football, Rugby Union, Rugby League, Australian Rules, Field Hockey, Lacrosse | Sport-specific point buttons, game clock, periods and overtime, cards and other counters |
| Court & ice | Basketball (NBA, FIBA, NCAA), Ice Hockey, Handball, Netball, Water Polo, Futsal | Same as above, with fouls, timeouts, shots and suspensions |
| Net & rally | Volleyball, Beach Volleyball, Badminton, Table Tennis, Squash, Pickleball | Set targets, win by 2, badminton's 30-point cap, table tennis serve rotation, pickleball side-out scoring |
| Racket | Tennis, Padel | 15/30/40, deuce and advantage or golden point, games, sets, 7- and 10-point tiebreaks |
| Bat & ball | Cricket (T20, ODI, T10, no limit), Baseball, Softball | Runs, wickets, overs and extras with target and required run rate; balls, strikes, outs, bases and line score |
| Individual & custom | Golf (9 or 18 holes), Custom Game | Scorecard against par for up to 6 players; free-form points and a timer |

## Features

- **Works offline.** After the first visit, everything is cached on the device. The home screen shows "Ready offline" once it is.
- **Installable.** On a phone, use "Add to Home Screen" (iPhone: Share menu; Android: browser menu or the install prompt).
- **Teams and players.** Tap "Edit teams & players" to rename teams and build a roster. Teams with players are saved on the device and can be loaded into any later game.
- **Credit scorers.** In timed team sports, pick a player before tapping a score and a scorers table builds up below the line score.
- Undo for every action
- Format options per sport, such as best of 3 or 5 sets
- The game in progress is saved on the device, so it survives a reload
- Light and dark themes that follow the device setting

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles and scoring logic |
| `sw.js` | Service worker that caches the app for offline use |
| `manifest.webmanifest` | App name, colors and icons for installing |
| `fonts/` | Barlow and Big Shoulders Display (SIL Open Font License) |
| `icons/` | App icons |

## Run it

Serve the folder over HTTP, for example `python3 -m http.server`, and open it in a browser. Opening `index.html` straight from disk also works, but offline caching needs HTTP or HTTPS.

## Updating

When you change any file, bump `VERSION` in `sw.js`. Installed copies then fetch the new files the next time they are online.
