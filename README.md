<div align="center">

<img src="https://img.shields.io/badge/version-2.0-C2185B?style=for-the-badge" />
<img src="https://img.shields.io/badge/static-no%20backend-00695C?style=for-the-badge" />
<img src="https://img.shields.io/badge/license-open%20source-880E4F?style=for-the-badge" />

# 🛡️ SafeRoute Bengaluru

**A crowd-sourced women's safety webapp for Namma Bengaluru**

*Interactive maps · SOS tools · Women-only transport · Smart route planning*
*— all in a single static HTML file, no login required.*

[🚀 **Live Demo**](https://akritichhaya.github.io/Safe_Route/Saferoute_bengaluru.html) &nbsp;·&nbsp; [⭐ Star on GitHub](https://github.com/akritichhaya/Safe_Route)

---

</div>

## 📌 Overview

SafeRoute Bengaluru is a browser-based safety tool designed for women and commuters in Bengaluru. It combines real crowd-sourced incident data, WhatsApp-powered alerts, night check-in timers, and women-only transport directories — entirely client-side with no server required.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🗺️ **Live Safety Map** | Interactive map with crowd-sourced hotspot markers at real BLR coordinates. Filter by time of day. |
| 🚨 **SOS Emergency Modal** | One-tap emergency with helplines, fake call trigger, WhatsApp alerts & live location sharing. |
| 🌙 **Night Check-In Timer** | Set a countdown — if you don't check in, an automatic SOS is sent to your contacts via WhatsApp. |
| 🚺 **Women-Only Transport** | Sakhi, Vanitha & more — curated women-only cab services with direct WhatsApp booking links. |
| 🏛️ **City Partner Alerts** | One-tap official alerts to BBMP, Bengaluru City Police, and BMTC directly from the app. |
| 🧭 **Safe Route Planner** | Route suggestions avoiding high-risk zones, with WhatsApp sharing and Google Maps integration. |
| 👍 **Community Reports** | Upvote or submit anonymous incident reports — session-only, nothing stored on any server. |

---

## 📁 Files

```
Safe_Route/
├── Saferoute_bengaluru.html   # Main app — all HTML, CSS, and JS in one file
└── README.md                  # Project documentation
```

---

## 🛠️ Tech Stack

- 🍃 **Leaflet.js** — interactive map rendering
- 💬 **WhatsApp API** — alerts, SOS, route sharing
- 📍 **Geolocation API** — live location detection
- 🗺️ **Google Maps** — route navigation
- 🔤 **Google Fonts** — UI typography
- 🌐 **No backend** — runs entirely in the browser

---

## 💻 Local Testing

Open `Saferoute_bengaluru.html` directly in your browser, **or** run a local server:

```powershell
# Navigate to project folder
Set-Location -Path 'D:\Safe_Route'

# Start local server
python -m http.server 8000
```

Then open in your browser:
```
http://localhost:8000/Saferoute_bengaluru.html
```

---

## 🚀 Deployment

This is a fully static site — deploy anywhere with **zero build steps**.

### GitHub Pages
1. Push project files to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to the root branch
4. Your site will be live at `https://<username>.github.io/<repo>/`

### Netlify / Vercel
1. Connect your GitHub repository
2. Deploy from the root folder
3. No build command required ✅

---

## ⚠️ Notes

> **Test Mode:** All helpline numbers are currently set to `9155647042` for safe testing. Update these before any production use.

- 🔒 100% anonymous — no login, no data stored on any server
- 📵 Session-only reports — nothing persists between browser sessions
- 📦 Leaflet.js and Google Fonts loaded from CDN
- 🌐 No backend server required

---

## 📜 License

Use and adapt this project freely for safety awareness and testing purposes.

---

<div align="center">

Built with 💜 for **Namma Bengaluru**

</div>
