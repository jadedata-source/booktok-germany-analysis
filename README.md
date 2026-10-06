# German BookTok Bestseller Analysis 📚

**A data analysis of the official German BookTok Top 20 bestseller charts from April 2023 to July 2026.**

This project explores which characteristics are associated with stronger BookTok chart performance in Germany and what publishers can learn from these patterns.

---

## Research Question

**Which characteristics are associated with stronger BookTok chart performance in Germany, and what can publishers learn from these patterns?**

The analysis focuses on differences in:

- genre
- chart longevity
- publication age
- publisher
- publishing model
- series status

---

## Dataset

The project is based on the official German **#BookTok Top 20 bestseller rankings** published by Media Control.

### Dataset overview

- **292 unique titles**
- **780 complete monthly chart observations**
- **40 months of rankings**
- **April 2023 – July 2026**

The ranking data was enriched with book-level metadata including:

- title
- author
- genre
- publisher
- publication date
- ISBN
- series status
- self-publishing status
- months in chart
- best rank
- average rank

> Note: November 2024 was only partially available and was therefore excluded from core longevity calculations where full monthly coverage was required.

---

## Tools & Technologies

- **Python**
- **pandas**
- **NumPy**
- **SciPy**
- **Matplotlib**
- **Tableau**
- **Excel**

Python was used for data preparation, analysis and statistical testing, while Tableau was used for interactive visual exploration.

---

# Key Findings

## 1. High genre volume does not necessarily mean long-term chart presence

**New Adult / Contemporary Romance** was by far the largest BookTok category with **127 unique titles**, followed by **Fantasy / Romantasy** with 80 titles.

However, smaller categories stayed in the charts much longer on average.

| Genre | Unique Titles | Avg. Months in Chart |
|---|---:|---:|
| New Adult / Contemporary Romance | 127 | 2.3 |
| Fantasy / Romantasy | 80 | 2.0 |
| Dark Romance | 34 | 2.2 |
| Thriller / Mystery | 12 | 4.1 |
| Contemporary / Literary Fiction | 18 | 5.3 |
| Self-Help / Non-Fiction | 20 | 5.8 |

**Takeaway:** The genres producing the most BookTok titles are not necessarily the genres with the strongest chart persistence.

---

## 2. BookTok is not only a launch channel

Books that entered the chart more than six months after publication remained in the BookTok rankings substantially longer on average.

- **New releases (≤6 months old): 2.2 months**
- **Older titles (>6 months old): 5.8 months**

This suggests that BookTok can generate renewed visibility for older titles and create opportunities for publishers to reactivate their backlist.

**Takeaway:** BookTok marketing does not have to focus exclusively on new releases.

---

## 3. Publisher-backed books still dominate BookTok

Despite the direct-to-consumer opportunities created by social media, traditionally published books overwhelmingly dominated the official German BookTok charts.

Among titles with known publishing status:

- **95.7% traditionally published**
- **4.3% self-published**

Self-published books represented only around **2.6% of monthly chart appearances**.

**Takeaway:** Social media may democratize book discovery, but publisher support remains highly relevant for achieving sustained visibility in the official BookTok bestseller ecosystem.

---

## Publisher Landscape

The publishers with the largest number of unique titles appearing in the dataset included:

| Rank | Publisher | Unique Titles |
|---:|---|---:|
| 1 | LYX | 43 |
| 2 | dtv | 22 |
| 3 | Penguin | 20 |
| 4 | Goldmann | 13 |
| 5 | everlove / Piper | 12 |
| 6 | Heyne | 12 |
| 7 | Blanvalet | 10 |
| 8 | Carlsen | 10 |
| 9 | VAJONA | 10 |
| 10 | Knaur TB | 9 |

Publisher presence also differs strongly by genre.

Examples:

- **LYX** has a particularly strong presence in New Adult / Contemporary Romance.
- **VAJONA** is highly concentrated in Dark Romance.
- **dtv** has a strong presence in Fantasy / Romantasy.

---

# Tableau Visualizations

The project includes a Tableau analysis covering four perspectives:

### Genre Volume vs. Chart Persistence
Compares the number of unique titles within each genre with the average number of months those titles remained in the chart.

### Top 10 Publishers
Ranks publishers according to the number of unique titles appearing in the German BookTok Top 20.

### Publisher Presence by Genre
A heatmap showing which publishers are most represented across the main BookTok genre categories.

### Backlist vs. New Releases
Compares the average chart duration of newly released books with titles that were already more than six months old when they first entered the BookTok chart.

### Interactive Tableau Dashboard

**[View the Tableau Public dashboard](PASTE_TABLEAU_PUBLIC_LINK_HERE)**

Screenshots and exported visualizations are also available in the [`visuals/`](visuals/) folder.

---

# Python Analysis

The complete Python analysis can be found in the Jupyter Notebook:

**[View the analysis notebook](notebooks/BookTok_Final_Analysis.ipynb)**

The notebook includes:

- data loading and preparation
- data quality checks
- descriptive analysis
- genre analysis
- publisher analysis
- publication-age / backlist analysis
- self-publishing analysis
- statistical testing
- visualizations

---

# Project Structure

```text
booktok-germany-analysis/
│
├── data/
│   └── booktok_germany_master_2023_2026_enriched_clean.xlsx
│
├── notebooks/
│   └── BookTok_Final_Analysis.ipynb
│
├── visuals/
│   └── Tableau charts and dashboard screenshots
│
├── presentation/
│   └── Final project presentation
│
├── docs/
│   └── Additional methodology and documentation
│
└── README.md
