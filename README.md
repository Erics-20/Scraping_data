# Scraping_data
The aim of this repository is to interact and extract data of web pages using selenium, pandas and APIs

# UNMSM Admission Results Scraper 

## What does the project do?
This project is an automated Web Scraping tool built with Python. Its primary goal is to extract the admission exam results from the Universidad Nacional Mayor de San Marcos (UNMSM) website. 

Instead of manually clicking through hundreds of pages, this script uses **Selenium** to programmatically navigate the university's admissions portal. It iterates through every single career link, bypasses the default JavaScript pagination (DataTables) by forcing the site to display all applicants at once, extracts the visible HTML data, and consolidates the information of all careers into a single, clean Excel (`.xlsx`) file using **Pandas**.

## How to install the dependencies?
To run this script, you need Python installed on your machine along with a few external libraries. You can install all the required dependencies at once by running the following command in your terminal:

```bash
pip install selenium pandas openpyxl beautifulsoup4 webdriver-manager
```

* Selenium & webdriver-manager: Used for browser automation and interaction with JavaScript elements (like dropdowns).

* Pandas: Used to parse the HTML tables and structure the data into DataFrames.

* BeautifulSoup & StringIO: Used as helper tools to safely parse HTML content into Pandas.

* Openpyxl: The engine required by Pandas to export the final DataFrame to an Excel file.

## How to run the script?
Open the project folder in your preferred IDE (like Visual Studio Code) or Jupyter Notebook environment.

Important path configuration: By default, the script is configured to save the output in a specific local absolute path (/Users/macbookair/Desktop/...). Before running, locate "Paso 1" in the code and update the output_dir variable to match your desired local folder path or change it to a relative path (e.g., "./output").

Run the script. If you are using a standard .py file, execute:

```bash
python nombre_del_archivo.py
```

The script will automatically launch a hidden/background Chrome browser, navigate through all the career links, and print its progress in the terminal.

## What does the output contain?
The script generates an Excel file named resultados_unmsm_2026_consolidado.xlsx inside your specified output folder.

This file contains a consolidated tabular dataset of the applicants across all processed careers. The columns include the applicant's code, full name, and the specific career they applied to.



# Scraping & API Data Analysis

## What does the project do?
This project extracts and analyzes data from the video game industry using the RAWG API. The script allows users to obtain global statistics, compare performance across platforms (PC vs. PS5), analyze genres, and export a ranking of the best games based on professional critic reviews (Metacritic).

## How to install the dependencies?
Make sure you have Python installed and run the following command in your terminal to install the required libraries:

```bash
pip install requests pandas
```

## How to run the script?
1. Get your API_KEY en rawg.io.

2. Open api/tarea_rawg_api.ipynb notebook.

3. Paste your key in API_KEY.

4. Execute.

## What does the output contain?
* Console analysis: Rating comparisons, tables of popular games, and averages by genre/year.

* CSV file: A report located at api/output/top20_rawg.csv with the top 20 games, including name, rating, Metacritic score, release date, and primary genre.
