# CRAFT platform (compact deploy build of UPDATE_174)

Same 6-file layout as before: `package.json`, `start.js`, `app.pack` (the whole platform, 100 games), `.env.example`, `.gitignore`, `README.md`.

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. First start prints `[launcher] unpacked N files`, `[TEAMARENA] Mounted ... 36 formats`, `[HANGMAN] Mounted ...` and 66 `[...] Mounted at /<game>` lines. Saved settings under `app/data/` are never overwritten.

## What's new in 174 (verification pass of games 33-100)
- Every setting of every game from Team Arena to #100 was tested (all values), the Settings window of all 67 pages was tested in a browser (change, Save & Apply, reload), all host controls were tested, bots and typed answers work in all 66 arcade games in Test mode, and every Team Arena option of every format was run with bots.
- **Team Arena now fits one phone screen** (no page scrolling), and the arcade games fit small Android phones (360x640 up to 412x915).
- Fixed: Word Search could loop on a category without enough words.

Details: `CHANGES_UPDATE_174.md` (in `app/` after the first start).
