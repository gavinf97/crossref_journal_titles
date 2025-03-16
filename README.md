# Crossref Journal Titles Download - For DOME Registry

## Overview
This repository contains a IPYNB Python script usable on Google Colab that retrieves a comprehensive list of academic journals from the Crossref API and exports them to a CSV file. The resulting dataset provides an extensive registry of journal titles, and their publishers, which can be utilized for the DOME Registry as a fixed vocabulary of journal titles.

## Contents
- `CrossRef_Journals_CSV_Generator_20250316.ipynb`: Python script to retrieve journal data from Crossref API
- `crossref_journals.csv`: CSV file containing journal titles, and publishers (generated when script is run)

## Requirements
- Python 3.6 or higher
- `requests` library (install via `pip install requests`)

## Usage
1. Replace the placeholder email in the script with your actual email address:
   ```python
   "User-Agent": "JournalExporter/1.0 (mailto:your-email@example.com)"
   ```

2. Open the interactive IPYNB on Google Colab or Jupyter Notebooks.

3. When prompted, choose whether to retrieve all journals or specify a maximum number.

4. The script will generate a CSV file named `crossref_journals.csv` containing the journal data.

## CSV File Structure
The generated CSV file contains the following columns:
- `title`: The full title of the journal
- `issn`: Comma-separated list of ISSNs associated with the journal (print and online)
- `publisher`: The name of the journal's publisher

## DOME Registry Usage Notes
This dataset is specifically prepared for DOME registry purposes, providing a comprehensive and authoritative record of academic journal titles. When using this data for domain registry:

1. Publisher information can be used for registry categorization and filtering.

## API Considerations
- The script includes appropriate rate limiting (1 second between requests) to respect Crossref's API guidelines
- Pagination is handled automatically to retrieve the complete dataset
- Progress reporting is included to monitor the data collection process

## Maintenance
To keep the journal title usage up-to-date, consider:
- Running this script periodically (monthly/quarterly) to capture new journals
- Implementing a diff comparison with previous exports to identify new additions
- Maintaining version control of the CSV files to track changes over time

## License
This script is designed for DOME Registry purposes. When using the data, please respect Crossref's terms of service and provide appropriate attribution.
