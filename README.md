<p align="center">
  <h1 align="center">IBM Data Analyst Capstone Project — Technology Trends Among Developers</h1>
  <p align="center">
    End-to-end capstone workflow: data collection → wrangling → EDA → visualization → dashboard → stakeholder presentation
  </p>
  <p align="center">
    <b>Author:</b> Rooshikesh Bhatt
  </p>
</p>

---

## Overview

This repository contains my capstone project work from the **IBM Data Analyst Professional Certificate**. The objective is to analyze developer survey data (and supporting sources) to identify:

- **Current technology usage** among developers  
- **Future technology interest** (what developers want to work with next)  
- **Demographic patterns** that can inform hiring, training, and technology strategy  

Deliverables include:
- Jupyter notebooks implementing each stage of the analytics workflow  
- A **dashboard export (PDF)** from the BI/dashboarding stage  
- A **final presentation (PDF/PPTX)** summarizing findings and implications  

---

## Repository Contents

### High-level structure
- `Task 1/` — Data collection (APIs + web scraping) + initial dataset exploration  
- `Task 2/` — Data wrangling (duplicates, missing values, normalization)  
- `Task 3/` — Exploratory Data Analysis (EDA), distributions, outliers, correlations  
- `Task 4/` — Data visualization (histograms, box plots, scatter, pie, stacked, line, bar) + SQL/database demo  
- `Task 5/` — Dashboard export (PDF)  
- `Task 6/` — Final stakeholder presentation (PDF + PPTX)

---

## Quick Links (Key Deliverables)

- **Dashboard (PDF export):** [`Task 5/Stack Overflow Dashboard.pdf`](Task%205/Stack%20Overflow%20Dashboard.pdf)
- **Final Presentation (PDF):** [`Task 6/DataAnalystPresentation.pdf`](Task%206/DataAnalystPresentation.pdf)
- **Final Presentation (PPTX):** [`Task 6/DataAnalystPresentation.pptx`](Task%206/DataAnalystPresentation.pptx)

---

## Data Sources (as implemented in notebooks/presentation)

The capstone uses multiple sources and collection methods:

1. **API-style dataset ingestion**
   - Notebook uses a hosted `jobs.json` (GitHub Jobs API–style schema) and an example public API endpoint used in the lab context.

2. **Web scraping**
   - Scrapes a provided HTML page containing programming languages and salary data and saves the output as a CSV.

3. **Stack Overflow Developer Survey (subset)**
   - Survey datasets are pulled from hosted course storage (CSV and SQLite-based artifacts used throughout wrangling/EDA/visualization).

> Note: This repository primarily stores notebooks and final deliverables. The datasets are downloaded inside notebooks from hosted URLs during execution.

---

## Tools & Libraries

Across the notebooks, the primary Python stack includes:
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `requests`, `bs4 (BeautifulSoup)`
- `sqlite3`
- `openpyxl`
- Additional/optional: `scipy`, `sklearn`, `matplotlib-venn`

---

## Detailed Workflow (Task-by-Task)

### Task 1 — Data Collection

**Goal:** Collect data using APIs and web scraping, and explore the initial survey dataset.

Notebooks:
- **Collecting job data using APIs**
  - [`Task 1/Capstone Project - Lab 2 Collecting_job_data_using_APIs-Lab.ipynb`](Task%201/Capstone%20Project%20-%20Lab%202%20Collecting_job_data_using_APIs-Lab.ipynb)
  - Output artifacts written by notebook:
    - `job-postings.xlsx`
    - `job-postings-techno.xlsx`

- **Web scraping (review)**
  - [`Task 1/Capstone Project - Lab 3 Web-Scraping-Review-Lab.ipynb`](Task%201/Capstone%20Project%20-%20Lab%203%20Web-Scraping-Review-Lab.ipynb)

- **Web scraping (hands-on)**
  - [`Task 1/Capstone Project - Lab 4 Web-Scraping-Lab.ipynb`](Task%201/Capstone%20Project%20-%20Lab%204%20Web-Scraping-Lab.ipynb)
  - Output artifact written by notebook:
    - `popular-languages.csv`

- **Explore survey dataset**
  - [`Task 1/Capstone Project - Lab 5 M1ExploreDataSet-lab_V2.ipynb`](Task%201/Capstone%20Project%20-%20Lab%205%20M1ExploreDataSet-lab_V2.ipynb)

---

### Task 2 — Data Wrangling

**Goal:** Identify and treat duplicates, handle missingness, and normalize/transform relevant variables.

