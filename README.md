# capstone_project_itds_2373
# Data Mining Capstone Project
## Anime Acquisition Strategy for a Streaming Platform

**Course:** ITDS 2373 — Data Mining

**Project Status:** Data Engineering & Acquisition phase completed; remaining team analyses pending.

## Business Scenario

A new streaming platform has hired a Data Mining Consulting Team to identify 10 anime titles for licensing from the MyAnimeList database.

The Chief Content Officer (CCO) has allocated a significant acquisition budget. However, the company is looking beyond popular anime titles. It wants investments that can attract large audiences, generate positive viewer engagement, and potentially develop into long-term franchises through sequels, spin-offs, merchandise, movies, and other intellectual property opportunities.

### Business Question

> If you were responsible for investing millions of dollars in anime licensing and future franchise ownership opportunities, which 10 anime would you recommend and why?

The team's recommendations must be supported by data cleaning, exploratory analysis, clustering, predictive modeling, review analysis, and business interpretation.

## Dataset

**Source:** [Anime Dataset with Reviews — MyAnimeList (Kaggle)](https://www.kaggle.com/datasets/marlesson/myanimelist-dataset-animes-profiles-reviews)

The project uses three datasets:

- **Anime:** Anime titles, genres, ratings, popularity, membership, and release information.
- **Profiles:** User profiles and favorite anime selections.
- **Reviews:** Anime reviews and associated ratings.

## Team Roles and Responsibilities

The capstone is divided into four analytical roles.

### 1. Data Engineering & Acquisition Analyst

**Key Question:** What data should the team trust and use for decision-making?

Responsibilities include exploring the datasets, documenting their structure, addressing data-quality issues, engineering relevant features, and integrating the data for further analysis.

**Deliverables:** Data dictionary, cleaning report, and final merged dataset.

### 2. Market Intelligence & Visualization Analyst

**Key Question:** What characteristics appear to make anime successful?

This role focuses on exploratory analysis of ratings, popularity, genres, episode counts, review sentiment, and audience engagement.

**Deliverables:** Visual dashboard and business insights document.

### 3. Consumer Segmentation & Clustering Analyst

**Key Question:** Which anime belong in the same investment category?

This role applies clustering techniques to identify groups such as mainstream hits, hidden gems, highly rated niche titles, and potential franchise opportunities.

**Deliverables:** Cluster visualizations, interpretations, and strategic recommendations.

### 4. Predictive Analytics & Acquisition Strategist

**Key Question:** Which anime have the highest probability of becoming long-term successes?

This role uses predictive models to evaluate anime performance, identify important success factors, and develop a strategic ranking system.

**Deliverables:** Predictive models, feature importance analysis, and strategic rankings.

---

## My Contribution: Data Engineering & Acquisition

This repository currently documents my work as the Data Engineering & Acquisition Analyst.

### Dataset Exploration and Preparation

The work completed includes:

- Examining the anime, profiles, and reviews datasets.
- Identifying relationships between anime records, reviews, and user favorites.
- Identifying and removing duplicate records and identifiers.
- Assessing missing values and data completeness.
- Standardizing data types and correcting inconsistencies.
- Parsing genre information and user favorite lists.
- Aggregating review scores and favorite counts.
- Merging the datasets and validating the final output.

### Feature Engineering

Additional features were developed to support subsequent analysis:

| Feature | Purpose |
|---|---|
| `genre_count` | Number of genres associated with each anime |
| `popularity_index` | Normalized measure of relative popularity |
| `franchise_indicator` | Identifies potentially related anime titles using a heuristic |
| `review_count` | Number of reviews per anime |
| `avg_review_score` | Average review score |
| `favorites_count` | Number of distinct profiles favoriting an anime |
| `release_year` | Year the anime was released |
| `anime_age` | Age of the anime based on its release year |
| `release_decade` | Decade in which the anime was released |

### Completed Deliverables

| Deliverable | Description |
|---|---|
| [Jupyter Notebook](notebooks/Capstone_Project_ITDS_2373.ipynb) | Python workflow for dataset exploration, cleaning, feature engineering, and integration |
| [Data Dictionary](reports/anime_data_dictionary.docx) | Definitions, data types, and documentation of dataset attributes |
| [Cleaning Report](reports/anime_cleaning_report.docx) | Data-quality assessment and documentation of cleaning decisions |
| [Final Merged Dataset](data/processed/final_anime_dataset.csv) | Cleaned, integrated dataset prepared for further analysis |

## Data Access

Due to the large size of some CSV files and GitHub's file preview limitations, the cleaned datasets are also available through Google Drive.

**[Access Cleaned CSV Files on Google Drive](https://drive.google.com/drive/folders/1ChEe84csJKMN5PtDWmRVp3y8IPAEOm1y?usp=drive_link)**

These datasets were prepared during the Data Engineering & Acquisition phase and will support the subsequent exploratory analysis, clustering, and predictive modeling stages of the capstone project.

### Tools and Technologies

Python, pandas, NumPy, Jupyter Notebook, Git, and GitHub.

### Outcome

This phase produced a consolidated dataset combining anime attributes with aggregated review and user-favorite information.

The dataset, data dictionary, and cleaning report establish a documented foundation for the remaining data mining activities.

---

## Final Team Task: Anime Acquisition Strategy

After completing all four analytical phases, the team will present its findings to the streaming platform's executive leadership.

### Top 10 Anime to Acquire

Each recommendation will include:

- Anime title
- Rating and popularity
- Review sentiment
- Cluster membership
- Predictive model results
- Business justification and franchise potential

### Final Presentation

The presentation will address:

1. What characteristics define successful anime?
2. What patterns emerged from the data?
3. What clusters were identified?
4. What factors best predicted success?
5. Which 10 anime should be acquired?
6. Which 3 anime should receive priority investment for future franchise ownership?

### Executive Deliverable

The completed project will include a one-page **Investment Recommendation Memo** outlining the 10 recommended anime, three priority franchise investments, expected benefits, potential risks, and supporting data-driven evidence.

**Success Criterion:** Recommendations must be based on data mining results and business reasoning rather than personal preferences or fandom.

---


| Predictive Analytics & Acquisition Strategy | Pending |
| Final Team Presentation & Investment Memo | Pending |

*This repository currently focuses on the Data Engineering & Acquisition phase. Additional findings and deliverables will be incorporated as the team progresses through the capstone.*
