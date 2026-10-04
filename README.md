# Book Extractor

A lightweight Jupyter Notebook project for extracting book-related data from online sources. The notebook searches a topic on LibGen, pulls book titles, looks up rating information on Goodreads, and sorts the results by popularity and quality.

This repository is intentionally simple: it focuses on one notebook workflow and demonstrates how to gather bibliographic information from public web pages using Python.

## What this project does

The notebook in this repository can:

- search LibGen for books based on a keyword or topic
- extract book titles from search results
- query Goodreads for matching titles
- parse average ratings and number of ratings
- rank books by rating and rating volume
- collect download links for matching titles
- save downloaded files into a local folder

In short, this project is a practical example of scraping and metadata collection for book discovery.

## Repository contents

- `Books.ipynb` — the main notebook containing the extraction workflow
- `README.md` — project documentation

## Why it exists

This project is useful for learning and experimenting with:

- web scraping with Python
- parsing HTML with BeautifulSoup
- working with public metadata sources
- notebook-based data collection workflows
- building small research or recommendation tools

## Requirements

Before running the notebook, install the following:

- Python 3
- Jupyter Notebook or JupyterLab
- `requests`
- `beautifulsoup4`

Install dependencies with:

```bash
pip install jupyter requests beautifulsoup4
```

## Quick start

1. Clone the repository:

```bash
git clone https://github.com/mohammad-shahwan/Book-Extractor.git
cd Book-Extractor
```

2. Create and activate a virtual environment (optional but recommended):

```bash
python -m venv .venv
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install jupyter requests beautifulsoup4
```

4. Launch the notebook:

```bash
jupyter notebook Books.ipynb
```

Or open it in JupyterLab:

```bash
jupyter lab
```

## How the notebook works

The workflow is organized into a few key steps:

1. Search LibGen for a topic such as `Entrepreneurship`
2. Extract book titles from the HTML results
3. Search each title on Goodreads
4. Extract the rating summary from Goodreads pages
5. Filter out entries without valid ratings
6. Sort the valid results by average rating
7. Optionally collect download links and save files locally

## Example use case

The notebook currently demonstrates an `Entrepreneurship` search and then ranks the returned books by Goodreads rating. This makes it a useful example for exploring how books can be discovered and ranked from search results.

## Important notes

- This project depends on external websites and their page structure. If those sites change, the scraper may need updates.
- Some pages may not return metadata consistently, so the script may skip titles without valid ratings.
- This repository is intended for educational, research, or experimentation purposes.
- Please respect the terms of service and copyright policies of the sites you access.

## Project status

The repository is currently a notebook-based prototype focused on data extraction and ranking, with a simple workflow centered around `Books.ipynb`.

## License

No explicit license file is included in the repository, so the project is currently unlicensed unless otherwise stated by the repository owner.

## Author

- Mohammad Shahwan

## Contributing

This is a small personal project, but suggestions and improvements are welcome. If you would like to improve the notebook or add more robust parsing logic, feel free to open an issue or submit a pull request.
