# Python — Netflix Content Analysis

This folder contains the Python notebook for exploratory data analysis on the Netflix Movies and TV Shows dataset. The analysis covers data cleaning, transformation, and visualization to answer 6 business questions about Netflix content trends.

---

## File

| File | Description |
|---|---|
| Netflix_Project.ipynb | Main EDA notebook with cleaning, analysis and visualizations |
| netflix_dataset.csv | Raw original dataset from Kaggle |
| Cleaned_Netflix_data.csv | Cleaned dataset after preprocessing |
| README.md | Project documentation |

---

## Libraries Used

| Library | Purpose |
|---|---|
| Pandas | Data cleaning and transformation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualizations |

---

## Data Cleaning Steps

- Handled null values in director, cast, and country columns
- Parsed date_added column into proper datetime format
- Extracted year_added and month_added as separate columns
- Standardized inconsistent text values across categorical columns
- Removed duplicate rows

---

## Business Questions Answered

| # | Question |
|---|---|
| 1 | What is the distribution of Movies vs TV Shows on Netflix? |
| 2 | Which countries produce the most Netflix content? |
| 3 | How has Netflix content grown over the years? |
| 4 | What are the most common ratings on Netflix? |
| 5 | What are the most popular genres on Netflix? |
| 6 | What is the most common movie duration on Netflix? |

---

## Dataset

[Download the Netflix Dataset from Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

| File | Description |
|---|---|
| netflix_titles.csv | Title, type, director, cast, country, date added, rating, duration, genre |

---

## Author

Arshiyan Mairaj
[LinkedIn](https://linkedin.com/in/arshiyanmairaj/) | [GitHub](https://github.com/Arshiyan7)