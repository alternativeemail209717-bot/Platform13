# CRAFT platform (compact deploy build of UPDATE_175)

Same 6-file layout as before: `package.json`, `start.js`, `app.pack` (the whole platform, 100 games), `.env.example`, `.gitignore`, `README.md`.

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. First start prints `[launcher] unpacked N files`, `[TEAMARENA] Mounted ... 36 formats`, `[HANGMAN] Mounted ...` and 66 `[...] Mounted at /<game>` lines. Saved settings under `app/data/` are never overwritten.

## What's new in 175 (second verification pass, games 33-100)
- **Customize section rebuilt for Hangman and the 66 arcade games**: every button, the puzzle area, the board and the tiles can be hidden / resized / restyled, and every part was tested to really work on every page.
- Odd One Out difficulty is real (hint timing by level).
- Tested in a real browser: host buttons, Hangman controls, Team Arena host panel (307 controls), result windows on a 360 x 640 phone, animations, home page (100 cards), and a long run of all arcade games.

Details: `CHANGES_UPDATE_175.md` (in `app/` after the first start).
