# UNESCO World Heritage Sites — Cultural Intelligence Pipeline

## Overview

This project builds an end-to-end ETL pipeline that pulls live data from the
UNESCO World Heritage List API, cleans and enriches it, loads it into Google
Sheets, and visualizes key findings in a Looker Studio dashboard.

The pipeline demonstrates the full cycle: extract → transform → load — applied
to a real public dataset with 1,248 heritage sites across 167 countries.

---

## Key Findings

1. **Europe dominates global heritage recognition**: 580 out of 1,248 sites
(46%) are in Europe and North America, despite representing one of five UNESCO
regions.

2. **Arab League countries are significantly underrepresented** :96 sites
(7.7% of the global total) across 19 member states, despite the region's
historical depth and civilizational legacy.

3. **Inscriptions peaked in the 1990s** : 308 sites were added that decade,
nearly double the 1980s pace. The number has declined each decade since.

4. **Arab States has the highest endangered site rate** : 22 out of 96 sites
(23%) are on the danger list, compared to just 1.2% for Europe and North
America. Conflict, instability, and under-resourcing are probable factors.

---

## The Question

How does UNESCO World Heritage inscription activity vary across regions, and what patterns emerge in endangerment, category, and criteria?

---

## Pipeline 
UNESCO DataHub API

↓

requests (pagination loop)

↓

pandas (clean + enrich)

↓

gspread (load to Google Sheets)

↓

Looker Studio (dashboard)

---

## Tools & Libraries

Python, requests, pandas, gspread, google-auth, Jupyter Notebook,
Google Sheets, Looker Studio

---

## Data Source

UNESCO World Heritage List:  DataHub API (public with no authentication required)
https://data.unesco.org/explore/dataset/whc001/api/

---

## Dashboard

[View the Looker Studio Dashboard](https://datastudio.google.com/reporting/cd93f120-f745-46f0-9a17-91ce92486fb9) 

---

## How to Run

1. Clone the repo
2. Add your own `credentials.json` (Google Service Account with Sheets + Drive access)
3. Create a Google Sheet named `UNESCO Heritage Pipeline` and share it with your service account
4. Run all cells in `unesco_exploration.ipynb` top to bottom

---

## About

Built by Nour Elhouda Bencherif as part of the Elhouda Lab portfolio.
Decision Science | Data Analytics | Culture & Society



