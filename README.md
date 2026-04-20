# 🍹 Drink Tracker

A simple PWA to track alcohol consumption with daily, weekly, and monthly reports.

## Features

- **Four drink types**: Beer 🍺, Wine 🍷, Cocktail 🍸, Liquor 🥃
- **One-tap logging** with undo support
- **Reports**: Daily, weekly, and monthly breakdowns with bar charts
- **Offline support**: Works without internet once installed
- **Data stays on-device**: Uses IndexedDB — nothing sent to any server

## Deploy to GitHub Pages

```bash
cd ~/devel/alc-count
git init
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:rbowen/alc-count.git
git push -u origin main
```

Then on GitHub:

1. Go to **Settings → Pages**
2. Under "Source", select **Deploy from a branch**
3. Pick **main** / **/ (root)**
4. Save

Your app will be live at `https://rbowen.github.io/alc-count/` within a minute.

## Install on Phone

1. Open the URL in Chrome (Android) or Safari (iOS)
2. Tap the browser menu → **"Add to Home Screen"** / **"Install App"**
3. The app now has its own icon and runs full-screen, like a native app

## Local Testing

```bash
cd ~/devel/alc-count
python -m http.server 8080
```

Open `http://localhost:8080` in your browser. (Service worker requires HTTPS for full PWA features, but the app itself works fine over HTTP.)

## Data

All drink data is stored in the browser's IndexedDB. It persists across sessions but is tied to that specific browser. Clearing browser data will erase it.
