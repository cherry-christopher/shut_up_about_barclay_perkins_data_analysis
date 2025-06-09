# Shut Up About Barclay Perkins Data Analysis

A large-scale, open data project extracting and analyzing over 1,000 historical beer recipes from the "Shut Up About Barclay Perkins" blog.  
This project uses web scraping, LLM-based table extraction, and one-hot encoding to build a machine-readable dataset suitable for classification, clustering, and historical trend analysis.

---

## Project Goals

- Scrape all “Let’s Brew” recipe posts (approx. 1,100 entries)
- Extract recipe tables using LLMs
- Normalize and one-hot encode brewing data (malts, hops, gravities, etc.)
- Build a structured dataset of ingredients and brewing parameters
- Analyze and visualize historical brewing trends

---

## Project Structure

```text
shut_up_about_barclay_perkins_data_analysis/
├── data/
│   └── raw_html/                # Scraped full HTML blog posts
│   └── extracted_tables.jsonl   # Table text parsed by LLM
│   └── encoded_dataset.csv      # One-hot encoded dataset
├── notebooks/
│   └── 01_explore.ipynb         # EDA, trends, model results
├── src/
│   ├── scrape_posts.py          # Full scraper with pagination
│   ├── extract_tables.py        # Table extraction for LLM parsing
│   ├── encode_features.py       # One-hot encoding + normalization
│   └── model.py                 # Style classification and clustering
├── Makefile                     # Workflow automation
├── requirements.txt             # Project dependencies
└── README.md                    # This file

Use Cases

- How well do historical style labels correspond to data-driven ingredient clusters?
- Are beer styles like "Porter" and "Stout" or "IPA" and "Pale Ale" physically distinct, or do they reflect evolving trade language?
- Can you classify historical beer styles by ingredients alone?

Tech Stack

requests - for web scraping
BeautifulSoup - for HTML parsing
OpenAI API - for table parsing using LLMs
pandas - for data wrangling and encoding
scikit-learn - for classification and cluster analysis
matplotlib - for visualization
Makefile - for command-line automation
GCS / BigQuery - optional cloud storage and analysis

Development Status

Scraper with pagination complete
Table extraction in progress
Feature encoding planned
Modeling and analysis to follow
License

MIT License.
All recipe content copyright Ron Pattinson.
This project is for educational and research use only and is not affiliated with the original site.

Author

Chris Cherry
https://github.com/cherry-christopher
Economics and Data Science. Brewing industry background.
Open to roles in development, data analytics, sales, and leadership.
