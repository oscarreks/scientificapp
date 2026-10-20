# Calc

A minimal scientific calculator with a scrolling history, built as an installable web app (PWA). No app store needed.

## Put it on GitHub Pages

1. Create a new repository on GitHub (e.g. `calc`). It can be public; on a free account, Pages requires a public repo.
2. Upload everything in this folder to the root of the repo (Add file → Upload files, drag the files *and* the `fonts` and `icons` folders in, then Commit).
3. In the repo go to **Settings → Pages**, set **Source: Deploy from a branch**, branch **main**, folder **/ (root)**, and Save.
4. After a minute the app is live at `https://<your-username>.github.io/<repo-name>/`.

## Install on Android

1. Open that URL in Chrome on your phone.
2. Tap the ⋮ menu → **Install app** (or **Add to Home screen**).
3. Launch it from the home screen: it opens full screen with no browser bar, and works offline.

## Updating

Edit or re-upload files on GitHub. The installed app checks for changes in the background, so the new version shows up the *second* time you open it after an update. If you ever need to force it, bump `CACHE = "calc-v1"` in `sw.js` to `calc-v2`.

## How it works

| Key | Tap | With ⇧ (shift) |
|---|---|---|
| sin / cos / tan | sin( cos( tan( | sin⁻¹ cos⁻¹ tan⁻¹ |
| √ | √( | x² |
| log | log( (base 10) | 10ˣ |
| ln | ln( | eˣ |
| π | π | e |
| C | delete last; **hold** to clear the line | AC: clear the whole history |
| (-) | negative sign | |

- Pressing an operator on an empty line continues from the previous answer.
- Tap a past **result** to insert it into the current line; tap a past **expression** to load it for editing.
- A faint live result appears while you type; missing closing brackets are added automatically.
- The **DEG / RAD** label in the top corner shows the angle mode; tap it (or use Settings) to switch.
- History and settings are saved on the device.
- On a computer you can type with the keyboard (Enter = equals, Backspace, Esc clears the line).

## Files

- `index.html`: the whole app (layout, styles, calculator logic)
- `manifest.webmanifest`: name, icons and "standalone" display mode for installing
- `sw.js`: service worker for offline use
- `fonts/mulish.woff2`: Mulish typeface (SIL Open Font License, see `fonts/OFL.txt`)
- `icons/`: home-screen icons
