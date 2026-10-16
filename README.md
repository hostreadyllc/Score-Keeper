# Score Keeper

A scoreboard for 26 sports, each scored by its own rules. It is a single `index.html` file with no build step and no dependencies beyond Google Fonts.

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

- Undo for every action
- Editable team and player names
- Format options per sport, such as best of 3 or 5 sets
- The game in progress is saved in the browser, so it survives a reload
- Light and dark themes that follow the device setting
- Works on phones

## Run it

Open `index.html` in a browser. To publish it with GitHub Pages, go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
