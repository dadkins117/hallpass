# Hall Pass — Classroom Tool

A simple, offline-capable hall pass tracker that runs in any modern browser. Built as a single-folder web app you can host on GitHub Pages, Netlify, or any static host.

## Files

- `index.html` — the app itself
- `manifest.json` — declares the app's name, icons, and install behavior
- `sw.js` — service worker that caches files for offline use
- `icon-*.png` and `apple-touch-icon.png` — app icons

## To use locally on a laptop

1. Download or copy the whole folder somewhere stable on your computer
2. Double-click `index.html` to open in your browser
3. Note: from a local file (`file://...`), some PWA features won't work — the service worker won't register, and "Install as app" won't be available. The app still works fine, but for the full experience, host it (see below).

## To host on GitHub Pages (free, ~10 minutes)

This gives you a permanent URL like `yourusername.github.io/hallpass` that works on any device, including iPad.

1. Create a free account at github.com if you don't have one
2. Create a new repository — name it whatever you like (e.g. `hallpass`)
3. Make sure it's set to "Public" (required for free GitHub Pages)
4. Upload all the files in this folder to the repo (use the "uploading an existing file" link on a fresh repo, or drag and drop)
5. Go to the repo's **Settings** → **Pages**
6. Under "Source", pick `main` (or `master`) branch and `/ (root)` folder, save
7. Wait 1-2 minutes — GitHub will give you a URL like `https://yourusername.github.io/hallpass/`
8. Open that URL on any device and use the app

To update the app later, just upload new files to the same repo. The site updates automatically.

## To install as an app

### On Chrome/Edge (laptop)
- Open the URL
- Look for an install icon in the address bar (small monitor or download arrow), or open the menu (⋮) and pick "Install Hall Pass"

### On iPad/iPhone (Safari)
- Open the URL in Safari
- Tap the Share button (square with up arrow)
- Tap "Add to Home Screen"
- Tap "Add"

### On Android (Chrome)
- Open the URL
- Tap menu (⋮), then "Install app" or "Add to Home screen"

## Backups

The app saves backups in two ways:

**Manual backup folder (Chrome/Edge desktop):** In Setup, click "Pick backup folder" once and choose a folder inside your OneDrive or Google Drive (something like `OneDrive/Hall Pass Backups`). After that, every backup writes directly to that folder. Since OneDrive/Drive sync that folder to the cloud automatically, your backups are everywhere.

**Auto-backup at end of school day:** Once a folder is set, the app automatically saves a backup every day around 4pm (configurable). No clicks needed.

**On iPad/Safari/Firefox:** these browsers don't support the folder picker, so backups download to your Downloads folder. You can manually drag those into OneDrive, or configure your browser to point Downloads at a synced folder.

To restore on a new device, install the app there and use "Restore from backup" with the most recent JSON file. The app reminds you when your last backup is over a week old.

## Privacy

All your data lives only in your browser, on the devices where you've installed or visited the app. Nothing is sent to any server. The only network requests the app makes are to load fonts and the QR-code scanner library on first run.