Notebooks:
- **Finding duplicates**
  - [`Task 2/Capstone Project - Lab 6 Finding Duplicates_v2.ipynb`](Task%202/Capstone%20Project%20-%20Lab%206%20Finding%20Duplicates_v2.ipynb)

- **Removing duplicates**
  - [`Task 2/Capstone Project - Lab 7 Removing Duplicates_v2.ipynb`](Task%202/Capstone%20Project%20-%20Lab%207%20Removing%20Duplicates_v2.ipynb)

- **Finding missing values**
  - [`Task 2/Capstone Project - Lab 8 Finding Missing Values.ipynb`](Task%202/Capstone%20Project%20-%20Lab%208%20Finding%20Missing%20Values.ipynb)

- **Imputing missing values**
  - [`Task 2/Capstone Project - Lab 9 Imput Missing Values.ipynb`](Task%202/Capstone%20Project%20-%20Lab%209%20Imput%20Missing%20Values.ipynb)

- **Normalizing data**
  - [`Task 2/Capstone Project - Lab 10 Normalizing Data.ipynb`](Task%202/Capstone%20Project%20-%20Lab%2010%20Normalizing%20Data.ipynb)

- **End-to-end wrangling notebook**
  - [`Task 2/Capstone Project - Lab 11 M2DataWrangling-lab-v2.ipynb`](Task%202/Capstone%20Project%20-%20Lab%2011%20M2DataWrangling-lab-v2.ipynb)

---

### Task 3 — Exploratory Data Analysis (EDA)

**Goal:** Understand the dataset structure, distributions, outliers, and relationships/correlations.

Notebooks:
- **EDA**
  - [`Task 3/Capstone Project - Lab 12 Exploratory Data Analysis.ipynb`](Task%203/Capstone%20Project%20-%20Lab%2012%20Exploratory%20Data%20Analysis.ipynb)
  - Output artifact written by notebook:
    - `modified_dataset.csv`

- **Distributions**
  - [`Task 3/Capstone Project - Lab 13 Finding How The Data is Distributed.ipynb`](Task%203/Capstone%20Project%20-%20Lab%2013%20Finding%20How%20The%20Data%20is%20Distributed.ipynb)

- **Outliers**
  - [`Task 3/Capstone Project - Lab 14 Finding Outliers.ipynb`](Task%203/Capstone%20Project%20-%20Lab%2014%20Finding%20Outliers.ipynb)

- **Correlation**
  - [`Task 3/Capstone Project - Lab 15 Finding Correlation.ipynb`](Task%203/Capstone%20Project%20-%20Lab%2015%20Finding%20Correlation.ipynb)

---

### Task 4 — Data Visualization

**Goal:** Create a comprehensive visualization suite, and demonstrate database-backed querying/analysis where applicable.

Notebooks:
- **Data visualization (includes SQL/database demos)**
  - [`Task 4/Capstone Project - Lab 16 Data Visualization.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2016%20Data%20Visualization.ipynb)

- **Histogram**
  - [`Task 4/Capstone Project - Lab 17 Data Visualization - Histogram.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2017%20Data%20Visualization%20-%20Histogram.ipynb)

- **Box plot**
  - [`Task 4/Capstone Project - Lab 18 Box Plot.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2018%20Box%20Plot.ipynb)

- **Scatter plot**
  - [`Task 4/Capstone Project - Lab 19 Scatter Plot.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2019%20Scatter%20Plot.ipynb)

- **Pie charts**
  - [`Task 4/Capstone Project - Lab 21 Pie Charts.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2021%20Pie%20Charts.ipynb)

- **Stacked charts**
  - [`Task 4/Capstone Project - Lab 22 Stacked Charts.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2022%20Stacked%20Charts.ipynb)

