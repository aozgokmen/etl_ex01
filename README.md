
# ETL Pipeline for GDP Data Extraction, Transformation, and Loading

This project demonstrates an ETL (Extract, Transform, Load) pipeline that retrieves GDP data from a web source, transforms it, and loads it into both a CSV file and a SQLite database.

## Project Overview

The goal is to automate the extraction of GDP data from the Wikipedia page for countries by GDP (nominal), transform the values from "Million USD" to "Billion USD" (rounded to two decimal places), and then load the transformed data into:
- A CSV file named `Countries_by_GDP.csv`
- A SQLite database file `World_Economies.db`

Additionally, a query is run to display countries with economies greater than 100 billion USD, and all the process steps are logged.

### Data Source

The data is sourced from [Wikipedia's List of Countries by GDP](https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29).

## Requirements

You’ll need the following libraries to run the project:
```bash
pip install requests beautifulsoup4 pandas sqlite3
```

## Features

- Data Extraction: Scrapes GDP data from the provided URL.
- Data Transformation: Converts GDP values from "Million USD" to "Billion USD" and rounds to two decimal places.
- Data Loading:
  - Saves the data to `Countries_by_GDP.csv`.
  - Loads the data into an SQLite database (`World_Economies.db`) in a table called `Countries_by_GDP`.
- Database Query: Retrieves countries with GDP > 100 billion USD.
- Logging: Logs the entire process in `etl_project_log.txt`.

## File Structure

- `etl_project_gdp.py` - The main Python script that performs the ETL process.
- `Countries_by_GDP.csv` - The output CSV file.
- `World_Economies.db` - The SQLite database.
- `etl_project_log.txt` - Log file tracking the execution steps.

## How to Run

1. Clone the repository.
2. Ensure you have the required libraries installed.
3. Run the Python script:
   ```bash
   python etl_project_gdp.py
   ```
4. Check the output:
   - View `Countries_by_GDP.csv` for the transformed data.
   - Query `World_Economies.db` to see the stored data.

