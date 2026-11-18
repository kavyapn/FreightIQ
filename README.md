# FreightIQ

Freight price analytics on Indian logistics data: data quality assessment, cleaning, geocoding-based enrichment and exploratory analysis.

HFU Furtwangen University, Data Science team project, structured along the CRISP-DM process.

## What this project does

Freight contracts carry noisy city names, inconsistent destination states and unreliable distances. This work turns the raw transport price data into a clean, enriched dataset that is ready for price modelling.

- **Data understanding:** feature categorisation, distributions, skewness and kurtosis, correlation analysis
- **Data quality assessment:** format conformity, missing values, duplicates, outliers, timeliness
- **Cleaning:** standardised source and destination cities and states, vehicle type and body type, pricing type
- **Enrichment pipeline:** corrected destination state and driving distance per source-destination pair, using geocoding (LocationIQ with Photon as fallback) and distance lookups
- **Exploratory analysis:** distance vs cost, cost trends by year, month, contract type, vehicle type and product, load analysis, price per km by financial year

## Notebooks

| Notebook | Content |
|---|---|
| `01_Data_Understanding_Cleaning_Enrichment.ipynb` | Data loading, quality assessment, cleaning and the enrichment pipeline |
| `02_Exploratory_Data_Analysis.ipynb` | Visual exploration of the cleaned dataset (charts are saved in the notebook) |

## Tech stack

Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, requests, Jupyter

## Data and running it

The raw dataset is company freight data and is **not** included in this repository. To re-run the geocoding step, set your own API key:

```bash
export LOCATIONIQ_API_KEY="your-key"
```

## Status

Cleaning and exploratory analysis are complete. Modelling notebooks will be added.
