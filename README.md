# NES Emulator

A cycle-oriented NES emulator written in JavaScript. It runs as a single HTML page in any modern browser and is packaged as a Windows app with Electron.

## Features
- Cycle-stepped 6502 + per-dot PPU + APU (pulse x2, triangle, noise, DMC)
- Mappers: 0, 1, 2, 3, 4, 7, 66
- Accuracy: 135 / 147 tests of the [AccuracyCoin](https://github.com/100thCoin/AccuracyCoin) test ROM pass (latest ROM at the time of writing)
- Built-in TAS tools: record / play movies, frame advance, rewind, 10 save-state slots, piano-roll input editor, speed control
  - Movie formats: `.fm2` (FCEUX-compatible) and `.nestas` (for movies that start from a save state)

## Controls
| NES | Key |
|---|---|
| D-pad | Arrow keys |
| A / B | X / Z |
| Select / Start | Shift / Enter |

TAS hotkeys: `P` pause, `.` frame advance, `Backspace` rewind (hold), `F5` save state, `F7` load state, `0`-`9` choose slot.

## Run from source
    npm install
    npm start

You can also just open `index.html` in a browser, then load a `.nes` file (or drag it onto the page).

## Build the exe
    npm run dist

The portable exe appears in `dist/`.

## Release (GitHub Actions)
Pushing a tag that starts with `v` (for example `v1.0.2`) builds the Windows exe in the cloud and attaches it to a GitHub Release. Keep `version` in `package.json` equal to the tag so the file name matches.

## Notes
- ROM files are not included; use your own legally obtained ROMs. `*.nes` is git-ignored.
- AccuracyCoin is by 100thCoin (MIT) and is not bundled with this project.

## License
MIT
