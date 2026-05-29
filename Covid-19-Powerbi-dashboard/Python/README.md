# Python — COVID-19 Data Cleaning and Preprocessing

This folder contains the Python notebook for cleaning and preprocessing the COVID-19 dataset before loading into Power BI. The notebook handles two separate datasets — grouped time-series data and worldometer snapshot data — preparing both for data modeling and dashboard visualization.

---

## File

| File | Description |
|---|---|
| Covid-19.ipynb | Main cleaning notebook covering both datasets |
| full_grouped.csv | Raw time-series dataset from Kaggle |
| worldometer_data.csv | Raw worldometer snapshot dataset from Kaggle |
| grouped_data_cleaned.csv | Cleaned and exported grouped dataset |
| worldometer_data_cleaned.csv | Cleaned and exported worldometer dataset |
| README.md | Project documentation |

---

## Libraries Used

| Library | Purpose |
|---|---|
| Pandas | Data cleaning, transformation and export |

---

## Datasets

Two CSV files were used from the Kaggle dataset:

| File | Description |
|---|---|
| full_grouped.csv | Time-series data — confirmed cases, deaths, recoveries, daily changes by country |
| worldometer_data.csv | Snapshot data — total cases, deaths, recoveries, population, testing data per country |

---

## Data Cleaning Steps

### Grouped Dataset (df1)
- Converted Date column from object to datetime format
- Detected and handled negative values in Active, New Deaths and New Recovered columns using clip
- Renamed columns to remove spaces and special characters for Power BI compatibility

### Worldometer Dataset (df2)
- Filled missing values in numeric columns with 0
- Filled missing Population column with median value
- Filled missing Continent and WHO Region with Unknown
- Renamed all columns to snake_case for consistency
- Cleaned and renamed Serious,Critical column to Serious_Critical
- Dropped original problematic column after transformation

---

## Cleaning Approach

| Issue | Strategy |
|---|---|
| Negative values in daily metrics | Clipped to 0 using .clip(lower=0) |
| Missing numeric values | Zero imputation |
| Missing population values | Median imputation |
| Missing categorical values | Labeled as Unknown |
| Non-standard column names | Renamed to snake_case |

---

## Output

Both cleaned datasets were exported as CSV files for direct import into Power BI:

- grouped_data_cleaned.csv
- worldometer_data_cleaned.csv

---

## Author

Arshiyan Mairaj
[LinkedIn](https://linkedin.com/in/arshiyanmairaj/) | [GitHub](https://github.com/Arshiyan7)