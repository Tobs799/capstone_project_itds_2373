# Anime Acquisition Strategy | Data Engineering

## Project Overview

This project was developed as part of the Data Mining Methods (ITDS 2373) capstone at Houston Community College. The overall objective is to help a streaming platform identify 10 anime titles with strong licensing potential based on audience engagement, viewer sentiment, popularity and franchise potential.

My individual contribution focuses on transforming raw, inconsistent data into a reliable, analysis-ready dataset that supports the team's analytical models and acquisition decisions.

## My Role

**Tobechukwu Ibukun — Data Engineering & Acquisition Analyst**

My primary responsibility was to answer the question:

> What data should the team trust and use for decision-making?

My work included data cleaning, text preprocessing, feature engineering, dataset integration, data quality validation and technical documentation.

## Tools and Technologies

Python, Pandas, NumPy, Scikit-learn, NLTK, Regular Expressions (Regex), Jupyter Notebook and python-docx.

## Data Source

The project uses the [MyAnimeList Dataset — Animes, Profiles and Reviews](https://www.kaggle.com/datasets/marlesson/myanimelist-dataset-animes-profiles-reviews) from Kaggle.

| Dataset | Original Records | Description |
|---|---:|---|
| animes.csv | 19,311 | Anime titles, genres, ratings and popularity |
| profiles.csv | 81,727 | User profiles and favorite anime |
| reviews.csv | 192,112 | User reviews and rating components |

## Dataset Access

Due to GitHub's file size limitations, the raw and processed datasets can be accessed through Google Drive.

- [Original dataset — Kaggle](https://www.kaggle.com/datasets/marlesson/myanimelist-dataset-animes-profiles-reviews)
- [Download datasets — Google Drive](https://drive.google.com/drive/folders/1SeWjj1deW8uadpfGufheQvh1ixnctNiM?usp=sharing)
- [Final integrated dataset](final_anime_dataset.csv)

## Data Engineering Workflow

### 1. Data Cleaning

- Removed exact duplicates and repeated identifiers.
- Assessed missing values and inconsistent formats.
- Converted columns to appropriate data types and handled invalid ratings.
- Parsed structured information stored as text.
- Preserved missing ratings where imputation could introduce bias.

### 2. Text Preprocessing

Prepared reviews for downstream sentiment analysis by removing HTML tags, URLs, unnecessary headers, punctuation, numbers and stopwords. Negation words such as *no*, *not*, *nor* and *never* were preserved to maintain sentiment context.

### 3. Feature Engineering

| Feature Group | Business Purpose |
|---|---|
| Popularity Index | Standardizes popularity for comparison |
| Genre Indicators | Supports analysis across 43 genres |
| Franchise Indicator | Identifies potential franchise-related titles |
| Favorites Count | Measures audience interest |
| Review Metrics | Captures review volume and average ratings |
| Review Component Ratings | Evaluates specific aspects of viewer satisfaction |
| Release Features | Supports historical and release-period analysis |
| Content Suitability | Supports responsible licensing decisions |

### 4. Content Suitability Classification

Developed three genre-based features: `adult_content_flag`, `suggestive_content_flag` and `content_category`. These distinguish adult content, suggestive content, titles with no adult genre identified and unknown content categories.

All titles were retained to allow the acquisition team to apply appropriate filters. These indicators are based on genre labels and do not represent official age ratings.

### 5. Dataset Integration

Integrated the cleaned anime dataset with aggregated review metrics and user favorites using left joins and one-to-one merge validation. This preserved one record per unique anime ID, including titles without reviews.

### 6. Data Quality Validation

Performed checks for completeness, uniqueness, validity and feature consistency.

## Results

### Data Cleaning Summary

| Dataset | Before Cleaning | After Cleaning | Records Removed |
|---|---:|---:|---:|
| Anime | 19,311 | 16,216 | 3,095 |
| Profiles | 81,727 | 47,885 | 33,842 |
| Reviews | 192,112 | 130,519 | 61,593 |
| **Total** | **293,150** | **194,620** | **98,530** |

Approximately 33.6% of the original records were removed during duplicate cleaning.

### Final Dataset Quality

| Metric | Result |
|---|---:|
| Unique Anime Records | 16,216 |
| Total Columns | 79 |
| Overall Data Completeness | 95.14% |
| Duplicate Anime IDs | 0 |
| Missing Anime IDs | 0 |
| Detected Invalid Values | 0 |
| Detected Consistency Issues | 0 |
| Cleaned Reviews | 130,519 |
| Anime Titles with Reviews | 8,113 |
| Matched User Favorites | 216,297 |

## Project Deliverables

| Deliverable | Description |
|---|---|
| [Data Engineering Notebook](Capstone_project_itds_2373_final_submission.ipynb) | Complete preprocessing, feature engineering and validation workflow |
| [Final Anime Dataset](final_anime_dataset.csv) | Analysis-ready dataset containing 79 columns |
| [Data Dictionary](Anime_Data_Dictionary.docx) | Column definitions, data types and missing-value information |
| [Data Engineering Report](Anime_Data_Engineering_Report.docx) | Cleaning methodology, engineering decisions and data reliability |
| [Documentation Generator Notebook](Data_Dictionary_and_Data_Engineering_Report.ipynb) | Reproducible Python workflow for generating Word documentation |

## Repository Structure

```text
anime-acquisition-data-engineering/
├── README.md
├── .gitignore
├── requirements.txt
├── Capstone_project_itds_2373_final_submission.ipynb
├── Data_Dictionary_and_Data_Engineering_Report.ipynb
├── Anime_Data_Dictionary.docx
├── Anime_Data_Engineering_Report.docx
└── final_anime_dataset.csv
```

## How to Run the Project

1. Clone or download this repository.
2. Download the original datasets from [Kaggle](https://www.kaggle.com/datasets/marlesson/myanimelist-dataset-animes-profiles-reviews) or [Google Drive](https://drive.google.com/drive/folders/1SeWjj1deW8uadpfGufheQvh1ixnctNiM?usp=sharing).
3. Place `animes.csv`, `profiles.csv` and `reviews.csv` in the project directory.
4. Install the required Python libraries:

   ```bash
   pip install -r requirements.txt
   ```

5. Open `Capstone_project_itds_2373_final_submission.ipynb` in Jupyter Notebook.
6. Confirm the input and output paths match your local folder structure.
7. Restart the kernel and run all cells.
8. Open `Data_Dictionary_and_Data_Engineering_Report.ipynb`, confirm the dataset and documentation paths, and run all cells to regenerate the Word documents.

The processed datasets are available through Google Drive for users who wish to proceed directly to analysis.

## Data Limitations

- The dataset represents historical MyAnimeList activity and may not reflect current audience preferences.
- Review coverage varies across anime titles.
- Favorites counts reflect engagement within the available profile dataset.
- Franchise indicators are based on title patterns rather than verified franchise relationships.
- Content suitability classifications depend on available genre labels.
- Missing ratings were retained to avoid introducing artificial audience opinions.

## Business Impact

The final dataset provides a foundation for audience demand assessment, genre preference analysis, viewer sentiment analysis, franchise potential assessment, content suitability screening and data-driven licensing recommendations.

This project demonstrates my ability to transform multiple raw datasets into a structured, validated and documented analytical resource that supports business decision-making.
