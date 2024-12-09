# Predicting Estonian apartment rent prices based on KV.ee listings

## Sebastian Mais, Caroline Markov, Rainer Talvik

### Motivation & Goal

The real estate market in Estonia, particularly in cities like Tallinn and Tartu, has seen significant growth and fluctuation in recent years. With the increasing demand for rental properties, both landlords and tenants face challenges in determining fair rental prices. The project aims to analyse and model long-term apartment rental listings from the Estonian real estate sale and rental site [KV.ee](https://www.kv.ee/).

Our goal is to create a predictive model with an RSME (Root Mean Square Error) of 50€ to be within ±15% of most rental listings.

### Repository

The repository contains the following files (in alphabetical order):
* `B7_report.pdf` - a report stating our business and data mining goals, data mining progress and goals and the plan for the project.
* `README.md` - the file you're reading right now.
* `cleaned_data.csv` - a data file created after the cleanup done in `kv-data-cleanup.ipynb`.
* `corr_heatmap.pdf` and `corr_heatmap.png` - a feature correlation heatmap image which we used in our initial project poster, but then replaced.
* `importance.pdf` and `importance.png` - an image showing the ten most important features used by the final Gradient Boosting model, Figure 2 in the poster. This file didn't want to export properly, which is why the PDF version is cut off.
* `kv-data-cleanup.ipynb` - the main Jupyter Notebook file where almost all of the data cleanup, postprocessing and feature engineering happened.
* `kv-rent-data-16-11-2024.csv` - data scraped from the [KV.ee](https://www.kv.ee/) website on November 16th 2024 using the [Web Scraper extension](https://webscraper.io/); the initial dataset for our model.
* `kv_map.png` - an illustrative image of listings in Tallinn from [KV.ee's map search](https://www.kv.ee/#/search/map?deal_type=2), Figure 1 in the poster.
* `modelling.ipynb` - the Jupyter notebook where final touches (filling in NaN values, correlation checking) were done and where models were tested and tuned.
* `modelling_improved_visualisations.ipynb` - a copy of `modelling.ipynb`, which contains visualisations that were better matched with our poster's colour scheme and spacing.
* `performance_comparison.pdf` and `performance_comparison.png` - an image showing the performance of various models on our dataset.
* `web-scraper-sitemap.txt` - a plaintext copy of the [Web Scraper](https://webscraper.io/) sitemap configuration used to gather all listings from [KV.ee](https://www.kv.ee/). 

### Replication

The code can be run on your computer by following these steps:
1. Clone the repository or download it as a ZIP and extract it to your path of choice;
2. Install an environment in which to use Jupyter Notebook (VSCode, Anaconda, Jupyter Notebook etc.) alongside the dependencies required;
3. Installing the following Python packages in your environment using your environment's equivalent of
```shell
pip install matplotlib pandas numpy scikit-learn seaborn scikit-optimize
```
4. Run the codes in `kv-data-cleanup.ipynb` and `modelling.ipynb` for the respective sub-tasks.

The data could be gathered again by copying the text in `web-scraper-sitemap.txt` into the [Web Scraper Extension's](https://webscraper.io/) "Import sitemap" tab.

The poster visualisations can be recreated using `modelling_improved_visualisations.ipynb`. 