- **Line charts**
  - [`Task 4/Capstone Project - Lab 23 Line Charts.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2023%20Line%20Charts.ipynb)

- **Bar charts**
  - [`Task 4/Capstone Project - Lab 24 Bar Charts.ipynb`](Task%204/Capstone%20Project%20-%20Lab%2024%20Bar%20Charts.ipynb)

---

## Results Snapshot (From Dashboard + Presentation)

### Current Technology Usage — Top Languages (Have Worked With)

| Rank | Language | Respondents |
|---:|---|---:|
| 1 | JavaScript | 14,943 |
| 2 | SQL | 12,602 |
| 3 | HTML/CSS | 12,410 |
| 4 | TypeScript | 10,709 |
| 5 | Python | 9,590 |
| 6 | Bash/Shell (all shells) | 7,244 |
| 7 | C# | 6,340 |
| 8 | Java | 5,982 |
| 9 | PHP | 4,644 |
| 10 | PowerShell | 3,438 |

### Future Technology Trend — Top Languages (Want To Work With)

| Rank | Language | Respondents |
|---:|---|---:|
| 1 | JavaScript | 11,541 |
| 2 | SQL | 10,944 |
| 3 | TypeScript | 10,437 |
| 4 | HTML/CSS | 10,016 |
| 5 | Python | 8,919 |
| 6 | Go | 5,661 |
| 7 | Rust | 5,597 |
| 8 | C# | 5,590 |
| 9 | Bash/Shell (all shells) | 5,582 |
| 10 | Java | 4,048 |

### Databases — Current vs Future Interest (Highlights)

**Current (Have Worked With):** PostgreSQL, MySQL, SQLite, MongoDB, Microsoft SQL Server, Redis, MariaDB, Elasticsearch, DynamoDB, Oracle.

**Future (Want To Work With):**

| Rank | Database | Respondents |
|---:|---|---:|
| 1 | PostgreSQL | 12,193 |
| 2 | Redis | 6,384 |
| 3 | SQLite | 6,295 |
| 4 | MySQL | 6,204 |
| 5 | MongoDB | 5,618 |
| 6 | Microsoft SQL Server | 4,345 |
| 7 | Elasticsearch | 3,665 |
| 8 | MariaDB | 3,078 |
| 9 | DynamoDB | 2,154 |
| 10 | Supabase | 1,623 |

### Platforms (Future Interest — From Dashboard)

Top platforms developers want to work with include:
- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud
- Cloudflare
- Digital Ocean
- Vercel
- Firebase
- Hetzner
- Supabase
- Netlify

### Demographics (Age Distribution — From Dashboard)

| Age group | Respondents |
|---|---:|
| 25–34 years old | 7,788 |
| 35–44 years old | 5,149 |
| 18–24 years old | 2,988 |
| 45–54 years old | 2,053 |
| 55–64 years old | 632 |
| Under 18 years old | 136 |
| 65 years or older | 75 |
| Prefer not to say | 24 |

---

## Conclusions & Implications (From Final Presentation)

Key takeaways communicated in the final deck:
- Most technologies (languages, databases, platforms, frameworks, tools) remain broadly relevant into the coming year.
- The analyzed respondent profile is concentrated in the 25–34 age group, with bachelor’s-level education and a strong representation of full-stack development roles.
- Developers prioritize three major factors when choosing technologies:
  1. Strong performance for complex ecosystems  
  2. Comprehensive service offerings (AI/compute/storage/database/networking)  
  3. Free editions/open options to reduce cost  

Practical implications:
- Continue and deepen training on consistently dominant technologies (e.g., JavaScript/SQL/TypeScript/Python).
- Begin proactive upskilling for emerging interests (e.g., Go and Rust).
- Maintain cloud and web ecosystem readiness (AWS/Azure, Node.js/React).

---

## How to Run Locally

### 1) Clone the repository
```bash
git clone https://github.com/rooshikeshbhatt/IBM-Data-Analyst-Capstone-Project.git
cd IBM-Data-Analyst-Capstone-Project
```

### 2) Create and activate a virtual environment (recommended)

**Windows (PowerShell):**
```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS/Linux:**
```bash
python -m venv .venv
source .venv/bin/activate
```

### 3) Install dependencies
```bash
pip install -U pip
pip install pandas numpy matplotlib seaborn requests beautifulsoup4 openpyxl notebook
```

### 4) Launch Jupyter
```bash
jupyter notebook
```

### 5) Run notebooks by task order
Start in **Task 1** and proceed sequentially through **Task 6**.

> Some notebooks download datasets at runtime from hosted course storage (e.g., via `wget`). Ensure you have internet access when executing.

---

## Recommended Enhancements (Optional, Portfolio Upgrade)

To make this repository more portfolio-ready, consider adding:
- `requirements.txt` (or `environment.yml`)
- `/assets/` folder with dashboard screenshots and a few key plots
- A small “end-to-end pipeline” notebook/script that runs the main analysis workflow

---

## License

MIT License (as stated in the repository).

---

## Acknowledgements

- IBM Data Analyst Professional Certificate (capstone structure and lab framework)
- Stack Overflow Developer Survey (source dataset referenced by the capstone)
