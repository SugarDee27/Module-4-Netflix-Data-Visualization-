# Module 4 Assignment: Netflix Data Visualization

This package contains Python and R code for preparing, cleaning, exploring, and visualizing a Netflix dataset.

## Contents
- `Netflix_shows_movies.csv` — Original dataset copy (renamed).
- `Netflix_shows_movies_cleaned.csv` — Cleaned dataset after processing.
- `raw_head.csv` — First 20 rows preview of the raw dataset.
- `data_description.csv` — Descriptive statistics of the dataset.
- `genre_counts.csv` — Frequencies of genres (proxy for "most watched").
- `rating_counts.csv` — Distribution of ratings.
- `most_watched_genres.png` — Bar chart of top genres (Python/Matplotlib).
- `ratings_distribution.png` — Ratings distribution bar chart (Python/Matplotlib).
- `analysis.py` — Re-runnable Python script for generating the charts.
- `genre_barplot.R` — R script that generates the Top Genres bar chart.

## Getting Started (Python)
1. Ensure you have Python 3.9+ and install dependencies:
   ```bash
   pip install pandas numpy matplotlib
   ```
2. Run the analysis script:
   ```bash
   python analysis.py
   ```
3. The figures will be saved as PNG files in the same directory.

## Getting Started (R)
1. Install required packages in R:
   ```r
   install.packages(c("readr", "dplyr", "tidyr", "ggplot2"))
   ```
2. Set the working directory to this folder and run the script:
   ```r
   source("genre_barplot.R")
   ```
3. The plot `most_watched_genres_R.png` will be saved in the folder.

## Notes & Assumptions
- If the dataset lacks explicit view counts, the "Most watched genres" visualization uses **frequency of titles per genre** as a proxy.
- Missing categorical fields are filled with `"Unknown"`. Numeric fields are imputed with the median of the column.
- `duration_min` is derived only when `duration` is in minutes (e.g., `"90 min"`). Season-based durations are left as `NA` in `duration_min`.

## Reproducibility
All generated files are placed in the `netflix_assignment/` directory. Re-running `analysis.py` will regenerate the figures.