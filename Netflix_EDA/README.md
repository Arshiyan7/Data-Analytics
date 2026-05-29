# Netflix Content Analysis Project

An end-to-end data analytics project built on the Netflix Movies and TV Shows dataset. The goal of this project is to demonstrate a complete analytics pipeline across two industry-standard tools — Python and SQL — using a single real-world dataset from raw ingestion to business insight generation.

---

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Python (Pandas, Matplotlib, Seaborn) | Data cleaning, EDA and visualization |
| SQL (PostgreSQL) | Business question analysis and querying |

---

## Dataset

The raw dataset is publicly available on Kaggle and was not included in this repository to keep it lightweight.

[Download the Netflix Dataset from Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

| File | Description |
|---|---|
| netflix_titles.csv | Title, type, director, cast, country, date added, rating, duration, genre |

---

## Project Structure

```text
Netflix_EDA/
│
├── python/
│   ├── Netflix_Project.ipynb
│   ├── netflix_dataset.csv
│   ├── Cleaned_Netflix_data.csv
│   └── README.md
│
├── sql/
│   ├── netflix_analysis.sql
│   └── README.md
│
└── README.md
```

---

## Business Questions Answered

### Python EDA

| # | Question |
|---|---|
| 1 | What is the distribution of Movies vs TV Shows on Netflix? |
| 2 | Which countries produce the most Netflix content? |
| 3 | How has Netflix content grown over the years? |
| 4 | What are the most common ratings on Netflix? |
| 5 | What are the most popular genres on Netflix? |
| 6 | What is the most common movie duration on Netflix? |

### SQL Analysis

| # | Question |
|---|---|
| 1 | How many Movies vs TV Shows are on Netflix? |
| 2 | What are the top 10 most common ratings on Netflix? |
| 3 | How many titles were added to Netflix each year? |
| 4 | Show all Movies released in 2020 |
| 5 | Show all content from United States sorted by release year |
| 6 | Which top 5 countries produce the most Netflix content? |
| 7 | What is the most common duration for Movies? |
| 8 | Which directors have more than 3 titles on Netflix? |
| 9 | Show Movies and TV Shows added each year |
| 10 | Which genre category appears the most on Netflix? |

---

## Author

Arshiyan Mairaj
[LinkedIn](https://linkedin.com/in/arshiyanmairaj/) | [GitHub](https://github.com/Arshiyan7)