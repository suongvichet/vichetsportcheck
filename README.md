# ⚽🏎️ Sportcheck — World Cup & Formula 1 Dashboard

A friendly, single-file sports dashboard that runs entirely on GitHub Pages. No backend, no build step. Live driver/constructor standings and the full F1 calendar, plus World Cup group tables, results, and fixtures — all with flags, team colors, and stat cards.

## Data sources

| Sport | What it shows | API | Key needed? |
|-------|---------------|-----|-------------|
| Formula 1 | Driver & constructor standings, race calendar with winners | [Jolpica F1 API](https://github.com/jolpica/jolpica-f1) | No — free, open |
| World Cup | Group standings, results, fixtures | [football-data.org](https://www.football-data.org/) | Yes — free tier |

> Note: F1 uses Jolpica, the community-maintained successor to the old Ergast API (which has shut down). Same URL structure, still free, no key.

## Setup in 4 steps

### 1. Get a free World Cup API key
- Register at [football-data.org/client/register](https://www.football-data.org/client/register)
- Copy your API key

### 2. Add the key to the file
Open `index.html`, find this line and paste your key in:
```js
const FD_KEY = 'YOUR_API_KEY';
```

### 3. Upload to GitHub
- Create a new **public** repository (e.g. `sportcheck`)
- Upload `index.html` and `README.md`

### 4. Turn on GitHub Pages
- Repo **Settings → Pages**
- Source: **Deploy from a branch → main → / (root)** → Save
- Live in ~1 minute at `https://YOUR_USERNAME.github.io/sportcheck/`

## Features
- Tabbed layout — switch between Formula 1 and World Cup
- Hero stat cards (rounds, drivers, teams, season)
- Team color bars and nationality flags on every driver
- "Up next" race highlighted, past winners shown
- World Cup score cards in a clean VS layout
- Group tables with a green qualification line
- Upcoming fixtures with kickoff times
- Dark theme, works on mobile, zero dependencies

## Notes
- Until you add your football-data.org key, the World Cup tab shows clearly-labelled sample data so you can see the layout.
- World Cup 2026 is competition ID `2000` on football-data.org. Live data flows automatically once the tournament starts (June 2026).
- The free tier allows 10 requests/minute — plenty for this dashboard.
- Everything runs in the browser. Your API key is visible in the page source, which is normal for a free rate-limited key.
