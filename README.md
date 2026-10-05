# Automating Enterprise Content Audits with Unsupervised Machine Learning

A machine learning project completed during my **Machine Learning Internship at FlyRank AI**.

The project uses **K-Means clustering** to group website pages based on organic search performance and content characteristics, helping identify pages that are performing well, have optimization potential, or may require further investigation.

## Tech Stack

* Python
* Pandas
* NumPy
* DuckDB
* SQL
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook
* Hugging Face Datasets

## Workflow

* Retrieved data from the FlyRank internship warehouse using DuckDB
* Aggregated February 2026 daily content performance data
* Joined performance data with content metadata
* Created features such as impressions, clicks, CTR, average position, scrolls, and word count
* Applied log transformations to skewed features
* Standardized features using `StandardScaler`
* Applied K-Means clustering
* Identified four content performance groups
* Validated the frozen February model on unseen March 2026 data

## Content Archetypes

* ⭐ **Superstars**: Strong search performance and CTR
* 💎 **Hidden Gems**: High impressions with comparatively low CTR
* 📈 **Underdogs**: Potentially valuable content with weaker performance
* 🧟 **Zombies**: Low-performing pages requiring further investigation

## Time-Aware Validation

The model was trained using **February 2026** data and evaluated on **March 2026** data without retraining.

The February scaler and K-Means cluster centers were kept frozen during validation to avoid future data leakage.

The resulting cluster profiles remained highly consistent across both months.

## Project Context

This project was completed as part of my **Machine Learning Internship at FlyRank AI**, focusing on applying unsupervised machine learning to enterprise content performance analysis.

> The original internship dataset is not included in this repository due to data access and confidentiality considerations.
