# HAM RADIO 📡
### F1 Team Radio Archive

A fast, clean web app for browsing and listening to Formula 1 team radio communications. Browse every driver's radio messages across all sessions — practice, qualifying, sprint, and race — with live polling during race weekends.

Built with vanilla HTML, CSS, and JavaScript. No frameworks, no build step, no API key required.

**[→ Live App](https://your-netlify-url.netlify.app)**

---

## Features

- **All drivers** — every driver OpenF1 has data for, from 2023 to present
- **Full calendar** — browse by season (2023–2026), select any Grand Prix weekend, then choose a session
- **Audio playback** — play actual radio clips with waveform visualiser, progress bar, and volume control
- **Auto-advance** — plays through messages in sequence automatically
- **Live mode** — polls for new radio messages every 15 seconds during active sessions
- **Team colours** — UI accent colour updates to match the selected driver's team
- **Audio-only filter** — quickly filter to messages that have audio clips
- **Download** — save individual audio clips locally

---

## Data Source

All data is provided by the **[OpenF1 API](https://openf1.org)** — a free, open-source Formula 1 data API with no authentication required for historical data.

- Data available from the **2023 season onwards**
- Radio audio clips are a curated selection, not every communication
- Live data is available during and shortly after active sessions

> OpenF1 is an unofficial project and is not associated with Formula 1 companies. F1, FORMULA ONE, FORMULA 1, FIA FORMULA ONE WORLD CHAMPIONSHIP, GRAND PRIX and related marks are trade marks of Formula One Licensing B.V.

---

## Running Locally

Because the app makes API calls to `api.openf1.org`, it must be served over HTTP — it won't work if you just open the HTML file directly in your browser (`file://`).

The easiest way is Python's built-in server:

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/f1-radio.git
cd f1-radio

# Serve it
python3 -m http.server 8080
```

Then open [http://localhost:8080/hamilton-radio.html](http://localhost:8080/hamilton-radio.html)

Alternatively, use the [VS Code Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) and click **Go Live**.

---

## Deployment

The app is a single HTML file with no dependencies or build process. It can be deployed anywhere that serves static files.

**Netlify** (recommended)
1. Fork or clone this repo
2. Connect to Netlify via **Import an existing project**
3. Leave build settings blank — Netlify serves the file directly
4. Deploy

---

## Tech Stack

| Layer | Choice |
|---|---|
| Frontend | Vanilla HTML / CSS / JS |
| Data | [OpenF1 REST API](https://openf1.org/docs/) |
| Fonts | [Orbitron](https://fonts.google.com/specimen/Orbitron), [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono), [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) via Google Fonts |
| Hosting | Netlify |

---

## Limitations

- OpenF1 provides a **curated selection** of radio clips, not every communication that takes place
- Audio clips may occasionally be unavailable due to CORS restrictions on certain browsers
- 2026 calendar data is available but session radio will only appear after sessions have taken place
- Rate limit on OpenF1 free tier: 3 requests/second, 30 requests/minute

---

## Contributing

Pull requests welcome. If you find a bug or have a feature idea, open an issue.

---

## Disclaimer

This project is unofficial and is not affiliated with, endorsed by, or associated with Formula 1, the FIA, or any F1 team. All F1-related trademarks belong to their respective owners.
