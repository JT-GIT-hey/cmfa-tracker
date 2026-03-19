# CMFA PressCon Tracker 📊

**Live site:** `https://JT-GIT-hey.github.io/cmfa-tracker/`

| File | Description |
|---|---|
| `index.html` | Homepage — full data browser with theme filters |
| `analytics.html` | Research analytics dashboard |
| `data.csv` | Full dataset (43 MB, 35,346 entries) |

## New in this version

### Data Browser (index.html)
- **13 topic/theme filters** — Crisis, Conflict, Health/Pandemic, Trade, Human Rights, Nuclear, Terrorism, Climate, Taiwan, South China Sea, Russia-Ukraine, US-China, DPRK
- Any/All matching mode for themes
- Answer length filter (short/medium/long/very long)
- Named entity filters (has location / person / org mentions, has media attribution)
- Theme badges shown on every row and card
- Modal shows theme tags on each entry

### Analytics (analytics.html)
- **6 research insight boxes** with pre-computed findings
- Sentiment volatility chart (year-on-year change)
- Topic frequency over time (13 themes, filterable by group)
- Theme breakdown table with sparkbars and trend arrows
- Geographic focus with interactive country toggle
- Spokesperson sentiment + gap comparison (side by side)
- **Media outlet bias analysis** — quantified West vs Chinese state media question sentiment gap
- Q&A length evolution over 23 years
- Monthly seasonality chart

## Deploy update to GitHub

```bash
cd /path/to/cmfa-tracker

git add index.html analytics.html README.md
git commit -m "Add theme filters and expanded analytics"
git push
```

Done — GitHub Pages auto-deploys in ~60 seconds.
