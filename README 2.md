# Descriptive Analytics Report: Steam Game Sales, Ratings & Market Trends

A descriptive analytics study of the Steam PC gaming marketplace, covering **89,618 games**, **49,840 publishers** and **33 genres**. The analysis was carried out in a Jupyter Notebook (Python) and documented in a full report with charts, observations and interpretations.

---

## Objective

Build a descriptive analytics layer over Steam game data to answer five recurring business questions:

1. Which games are the most popular?
2. How do game sales (estimated owners) vary across genres?
3. Which games receive the highest user ratings?
4. Which publishers contributed to the largest number of successful games?
5. Which genres dominate the Steam marketplace?

---

## Dataset

| Attribute | Value |
|-----------|-------|
| Source | [Kaggle – Steam Games Dataset (artermiloff)](https://www.kaggle.com/datasets/artermiloff/steam-games-dataset) |
| File used | `Games_March_2025.csv` |
| Rows | 89,618 |
| Columns | 47 |
| Memory usage | ~661.3 MB |

**Key features used:** Positive Reviews, Negative Reviews, Estimated Owners (midpoint), Publishers, Genres, Price, Average Playtime, Release Date.

---

## Report Contents

| Section | What it covers |
|---------|----------------|
| **Game Popularity** | Top 10 games by estimated owners, positive reviews and average playtime |
| **Genre Analysis** | Games per genre, average price by genre, average rating by genre |
| **Publisher Analysis** | Publishers with most games, highest average rating, highest average price |
| **Price Analysis** | Price distribution, free vs paid split, most expensive games |
| **Rating Analysis** | Positive vs negative reviews, highest-rated games, rating distribution |
| **Release Trends** | Games released per year and per month |
| **Summary & KPIs** | Overall KPI table, key findings, predictive-analytics outlook |

---

## Key Findings

| KPI | Value |
|-----|-------|
| Total games | 89,618 |
| Total publishers | 49,840 |
| Genres | 33 |
| Estimated owners (total) | ~9.06 billion |
| Positive reviews | 113.8 million (85.8%) |
| Negative reviews | 18.8 million (14.2%) |
| Average user rating | 77.08% |
| Average game price | $7.31 |
| Paid games | 75,458 (84.2%) |
| Free-to-play games | 14,160 (15.8%) |

**Highlights**

- **Most owned:** Dota 2 (~350M estimated owners), followed by Counter-Strike 2 (~150M).
- **Most positive reviews:** Counter-Strike 2 (7,480,813).
- **Longest playtime:** Dota 2 averages 717.18 hours per player.
- **Dominant genres:** Indie, Casual, Action and Adventure have the most titles.
- **Pricing:** Most paid games are priced under $10; the priciest titles are mostly professional software and bundles.
- **Ratings:** Positive reception is the baseline, with the distribution peaking between 70% and 90%.
- **Release growth:** Yearly releases grew sharply from around 2014–2015 after Steam opened up self-publishing.
- **Seasonality:** Release volume peaks in October and November.
- **Publishers:** The market is heavily skewed; a few large publishers (e.g. Valve, Rockstar Games) capture most engagement, while tens of thousands of small studios share the long tail.

---

## Tools & Technologies

- **Python** (Jupyter Notebook)
- **Pandas** for data cleaning and aggregation
- **Matplotlib** for bar charts, histograms, pie charts and line charts

---

## Visualisations Included

- Horizontal bar charts: top games, genre price/rating, publishers, expensive games
- Vertical bar charts: games per genre, releases per month
- Histograms: price distribution, rating distribution
- Pie charts: free vs paid, positive vs negative reviews
- Line chart: games released per year

---

## Repository Structure

```
.
├── README.md
├── DA_STEAM_FINAL_Report.pdf      # Full analytics report
├── steam_analysis.ipynb           # Jupyter notebook (add your file)
└── data/
    └── Games_March_2025.csv       # Download from Kaggle (not included)
```

> The dataset is large, so download it from the Kaggle link above instead of uploading it to GitHub.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   ```
2. Install the dependencies:
   ```bash
   pip install pandas matplotlib jupyter
   ```
3. Download `Games_March_2025.csv` from Kaggle and place it in the `data/` folder.
4. Launch the notebook:
   ```bash
   jupyter notebook
   ```

---

## Future Scope

- **Sales forecasting:** time-series models using price, genre and release month to predict seasonal sales
- **User behaviour analysis:** link playtime with update, DLC and battle-pass schedules
- **Predictive analytics:** move from "what happened" to "what will happen"

---

## Author

**Saurabh Singh**
University Roll No: 1250258403
Bachelor of Computer Applications (BCA), Data Science and Artificial Intelligence
School of Computer Applications, Babu Banarasi Das University (BBDU), Lucknow
Subject: Descriptive Analytics | Session: 2026–2027
Submitted to: Ms. Monica

---

## Acknowledgements

- Dataset: [Steam Games Dataset on Kaggle](https://www.kaggle.com/datasets/artermiloff/steam-games-dataset)
- Valve Corporation for the Steam platform
