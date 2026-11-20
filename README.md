# CRAFT platform (compact deploy build of UPDATE_171)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (50 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena - 36 formats`, `[HANGMAN] Mounted ...` and 16 `[...] Mounted at /<game>` lines.
   Saved settings under `app/data/` are never overwritten.

## What's new in 171
1. **TEAM ARENA merged from your 3 builds (Platform8 / 9 / 10) - 26 -> 36 formats, nothing removed.** Base = Platform10 (newest core). Ported in: Codedle, Shapedle, Colorblindle, Colordle, Structle, Comparable, Linedle duels, Category Rush, ~200 more trivia questions and 3 more question types (number sequences, missing letters, EN/BM/ID vocabulary). Duplicates (Boxdle Word Hunt, Flagle Showdown, Numberblindle / PIN Breaker, Duel, Bracket, Last Letter) use the best version.
2. **New Team Arena formats:** Royal Rumble Quiz (free-for-all elimination) and Hangman Showdown (unlimited tries, Word Shuffle categories).
3. **HANGMAN** (`/hangman/`): built on Word Shuffle, viewers type letters or the whole answer, unlimited tries, Word Shuffle categories as answers.
4. **16 new games:** Emoji Decoder, Missing Vowels, Odd One Out, Math Frenzy, Number Hunter, Chat Quiz, Majority Rules, Word Chain, Word Search Live, Speed Typer, Higher or Lower, Simon Chat, Riddle Night, Name It!, Quick Draw, Lucky Wheel - each with the platform look and the full organised Settings window.

Full details: `CHANGES_UPDATE_171.md` (inside the pack, in `app/` after the first start).
