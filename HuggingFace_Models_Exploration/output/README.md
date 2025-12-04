# Output Directory

This directory contains the results of NLP analysis.

## Files

### `news_nlp_analysis_results.csv`
Contains processed news articles with:
- **Title:** Original article title
- **Sentiment:** POSITIVE or NEGATIVE classification
- **Confidence:** Model confidence score (0.0-1.0)
- **Summary:** BART-generated summary
- **Entities:** List of extracted named entities
- **Entity_Count:** Number of entities detected
- **URL:** Source article link

## Usage

Import the CSV into:
- **Excel/Google Sheets** for manual review
- **Power BI/Tableau** for visualization dashboards
- **Python/R** for further statistical analysis
- **Databases** for long-term storage and querying

## Note
Output files are not tracked in Git to keep the repository clean.
