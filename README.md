# CMFA PressCon Tracker 📊

> **Chinese Diplomatic Discourse Dataset** — Browse, filter and explore 35,346 Q&A dyads from MFA press conferences (2002–2025).

**Live site:** `https://YOUR-USERNAME.github.io/cmfa-tracker/`

---

## Pages

| File | URL | Description |
|---|---|---|
| `index.html` | `/` | **Homepage — full data browser** (35,346 entries) |
| `analytics.html` | `/analytics.html` | Charts, sentiment trends, geography |
| `data.csv` | `/data.csv` | Raw dataset download (43 MB) |

---

## Data Browser Features

The homepage (`index.html`) is a fully interactive dataset explorer:

**Filtering (left sidebar)**
- Full-text search across questions and/or answers (with keyword highlighting in results)
- Year range slider (2002–2025)
- Spokesperson checkboxes (all 16, with entry counts)
- Media outlet filter with search (from March 2020)
- Quick topic chips — US, Taiwan, Japan, DPRK, Russia, Ukraine, India, South China Sea, Hong Kong, Xinjiang, Iran, Afghanistan
- Answer sentiment range slider (0–5)
- Question sentiment range slider (0–5)

**Toolbar**
- Live search with debounce (250ms)
- Search scope: Questions + Answers / Questions only / Answers only
- Sort by: ID, Date, Q Sentiment, A Sentiment
- Table view / Card view toggle
- Export filtered results as CSV

**Results**
- Active filter chips (click × to remove individual filters)
- Live stats bar: result count, avg Q sentiment, avg A sentiment, date range
- Colour-coded sentiment badges (red → amber → green scale)
- Paginate: 25 / 50 / 100 / 200 per page
- Jump to any page number
- Click any row → full detail modal

**Modal (entry detail)**
- Full question and answer text
- Named entities with colour-coded tags (Locations / Persons / Organisations)
- Large sentiment scores with human-readable labels
- Prev/Next navigation through filtered results
- Keyboard: ← → to navigate, ESC to close

**Keyboard shortcuts**
- `/` — focus search box
- `←` / `→` — go to previous/next page (or previous/next modal entry when open)
- `Escape` — close modal

---

## Deploy to GitHub Pages

### Step 1 — Create the repo

1. [github.com/new](https://github.com/new) → name it `cmfa-tracker` → Public → **Create** (empty, no README)

### Step 2 — Push files via Git CLI

```bash
cd /path/to/your/cmfa-tracker/folder

git init
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
git remote add origin https://github.com/YOUR-USERNAME/cmfa-tracker.git
git add .
git commit -m "Initial commit: CMFA tracker"
git branch -M main
git push -u origin main
```

When prompted for password, use a Personal Access Token (GitHub → Settings → Developer settings → Tokens (classic) → Generate with `repo` scope).

### Step 3 — Enable GitHub Pages

GitHub repo → **Settings → Pages → Source → Deploy from branch → main / root → Save**

Site goes live in ~60 seconds at: `https://YOUR-USERNAME.github.io/cmfa-tracker/`

---

## CSV vs XLSX

Use **CSV**. GitHub can preview it, it loads in-browser via PapaParse, works with Git diffs, and is human-readable. Keep your `.xlsx` as a local editing master; upload `data.csv` to GitHub.

---

## Dataset Citation

> Mochtak, M. & Turcsanyi, R.Q. (2021). "Studying Chinese Foreign Policy Narratives: Introducing the Ministry of Foreign Affairs Press Conferences Corpus." *Journal of Chinese Political Science*, 26(4), 743–761.

**Sentiment:** Mochtak, M., Rupnik, P. & Ljubešić, N. (2023). ParlaSent. *arXiv* 2309.09783.  
**Model:** [classla/xlm-r-parlasent](https://huggingface.co/classla/xlm-r-parlasent)

---

## Stack

Zero build step · Pure HTML/CSS/JS · [PapaParse](https://www.papaparse.com/) · [Chart.js](https://www.chartjs.org/)
