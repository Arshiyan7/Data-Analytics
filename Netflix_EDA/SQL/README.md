# SQL — Netflix Content Analysis

This folder contains the SQL analysis built on top of the cleaned Netflix dataset loaded into PostgreSQL. The analysis answers 10 business questions covering content distribution, filtering, aggregation, and intermediate-level queries.

---

## File

| File | Description |
|---|---|
| netflix_analysis.sql | Full SQL script with 10 business questions and inline insights |
| README.md | Project documentation |

---

## Tools Used

| Tool | Purpose |
|---|---|
| PostgreSQL | Database and query execution |
| pgAdmin | SQL client and database management |

---

## Dataset

| Table | Rows | Description |
|---|---|---|
| netflix | 5,619 | Title, type, director, country, rating, duration, genre, year added |

---

## Business Questions Answered

| # | Question | Concept |
|---|---|---|
| 1 | How many Movies vs TV Shows are on Netflix? | GROUP BY, COUNT |
| 2 | What are the top 10 most common ratings on Netflix? | GROUP BY, ORDER BY, LIMIT |
| 3 | How many titles were added to Netflix each year? | GROUP BY, COUNT |
| 4 | Show all Movies released in 2020 | WHERE, filtering |
| 5 | Show all content from United States sorted by release year | WHERE, ORDER BY |
| 6 | Which top 5 countries produce the most Netflix content? | GROUP BY, LIMIT |
| 7 | What is the most common duration for Movies? | WHERE, GROUP BY |
| 8 | Which directors have more than 3 titles on Netflix? | HAVING, GROUP BY |
| 9 | Show Movies and TV Shows added each year | GROUP BY multiple columns |
| 10 | Which genre category appears the most on Netflix? | GROUP BY, ORDER BY |

---

## Key Insights

**Content Type** — Movies dominate Netflix content significantly over TV Shows across all years.

**Target Audience** — TV-MA is the most common rating followed by TV-14, indicating Netflix primarily targets mature audiences.

**Peak Year** — 2019 was Netflix's biggest content addition year with 1,334 titles added, followed by 2020 with 1,290.

**Top Country** — The United States leads content production with 1,224 titles, followed by India with 937 and the United Kingdom with 311.

**Top Director** — Cathy Garcia-Molina leads with 13 titles among directors with more than 3 Netflix titles.

**Movie Duration** — 90 minutes is the most common runtime for Netflix movies.

---

## Author

Arshiyan Mairaj
[LinkedIn](https://linkedin.com/in/arshiyanmairaj/) | [GitHub](https://github.com/Arshiyan7)