# Automating Enterprise Content Audits with Unsupervised Machine Learning

## Overview

A machine learning project completed during my **Machine Learning Internship at FlyRank AI**.

This project uses **K-Means clustering** to analyze enterprise website content based on organic search performance and content characteristics. The goal is to identify meaningful content groups and help prioritize pages for optimization or further investigation.

## Tech Stack

| Category         | Technologies          |
| ---------------- | --------------------- |
| Language         | Python                |
| Data Processing  | Pandas, NumPy         |
| Data Querying    | DuckDB, SQL           |
| Machine Learning | Scikit-learn, K-Means |
| Visualization    | Matplotlib, Seaborn   |
| Environment      | Jupyter Notebook      |
| Data Source      | Hugging Face Datasets |

## Methodology

The project follows the following workflow:

1. Retrieved data from the FlyRank internship warehouse using **DuckDB**.
2. Aggregated daily content performance data for **February 2026**.
3. Joined performance data with content metadata.
4. Engineered features including:

   * Impressions
   * Clicks
   * CTR
   * Average position
   * Scrolls
   * Word count
5. Applied log transformations to highly skewed features.
6. Standardized numerical features using **StandardScaler**.
7. Applied **K-Means clustering** to identify content performance patterns.
8. Validated the frozen February model on unseen **March 2026** data.

## Content Archetypes

The clustering process identified four main content groups:

| Archetype          | Description                                          |
| ------------------ | ---------------------------------------------------- |
| ⭐ **Superstars**   | Strong search performance and CTR                    |
| 💎 **Hidden Gems** | High impressions with comparatively low CTR          |
| 📈 **Underdogs**   | Potentially valuable content with weaker performance |
| 🧟 **Zombies**     | Low-performing pages requiring further investigation |

## Time-Aware Validation

To avoid future data leakage, the model was trained using **February 2026** data and evaluated on **March 2026** data without retraining.

The February **StandardScaler** and **K-Means cluster centers** were kept frozen during validation.

The resulting cluster profiles remained highly consistent across both monthly periods.

## Project Context

This project was completed as part of my **Machine Learning Internship at FlyRank AI**, with a focus on applying unsupervised machine learning to enterprise content performance analysis.

> **Note:** The original internship dataset is not included in this repository due to data access and confidentiality considerations.
