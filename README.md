# Web_Scraping_EvoAstra

A web scraping project that extracts remote job data from the RemoteOK API, performs data cleaning, and generates insightful visualizations to analyze job market trends.

## Table of Contents

- Overview
- Features
- Project Structure
- Prerequisites
- Installation
- Usage
- Data Pipeline
- Analysis and Visualizations
- Output Files
- Technologies Used
- License

## Overview

This project demonstrates end-to-end web scraping and data analysis workflow:

- Fetches real-time remote job listings from the RemoteOK API
- Cleans and preprocesses raw data
- Performs exploratory data analysis (EDA)
- Generates informative visualizations
- Provides insights into remote job market trends

## Features

- Fetches job data from RemoteOK API with proper headers to avoid blocking
- Extracts key job details including title, company, skills, location, and URL
- Removes duplicates and handles missing data
- Generates multiple visualization charts for analysis
- Analyzes skill demand trends across job titles
- Provides location distribution insights

## Project Structure

```
Web_Scraping_EvoAstra/
├── Data/
│   ├── cleaned/
│   │   └── remoteok_jobs_cleaned.csv
│   └── raw/
│       └── remote_jobs.csv
├── Plots/
│   ├── job_type_distribution.png
│   ├── skill_frequency_comparison.png
│   ├── top_job_titles.png
│   └── top_skills.png
├── Web_Scraping/
│   └── web_scraping.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Prerequisites

- Python 3.8 or higher
- Internet connection for API requests
- Basic understanding of data analysis and visualization

## Installation

1. Clone the repository:

```
git clone https://github.com/yourusername/Web_Scraping_EvoAstra.git
```

2. Navigate to the project directory:

```
cd Web_Scraping_EvoAstra
```

3. Create a virtual environment (optional but recommended):

```
python -m venv venv
```

4. Activate the virtual environment:

- On Windows:

```
  venv\Scripts\activate

```

- On macOS/Linux:

```
  source venv/bin/activate

```

5. Install the required dependencies:

```
pip install -r requirements.txt
```

## Usage

1. Open the Jupyter notebook:

```
jupyter notebook Web_Scraping/web_scraping.ipynb
```

2. Run the cells sequentially to:
   - Import required libraries
   - Fetch job data from RemoteOK API
   - Save raw data to CSV
   - Clean and preprocess the data
   - Perform exploratory data analysis
   - Generate visualizations

## Data Pipeline

The data processing pipeline consists of the following stages:

- **Data Fetching**: Uses requests library to fetch JSON data from RemoteOK API
- **Data Extraction**: Parses job details including position, company, tags, and location
- **Data Storage**: Saves raw data to CSV format
- **Data Cleaning**:
  - Removes rows with missing critical fields (Title, Company)
  - Drops duplicate entries based on Title and Company
  - Converts text to lowercase for consistency
- **Data Export**: Saves cleaned data to a separate CSV file

## Analysis and Visualizations

The project generates several visualizations:

- **Top Skills Chart**: Bar chart showing the most demanded skills in remote jobs
- **Job Type Distribution**: Pie chart displaying the distribution of job types
- **Top Job Titles**: Horizontal bar chart of the most common remote job titles
- **Skill Frequency Comparison**: Extended analysis of skill demand across job postings
- **Location Analysis**: Percentage breakdown of job locations

## Output Files

- **Raw Data**: `Data/raw/remote_jobs.csv` - Contains scraped job data before cleaning
- **Cleaned Data**: `Data/cleaned/remoteok_jobs_cleaned.csv` - Processed data ready for analysis
- **Visualizations**:
  - `Plots/top_skills.png` - Top 10 most demanded skills
  - `Plots/job_type_distribution.png` - Job type distribution
  - `Plots/top_job_titles.png` - Most common job titles
  - `Plots/skill_frequency_comparison.png` - Extended skill frequency analysis

## Technologies Used

- **Python** - Programming language
- **BeautifulSoup4** - HTML/XML parsing library
- **Pandas** - Data manipulation and analysis
- **Requests** - HTTP library for API requests
- **Matplotlib** - Data visualization library
- **Seaborn** - Statistical data visualization
- **Jupyter Notebook** - Interactive computing environment

## License

This project is licensed under the terms included in the LICENSE file.

---

Created by EvoAstra - Web Scraping and Data Analysis Project
