# 📊 YouTube Trending Videos Data Analysis

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Math-lightblue.svg)](https://numpy.org/)

This project contains an in-depth Exploratory Data Analysis (EDA) and Data Wrangling of YouTube trending videos across various countries (USA, Great Britain, Germany, Canada, France, Russia, etc.). The goal is to extract meaningful insights using Python Data Science libraries, transforming raw data into a structured and analysis-ready dataset.

## 📋 Project Description

The project is structured as a Jupyter Notebook that processes and analyzes the famous "Trending YouTube Video Statistics" dataset (often found on Kaggle). The workflow tackles several common data processing challenges, such as concatenating scattered datasets, string manipulation, time-series operations, and complex joins between different file formats (CSV and JSON).

## 🚀 Features and Completed Tasks

The analysis is divided into 15 main tasks:

1. **Data Integration**: Concatenation of multiple CSV files (one per country) into a single global DataFrame, dynamically adding a `country` column.
2. **Data Cleaning**: Identification and extraction of videos with no tags (labeled as `[none]`).
3. **Channel Analysis**: Calculation of the total number of views aggregated for each channel.
4. **Invalid Data Filtering**: Isolation and removal of non-analyzable videos (disabled comments, disabled ratings, or removed videos) into a separate DataFrame (`excluded`).
5. **Feature Engineering (Metrics)**: Creation of a new feature called `like_ratio`, calculated as the ratio between *likes* and *dislikes*.
6. **Time-Series Clustering**: Grouping publication times (`publish_time`) into discrete 10-minute intervals (e.g., from 02:20 to 02:30).
7. **Temporal Statistics**: Calculation of the total number of videos, and average likes and dislikes for each 10-minute interval.
8. **Tag Explosion and Cleaning**: Advanced string parsing to separate multiple tags, remove special characters, and explode the lists to get one row per single tag.
9. **Trend Analysis**: Identification of the most frequently used tags within the entire dataset.
10. **Tag/Country Cross-Analysis**: Calculation of the average `like_ratio` for each unique (tag, country) pair.
11. **Top Videos Extraction (Daily)**: Identification of the video with the highest number of views for each (trending date, country) combination.
12. **Date Manipulation**: Splitting the `trending_date` into three separate columns: `year`, `month`, and `day`.
13. **Top Videos Extraction (Monthly)**: Identification of the most viewed video for each month and country.
14. **JSON Integration**: Reading and normalizing (parsing) `.json` files containing YouTube category metadata for each country.
15. **Category Merge and Validation**: Join (Left Merge) between the main video dataset and the category DataFrames to identify how many videos have a category defined as non-assignable (`assignable = False`).

## 🛠️ Technologies Used

- **Language**: Python
- **Main Libraries**:
  - `pandas` (Data manipulation, Merging, Groupby, Datetime operations)
  - `numpy` (Numerical computing and array support)
  - `re` (Regular expressions for string cleaning)

## 📂 Required Dataset Structure

To run the code, ensure you have the following file structure inside your specified directory (e.g., `/trendingYT/`):
- CSV files for videos: `CAvideos.csv`, `DEvideos.csv`, `FRvideos.csv`, `GBvideos.csv`, `INvideos.csv`, `JPvideos.csv`, `KRvideos.csv`, `MXvideos.csv`, `RUvideos.csv`, `USvideos.csv`.
- JSON files for categories: `CA_category_id.json`, `DE_category_id.json`, etc.

## ⚙️ Installation and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/youtube-trending-analysis.git
   ```
2. Install the required dependencies:
   ```bash
   pip install pandas numpy
   ```
3. Modify the file reading paths inside the notebook (e.g., the `path` variables) to point to the local directory where you saved the CSV and JSON files.
4. Run the Jupyter Notebook to view the step-by-step output.

## 🤝 Contributing
Contributions are always welcome! Feel free to open an **Issue** to report bugs or propose new features, or submit a **Pull Request** directly.

---
*Project realized as a Data Science & Data Cleaning case study.*
