# Predicting Estonian apartment rent prices based on KV.ee listings

## Sebastian Mais, Caroline Markov, Rainer Talvik

### Motivation & Goal

The real estate market in Estonia, particularly in cities like Tallinn and Tartu, has seen significant growth and fluctuation in recent years. With the increasing demand for rental properties, both landlords and tenants face challenges in determining fair rental prices. The project aims to analyse  and model long-term apartment rental listings from the Estonian real estate sale and rental site [KV.ee](https://www.kv.ee/).

Our goal is to create a predictive model with an RSME (Root Mean Square Error) of 50€ to be within ±15% of most rental listings.

### Repository

The repository contains the following files in alphabetical order:
* `B7_report.pdf` - a report stating our business and data mining goals, data mining progress and goals and the plan for the project.
* `README.md` - the file you're reading right now.
* `cleaned_data.csv` - a data file created after the cleanup done in `kv-data-cleanup.ipynb`.
* `corr_heatmap.png` - a feature correlation heatmap image which we used in our project poster.
* `kv-data-cleanup.ipynb` - the main Jupyter Notebook file where almost all of the data cleanup, postprocessing and feature engineering happened.
* `kv-rent-data-16-11-2024.csv` - data scraped from the [KV.ee](https://www.kv.ee/) website on November 16th 2024 using the [Web Scraper extension](https://webscraper.io/); the initial dataset for our model.
* `kv_map.png` - an illustrative image of listings in Tallinn from [KV.ee's map search](https://www.kv.ee/#/search/map?deal_type=2).
* `modelling.ipynb` - the Jupyter notebook where final touches (filling in NaN values, correlation checking) were done and where models were tested and tuned.
* `web-scraper-sitemap.txt` - the [Web Scraper](https://webscraper.io/) sitemap used to gather all listings from [KV.ee](https://www.kv.ee/). 

### Replication

The code can be run on your computer by installing an environment in which to use Jupyter Notebook (VSCode, Anaconda, Jupyter Notebook etc.) alongside the dependencies required, by installing the required Python packages in your environment using your environment's equivalent of
```python
pip install matplotlib pandas numpy scikit-learn seaborn scikit-optimize
```
and by running the codes in `kv-data-cleanup.ipynb` and `modelling.ipynb` for the respective sub-tasks.
