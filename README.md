# Victoria's Drug Geography

A GIS look at a decade of recorded drug offences in Victoria, Australia: which drugs, where, and how the picture changed through the COVID-19 lockdowns. Covers 323,654 drug offences across 79 local government areas (LGAs), financial years 2017–2026 (July 2016 to June 2026).

## Notebooks

| Notebook | What it does |
|---|---|
| [`00_data_prep`](notebooks/00_data_prep.ipynb) | Cleans the CSA workbooks and ABS boundaries into `data/processed/` |
| [`01_crime_overview`](notebooks/01_crime_overview.ipynb) | All offences: statewide trend, offence divisions, crime mix by region |
| [`02_drug_offence`](notebooks/02_drug_offence.ipynb) | Drug groups over time, regional drug profiles, meth mapped across three periods |
| [`03_drug_map`](notebooks/03_drug_map.ipynb) | Interactive folium map, one layer per drug group, saved to `notebooks/outputs/03_drug_map.html` |

Figures are saved to `notebooks/outputs/`.

## Data

- **Crime Statistics Agency Victoria** ([crimestatistics.vic.gov.au](https://www.crimestatistics.vic.gov.au/)):
  recorded offences and criminal incidents by LGA, year ending June 2026.
- **ABS ASGS Edition 3** LGA 2024 boundaries (downloaded by `00_data_prep` if missing).

The processed files in `data/processed/` are in the repo, so notebooks 01–03 run straight away. To re-run `00_data_prep`, download the three CSA workbooks into `data/raw/`.

These are *recorded* offences, so they reflect where police find drugs as well as where drugs are.

## Setup

```bash
pip install "pandas<3" geopandas folium seaborn scipy matplotlib pyarrow openpyxl
```
