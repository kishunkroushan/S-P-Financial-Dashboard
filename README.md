# S&P Financial Dashboard

An interactive Tableau dashboard analyzing financial performance, profitability, risk, and growth across selected S&P 500 companies from 2014–2018.

## Dashboard Preview

The dashboard is organized into four analytical sections:

* **Overview** — Revenue, net income, average profit, ROE, company rankings, and performance trends
* **Profitability** — Profit margin trends, sector profitability, and ROE comparisons
* **Risk & Health** — Debt, leverage, liquidity, cash flow, and financial health indicators
* **Growth** — Revenue growth, EPS growth, free cash flow growth, and company performance

[View dashboard files](dashboard/)

![Dashboard Overview](screenshots/Dashboard%201%20%282%29.png)

![Profitability](screenshots/Dashboard%202.png)

![Risk & Health](screenshots/Dashboard%203.png)

![Growth](screenshots/Dashboard%204.png)

## Project Overview

This project analyzes historical financial data from **2014 to 2018** for selected S&P 500 companies and transforms the raw yearly datasets into a structured, Tableau-ready dataset.

The workflow combines Python-based data cleaning and feature engineering with an interactive Tableau dashboard to evaluate company performance across profitability, financial risk, liquidity, and growth.

## Data & Analysis Workflow

### 1. Data Preparation

Five yearly financial datasets were loaded and combined into a single dataset using Python.

* 2014
* 2015
* 2016
* 2017
* 2018

The data was cleaned by removing invalid tickers and duplicates, validating classification values, converting financial fields to numeric types, and handling rows without financial information.

Extreme values were capped at the 1st and 99th percentiles for visualization-focused analysis.

### 2. Feature Engineering

Additional analytical categories were created to make the data easier to interpret:

* Profit Margin Tier
* Leverage Bucket
* Revenue Growth Label
* Performance Label
* Class Label

The final Tableau-ready dataset focuses on **11 selected companies**:

`AAPL` · `MSFT` · `NVDA` · `JPM` · `GS` · `KO` · `PEP` · `PG` · `JNJ` · `PFE` · `XOM`

### 3. Dashboard Development

The processed dataset was used to build an interactive Tableau dashboard covering:

* Company and sector profitability
* Revenue and net income trends
* ROE and profit margins
* Debt and leverage
* Liquidity and cash flow
* Revenue and EPS growth
* Company-level performance comparisons

## Key Insights

* Revenue and net income show an overall upward trend across the analyzed period.
* Profitability varies significantly across sectors and companies.
* Industrial companies show strong ROE performance in several years.
* Technology demonstrates relatively consistent profit-margin performance.
* Leverage and liquidity profiles differ substantially across companies.
* Revenue and EPS growth reveal distinct differences in company momentum.
* The dashboard highlights companies with stronger profitability, liquidity, growth, and financial health characteristics.

## Tools & Technologies

| Category        | Tools                 |
| --------------- | --------------------- |
| Data Processing | Python, Pandas, NumPy |
| Data Format     | CSV                   |
| Visualization   | Tableau               |
| Environment     | Google Colab          |

## Repository Structure

```text
S-P-Financial-Dashboard/
│
├── dashboard/
│   └── s&p 500 finance dashboard.twbx
│
├── data/
│   ├── raw/
│   │   ├── 2014_Financial_Data.csv
│   │   ├── 2015_Financial_Data.csv
│   │   ├── 2016_Financial_Data.csv
│   │   ├── 2017_Financial_Data.csv
│   │   └── 2018_Financial_Data.csv
│   │
│   └── processed/
│       └── SP500_Tableau_Final.csv
│
├── notebook/
│   └── finance.py
│
├── screenshots/
│   ├── Dashboard 1 (2).png
│   ├── Dashboard 2.png
│   ├── Dashboard 3.png
│   └── Dashboard 4.png
│
└── README.md
```
