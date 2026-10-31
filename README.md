# Pour Decision

An installable wine app that learns each person's palate (red, white, rosé and sparkling), picks what to try next, pairs wine with food, tracks your wine rack, and scans wine lists and shop shelves.

## Install

Open the app's GitHub Pages link on your phone, then:

- **iPhone:** in Safari, tap Share → **Add to Home Screen**.
- **Android:** in Chrome, tap ⋮ → **Install app** (or **Add to Home screen**).

It updates itself whenever it's opened with a signal, and works offline.

## Your data

Ratings, notes, names and your rack are stored on your own phone (browser storage). Nothing is uploaded. Use **More → Save a backup file** now and then, and **Restore from a file** on a new phone.

## Claude features (optional)

Photo scanning and pairing unusual dishes use Claude. Add your own Anthropic API key under **More**. It is stored only on your phone and sent only to `api.anthropic.com`. Each scan costs a few pence.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `catalog.json` | Shared wine list (Lidl, Aldi, Tesco, Sainsbury's, The Wine Society) |
| `scout.json` | Weekly scout report |
| `sw.js` | Service worker: network-first, so updates arrive on next open; cached copy offline |
| `manifest.webmanifest`, `icon-*.png` | Install metadata and icons |

A weekly scheduled Claude task adds new wines to `catalog.json` and writes `scout.json`.
