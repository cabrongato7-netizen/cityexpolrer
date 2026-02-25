# 🗺️ City Explorer — PWA (Progressive Web App)

A hybrid web app that works like a native app on **any phone** (Android, iPhone, desktop) — no app store needed.

---

## 📂 Files

```
CityExplorer-PWA/
├── index.html      ← The entire app (single file)
├── manifest.json   ← Makes it installable
├── sw.js           ← Service worker (offline support)
└── README.md
```

---

## 🚀 Option 1: Host on Netlify (Easiest — Free, 1 minute)

1. Go to **https://netlify.com** → Sign up free
2. Drag and drop the entire `CityExplorer-PWA` folder onto the Netlify dashboard
3. Netlify gives you a live URL like `https://city-explorer-xyz.netlify.app`
4. Open that URL on your phone → tap browser menu → **"Add to Home Screen"**

Done! Works offline, installs like a native app.

---

## 🚀 Option 2: GitHub Pages (Free, permanent URL)

1. Go to **https://github.com** → New repository → name it `city-explorer`
2. Upload all 3 files (`index.html`, `manifest.json`, `sw.js`)
3. Go to repo **Settings → Pages → Source: main branch → / (root)**
4. Your app is live at `https://yourusername.github.io/city-explorer`

---

## 🚀 Option 3: Open Locally (No hosting needed)

Just open `index.html` directly in Chrome on your phone:
- Copy the files to your phone
- Open with Chrome
- Note: service worker & install prompt need HTTPS (use Netlify/GitHub Pages for that)

---

## 📱 Install on Android

1. Open the hosted URL in **Chrome**
2. Tap the **3-dot menu** → "Add to Home Screen"
3. Or tap the **install banner** that appears automatically
4. The app icon appears on your home screen — works offline!

## 📱 Install on iPhone

1. Open the hosted URL in **Safari** (must be Safari, not Chrome)
2. Tap the **Share button** (box with arrow)
3. Scroll down → tap **"Add to Home Screen"**
4. Tap **Add**

---

## ✨ Features

| Feature | How it works |
|---------|-------------|
| 🔍 Venue Search | Foursquare API v3 (real data) |
| 🗺️ Map | Leaflet.js + OpenStreetMap (FREE) |
| 🚇 Transit | OpenStreetMap Overpass API (FREE) |
| 🎤 Voice Search | Web Speech API (device language) |
| 🔊 Voice Feedback | Web Speech Synthesis |
| ❤️ Favorites | localStorage (persists offline) |
| 📜 Search History | localStorage (last 50 searches) |
| 🔄 Offline Cache | Service Worker + localStorage |
| 🧭 Navigate | Opens Google Maps or Apple Maps |
| 📞 Call | Native phone dialer |
| 🔗 Share | Web Share API |
| ⬇️ Install | PWA install prompt |

---

## 🌍 Voice Language Support

The app auto-detects your phone's language and uses it for:
- Speech recognition (speaks your language)
- Text-to-speech feedback

No configuration needed!

---

## ⚙️ Customize API Key

Open `index.html` and find line:
```javascript
const FS_KEY = 'JC3Y12LOF4Q4WBYFXCTTXWRJ04JYY0TGLB5BPFFWR5WNZ1SG';
```
Replace with your Foursquare API key from https://developer.foursquare.com

---

*Map data © OpenStreetMap contributors | Transit © OpenStreetMap Overpass API | Venues © Foursquare*
