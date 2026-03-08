# HAM RADIO 📡
### Lewis Hamilton · 2026 Season Team Radio

A clean, fast web app for browsing and listening to Lewis Hamilton's team radio communications during the 2026 Formula 1 season.

Built with vanilla HTML, CSS, and JavaScript. No frameworks, no build step, no API key required.

**[→ Live App](https://manicmig.github.io/ham-radio/)**

---

## Features

- **2026 season calendar** — browse every Grand Prix weekend as it happens
- **Session picker** — choose from Practice, Qualifying, Sprint, or Race sessions
- **Audio playback** — play actual radio clips with waveform visualiser, progress bar, and volume control
- **Auto-advance** — plays through messages in sequence automatically
- **Audio-only filter** — quickly filter to messages that have audio clips
- **Download** — save individual audio clips locally

---

## Data Source

All data is provided by the **[OpenF1 API](https://openf1.org)** — a free, open-source Formula 1 data API with no authentication required for historical data.

- Data available from the **2023 season onwards**
- Radio audio clips are a curated selection, not every communication
- New session data appears after each session completes

> OpenF1 is an unofficial project and is not associated with Formula 1 companies. F1, FORMULA ONE, FORMULA 1, FIA FORMULA ONE WORLD CHAMPIONSHIP, GRAND PRIX and related marks are trade marks of Formula One Licensing B.V.

---

## Running Locally

Because the app makes API calls to `api.openf1.org`, it must be served over HTTP — it won't work if you just open the HTML file directly in your browser (`file://`).

The easiest way is Python's built-in server:

```bash
# Clone the repo
git clone https://github.com/manicmig/ham-radio.git
cd ham-radio

# Serve it
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080)

Alternatively, use the [VS Code Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) and click **Go Live**.

---

## Deployment

The app is a single `index.html` file with no dependencies or build process, hosted on **GitHub Pages**.

To deploy your own fork:
1. Fork this repo
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch → main → / (root)**
4. Save — your site will be live at `https://YOUR-USERNAME.github.io/ham-radio/`

---

## Tech Stack

| Layer | Choice |
|---|---|
| Frontend | Vanilla HTML / CSS / JS |
| Data | [OpenF1 REST API](https://openf1.org/docs/) |
| Fonts | [Orbitron](https://fonts.google.com/specimen/Orbitron), [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono), [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) via Google Fonts |
| Hosting | GitHub Pages |

---

## Limitations

- OpenF1 provides a **curated selection** of radio clips, not every communication
- Session radio only appears after sessions have taken place
- Rate limit on OpenF1 free tier: 3 requests/second, 30 requests/minute

---

## Disclaimer

This project is unofficial and is not affiliated with, endorsed by, or associated with Formula 1, the FIA, Ferrari, or any F1 team. All F1-related trademarks belong to their respective owners.
