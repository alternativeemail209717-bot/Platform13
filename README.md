# CRAFT platform (compact deploy build of UPDATE_172)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (80 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. First start prints `[launcher] unpacked N files`, `[TEAMARENA] Mounted ... 36 formats`, `[HANGMAN] Mounted ...` and 46 `[...] Mounted at /<game>` lines. Saved settings under `app/data/` are never overwritten.

## What's new in 172 - 80 games
- **Every arcade game is now individual play**: no voting, nobody acts as "the whole chat", and no instant-reaction controls (TikTok chat delay is accounted for).
- **Removed / replaced (broke those rules):** Chat Quiz, Majority Rules, Higher or Lower, Number Hunter, Word Chain, Quick Draw, Lucky Wheel.
- **37 new games:** Trivia Rush, Capital Quest, Flag Rush, Where in the World, Neighbor Rush, Country Detective, Mystery City, Translate It, Element Rush, Estimate It, Survey Says, Word Bomb, Cipher Crack, Mirror Words, Letter Math, Spell Check, Typo Hunter, Finish the Saying, Common Link, Sentence Scramble, Alphabet Category, Memory Lane, Countdown Numbers, Pattern Master, Number Detective, Operator Puzzle, Roman Rush, Base Camp, Convert It, Time Warp, Day Finder, Percent Power, Emoji Equations, Robot Path, Count It, Odd Emoji, Missing Piece.
- Kept from 171: TEAM ARENA (36 formats), Hangman, Emoji Decoder, Missing Vowels, Odd One Out, Math Frenzy, Word Search Live, Speed Typer, Simon Chat, Riddle Night, Name It!.
- Every new game has the platform look, the organised Settings window, test mode, Offline box, Autopilot and HOME support.

Full details: `CHANGES_UPDATE_172.md` (in `app/` after the first start; also `CHANGES_UPDATE_171.md`).
