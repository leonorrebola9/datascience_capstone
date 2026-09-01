# Winning the Space Race with Data Science 🚀

Capstone project for the **IBM Data Science Professional Certificate**. This project predicts whether the first stage of a SpaceX Falcon 9 rocket will land successfully, using historical launch data collected via the SpaceX API and web scraping, then explored, visualized, and modeled with machine learning.

🎓 **[IBM Data Science Professional Certificate — Verify Credential](https://coursera.org/share/e5781d26affd738ba104da589ba19ed3)**

## Project Overview

SpaceX advertises Falcon 9 launches at $62 million, compared to $165+ million from other providers — largely because SpaceX reuses the rocket's first stage. If we can predict whether the first stage will land successfully, we can estimate the cost of a launch, which is valuable information for any company bidding against SpaceX.

This project walks through a full data science pipeline: data collection, data wrangling, exploratory data analysis (visualization, SQL, and interactive analytics), and predictive modeling with classification algorithms.

## Repository Structure

```
datascience_capstone/
├── README.md
├── presentation/
│   ├── ds-capstone-presentation.pdf
│   ├── ds-capstone-presentation.ppt
│   ├── ds-capstone-presentation_feedback.pdf
├── images
├── notebooks/
│   ├── jupyter-labs-spacex-data-collection-api-v2.ipynb
│   ├── jupyter-labs-webscraping.ipynb
│   ├── labs-jupyter-spacex-data-wrangling-v2.ipynb
│   ├── jupyter-labs-eda-dataviz-v2.ipynb
│   ├── jupyter-labs-eda-sql-coursera_sqllite.ipynb
│   ├── lab-jupyter-launch-site-location-v2.ipynb
│   └── SpaceX-Machine-Learning-Prediction-Part-5-v1.ipynb
└── dashboard/
    └── spacex-dash-app.py
```

| File | Description |
|---|---|
| `notebooks/jupyter-labs-spacex-data-collection-api-v2.ipynb` | Collects launch data from the SpaceX REST API |
| `notebooks/jupyter-labs-webscraping.ipynb` | Scrapes historical Falcon 9/Heavy launch records from Wikipedia |
| `notebooks/labs-jupyter-spacex-data-wrangling-v2.ipynb` | Cleans the data and builds the binary landing outcome label (`Class`) |
| `notebooks/jupyter-labs-eda-dataviz-v2.ipynb` | Exploratory data analysis with Matplotlib/Seaborn |
| `notebooks/jupyter-labs-eda-sql-coursera_sqllite.ipynb` | Exploratory data analysis with SQL |
| `notebooks/lab-jupyter-launch-site-location-v2.ipynb` | Interactive launch site map built with Folium |
| `notebooks/SpaceX-Machine-Learning-Prediction-Part-5-v1.ipynb` | Builds, tunes, and evaluates classification models |
| `dashboard/spacex-dash-app.py` | Interactive dashboard built with Plotly Dash |
| `ds-capstone-presentation.pdf` | Final summary presentation of the project |

## Methodology

1. **Data Collection** — Combined two sources: the [SpaceX REST API](https://github.com/r-spacex/SpaceX-API) (structured launch/rocket/payload/core data) and Wikipedia (historical launch records via web scraping with BeautifulSoup).
2. **Data Wrangling** — Handled missing values, engineered a binary `Class` label (1 = successful landing, 0 = unsuccessful) from the landing outcome column.
3. **Exploratory Data Analysis** — Visualized relationships between flight number, payload mass, launch site, and orbit type using Matplotlib/Seaborn, and queried the dataset directly with SQL.
4. **Interactive Visual Analytics** — Built an interactive map with Folium (launch site locations, color-coded outcomes, distance to coastline) and a Plotly Dash dashboard (site/payload filters).
5. **Predictive Analysis** — Trained and tuned four classification models (Logistic Regression, SVM, Decision Tree, KNN) with `GridSearchCV` and compared their cross-validated accuracy.

## Key Results

- Landing success rate improved substantially over time, from early failures (2010–2013) to a stable ~85%+ success rate in recent years, tracking SpaceX's booster evolution (v1.0 → v1.1 → FT → Block 5).
- Launch site, orbit type, and payload mass all show a measurable relationship with landing outcome.
- The **Decision Tree Classifier** was the best-performing model, with **87.5% cross-validated accuracy**, outperforming Logistic Regression, SVM, and KNN.

## Tools & Libraries

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Plotly` · `Dash` · `Folium` · `BeautifulSoup` · `Requests` · `SQLite` · `scikit-learn`

## Author

Leonor Rebola
