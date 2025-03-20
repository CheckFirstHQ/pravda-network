# Pravda Network Data Collection

![Last Update](https://img.shields.io/github/last-commit/CheckFirstHQ/pravda-network/main?label=Last%20Update)

This repository contains source data collected from the [Pravda Network](https://checkfirst.network/pravda-network-worldwide-expansion-and-llm-wikipedia-pollution/), a collection of Russian news websites across multiple countries and languages. The data is automatically updated hourly, providing a comprehensive dataset for analysis.

## Data Overview

Each CSV file in the `data/` directory represents a sub-domain from the Pravda Network. The files contain metadata extracted from articles, including:

- URL
- Source title
- Source URL
- Canonical URL
- OG:Title
- OG:Description
- Alternate language versions
- Country
- Publication date

## Data Collection Methodology

The data is collected using an automated web scraper that:

1. Traverses all articles listed on each domain
2. Extracts metadata from article pages

## Repository Structure

```
data/
├── abkhazia.news-pravda.com.csv.gz
├── albania.news-pravda.com.csv.gz
├── algeria.news-pravda.com.csv.gz
└── ...
```

## Automating Data Collection

This repository is updated hourly via an automated script. The update process:

1. Checks each domain for new articles
2. Appends new data to the appropriate CSV files
3. Commits and pushes changes to this repository

## File Format

All CSV files use the following header structure:

```
URL,Source Title,Source URL,Canonical,OG:Title,OG:Description,Alternates,Country,Publication Date
```

Example row:
```
https://domain.com/article/123.html,Original Source,https://source.com,https://domain.com/canonical,Title,Description,https://alt1.com(en);https://alt2.com(fr),Country,2024-03-15T14:30:00Z
```

## License and Attribution

This dataset is provided for research and analysis purposes. When using this data, please cite:

```
CheckFirst. Pravda Network Data Collection. GitHub Repository. https://github.com/CheckFirstHQ/pravda-network
```

## Updates

This repository is automatically updated hourly. The last update timestamp can be found at the top of this README.

---

Maintained by [CheckFirst](https://checkfirst.network)
