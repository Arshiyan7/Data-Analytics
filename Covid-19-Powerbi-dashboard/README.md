# COVID-19 Global Impact Analysis Project

An end-to-end data analytics project built on the COVID-19 2020 dataset. The goal of this project is to demonstrate a complete analytics pipeline across two industry-standard tools — Python and Power BI — covering data cleaning and preprocessing in Python followed by interactive dashboard development in Power BI.

---

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Python (Pandas) | Data cleaning and preprocessing |
| Power BI Desktop | Interactive dashboard and visualization |
| Power Query | Additional data transformation |
| DAX | Custom measures and KPI calculations |

---

## Dataset

The raw dataset is publicly available on Kaggle and was not included in this repository to keep it lightweight.

[Download the COVID-19 Dataset from Kaggle](https://www.kaggle.com/datasets/imdevskp/corona-virus-report)

Two CSV files were used:

| File | Description |
|---|---|
| full_grouped.csv | Time-series data — confirmed cases, deaths, recoveries, daily changes by country |
| worldometer_data.csv | Snapshot data — total cases, deaths, recoveries, population, testing data per country |

---

## Project Structure

```bash
Covid-19-Powerbi-dashboard/
│
├── Data/
│   ├── full_grouped.csv
│   ├── grouped_data_cleaned.csv
│   ├── worldometer_data.csv
│   ├── worldometer_data_cleaned.csv
│
├── python/
│   ├── Covid-19.ipynb
│   └── README.md
│
├── powerbi/
│   ├── covid_dashboard.pbix
│   ├── covid_dashboard.png
│   └── README.md
│
└── README.md
```

---

## Business Questions Answered

### Power BI Dashboard

| # | Question |
|---|---|
| 1 | What is the total number of confirmed cases worldwide? |
| 2 | What is the total number of deaths worldwide? |
| 3 | What is the total number of recoveries worldwide? |
| 4 | What is the global death rate? |
| 5 | How did confirmed cases grow over time? |
| 6 | How did deaths trend over time compared to recoveries? |
| 7 | Which 10 countries have the highest confirmed cases? |
| 8 | Which 10 countries have the highest death counts? |
| 9 | How are cases distributed across the world? |
| 10 | What is the recovery rate vs death rate globally? |

---

## Author

Arshiyan Mairaj  
[LinkedIn](https://linkedin.com/in/arshiyanmairaj/) | [GitHub](https://github.com/Arshiyan7)