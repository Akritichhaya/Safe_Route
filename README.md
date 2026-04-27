# SafeRoute Bengaluru

## Overview
Demo Link : https://akritichhaya.github.io/Safe_Route/Saferoute_bengaluru.html

SafeRoute Bengaluru is a browser-based safety webapp designed for women and commuters in Bengaluru. It provides interactive safety information, emergency support, women-only transport options, city partner alerts, and safe route guidance — all in a single static HTML file.

## Features

- Interactive Bengaluru safety map with hotspot markers
- SOS emergency modal with test helplines and WhatsApp alert options
- Women-only transport services with WhatsApp contacts for safe booking
- BBMP / Police / BMTC alert cards for fast city reporting
- Safe route planner with route sharing over WhatsApp
- Mobile-friendly layout and accessible UI design

## Files

- `Saferoute_bengaluru.html` — main application file containing HTML, CSS, and JavaScript
- `README.md` — project documentation

## Local Testing

1. Open `Saferoute_bengaluru.html` directly in your browser.
2. Or run a local server from the project folder:
   ```powershell
   Set-Location -Path 'D:\Safe_Route'
   python -m http.server 8000
   ```
3. Open the page in your browser:
   `http://localhost:8000/Saferoute_bengaluru.html`

## Deployment

This is a static website. You can deploy it to any static hosting service such as:

- GitHub Pages
- Netlify
- Vercel

### GitHub Pages

1. Create a GitHub repository.
2. Push the project files to GitHub.
3. Enable Pages from the repository settings using the root branch.

### Netlify / Vercel

1. Connect the GitHub repository.
2. Deploy the site from the root folder.
3. No build step is required.

## Notes

- All contact/test phone numbers are currently configured to `9155647042` for safe testing.
- The app uses Leaflet.js and Google Fonts from CDN.
- No backend server is required; the app runs entirely in the browser.

## License

Use and adapt this project freely for safety awareness and testing purposes.
