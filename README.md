# Web-Scraper
A Web scrapper made using python libraries
Here is the full README content:

---

# Hockey Stats Web Scraper

---

## Table of Contents

- [Project Title](#project-title)
- [Project Description](#project-description)
- [Project Vision](#project-vision)
- [Key Features](#key-features)
- [Future Scope](#future-scope)

---

## Project Title

**Web Scraping — Hockey Stats Scraper**

---

## Project Description

This project is a lightweight Python web scraper built to extract hockey team statistics from [ScrapeThisSite](https://www.scrapethissite.com/pages/forms/). It navigates through paginated tables containing historical NHL team data — including team names, years, wins, losses, goals, and more — and consolidates everything into a clean, analysis-ready CSV file.

The scraper is structured around **4 focused functions** that each handle a distinct responsibility: fetching a page, extracting headers, extracting row data, and orchestrating the full multi-page scrape.

**Tech Stack:**
- `Python 3.x`
- `requests` — HTTP page fetching
- `BeautifulSoup (lxml)` — HTML parsing
- `pandas` — Data structuring and CSV export

**Usage:**
```bash
pip install requests beautifulsoup4 lxml pandas
python hockey_scraper.py
```
Output is saved as `hockey_data.csv` in the working directory.

---

## Project Vision

The vision of this project is to demonstrate how real-world structured data locked inside paginated HTML tables can be cleanly extracted, transformed, and made available for downstream analysis — with minimal, well-organised code.

Beyond the immediate scraping task, this project serves as a reusable template for anyone looking to scrape similar paginated tabular websites. The goal is to promote good scraping practices: respect for site structure, clean separation of concerns across functions, and reproducible data outputs that can feed directly into data analysis or visualisation pipelines.

---

## Key Features

- **Paginated scraping** — Automatically iterates across all available pages with a configurable range.
- **Clean modular design** — Only 4 functions; each does one thing well.
- **Automatic header extraction** — Column names are pulled dynamically from the page itself, not hardcoded.
- **Robust row parsing** — Handles the quirky empty 5th column gracefully by removing it automatically.
- **CSV export** — Results are saved directly to a `.csv` file with `pandas`, ready for Excel, Jupyter, or any data tool.
- **Configurable output path** — The output file location can be set at call time without editing the code.

---

## Future Scope

- **Search & filter support** — Add query parameters to scrape only specific teams or seasons using the site's built-in search functionality.
- **Database integration** — Store scraped data into a SQLite or PostgreSQL database instead of (or in addition to) CSV, enabling incremental updates and querying.
- **Scheduled scraping** — Automate periodic runs using `cron` or a task scheduler so the dataset stays current.
- **Data visualisation** — Build a simple dashboard (e.g. with `matplotlib` or `plotly`) to visualise win/loss trends, goals over time, and team comparisons directly from the scraped data.
- **Error handling & retries** — Add exponential back-off and retry logic for transient network failures to make the scraper production-grade.
- **Multi-site support** — Abstract the scraper to support additional hockey or sports data sources with minimal configuration changes.
