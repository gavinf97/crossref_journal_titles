# Crossref Journal Registry

## Overview
This repository contains a Python script that retrieves a comprehensive list of academic journals from the Crossref API and exports them to a CSV file. The resulting dataset provides an extensive registry of journal titles, their ISSNs, and publishers, which can be utilized for domain registry purposes.

## Contents
- `crossref_journals.py`: Python script to retrieve journal data from Crossref API
- `crossref_journals.csv`: CSV file containing journal titles, ISSNs, and publishers (generated when script is run)

## Requirements
- Python 3.6 or higher
- `requests` library (install via `pip install requests`)

## Usage
1. Replace the placeholder email in the script with your actual email address:
   ```python
   "User-Agent": "JournalExporter/1.0 (mailto:your-email@example.com)"
   ```

2. Run the script:
   ```bash
   python crossref_journals.py
   ```

3. When prompted, choose whether to retrieve all journals or specify a maximum number.

4. The script will generate a CSV file named `crossref_journals.csv` containing the journal data.

## CSV File Structure
The generated CSV file contains the following columns:
- `title`: The full title of the journal
- `issn`: Comma-separated list of ISSNs associated with the journal (print and online)
- `publisher`: The name of the journal's publisher

## Domain Registry Usage Notes
This dataset is specifically prepared for domain registry purposes, providing a comprehensive and authoritative record of academic journal titles. When using this data for domain registry:

1. The ISSN can serve as a unique identifier for domain registration validation
2. Publisher information can be used for organizational categorization
3. Journal titles provide the basis for domain name allocation

## API Considerations
- The script includes appropriate rate limiting (1 second between requests) to respect Crossref's API guidelines
- Pagination is handled automatically to retrieve the complete dataset
- Progress reporting is included to monitor the data collection process

## Maintenance
To keep the journal registry up-to-date, consider:
- Running this script periodically (monthly/quarterly) to capture new journals
- Implementing a diff comparison with previous exports to identify new additions
- Maintaining version control of the CSV files to track changes over time

## License
This tool is provided for domain registry purposes. When using the data, please respect Crossref's terms of service and provide appropriate attribution.
