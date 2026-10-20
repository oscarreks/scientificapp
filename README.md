# Calc

A minimal scientific calculator with a scrolling history, built as an installable web app (PWA). No app store needed.

## Install on Android

1. Open that URL in Chrome or Firefox on your phone.
2. Tap the ⋮ menu → **Install app** (or **Add to Home screen**).
3. Launch it from the home screen: it opens full screen with no browser bar, and works offline.

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
- Tap anywhere in your current equation to move the cursor.
- Tap a past **result** or **expression** to insert it into the current expression at the cursor.
- If the past expression is being inserted in the middle of the current equation, it will gain **brackets** so it keeps its own meaning. 
- Toggle Live Answer if you want a faint live result to appear while you type; missing closing brackets are added automatically.
- The **DEG / RAD** label in the top corner shows the angle mode; tap it (or use Settings) to switch.
- History and settings are saved on the device.
- On a computer you can type with the keyboard (Enter = equals, Backspace, Esc clears the line).

## Files

- `index.html`: the whole app (layout, styles, calculator logic)
- `manifest.webmanifest`: name, icons and "standalone" display mode for installing
- `sw.js`: service worker for offline use
- `fonts/lexend.woff2`: Lexend typeface
- `fonts/mulish.woff2`: Mulish typeface (SIL Open Font License, see `fonts/OFL.txt`)
- `icons/`: home-screen icons
