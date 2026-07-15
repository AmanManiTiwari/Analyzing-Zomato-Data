<div align="center">

# 🍽️ Zomato Data Analysis

**Exploratory data analysis of restaurant listings on Zomato — uncovering patterns in ratings, votes, online ordering, and pricing using Python.**

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?logo=plotly&logoColor=white)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)](https://seaborn.pydata.org/)
[![Open In Colab](https://img.shields.io/badge/Open%20in-Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/github/AmanManiTiwari/Analyzing-Zomato-Data/blob/main/Analyzing_Zomato_Data.ipynb)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](#license)

[Overview](#-overview) •
[Dataset](#-dataset) •
[Analysis Workflow](#-analysis-workflow) •
[Key Insights](#-key-insights) •
[Getting Started](#-getting-started) •
[Project Structure](#-project-structure)

</div>

---

## 📖 Overview

This project is an **exploratory data analysis (EDA)** of a Zomato restaurant listings dataset, aimed at understanding what drives restaurant popularity and customer preference. Using **Pandas** for data wrangling and **Matplotlib** / **Seaborn** for visualization, the analysis explores restaurant categories, customer ratings, vote counts, online ordering behavior, and pricing trends.

The entire analysis lives in a single, well-commented Jupyter notebook and is also runnable directly in **Google Colab** — no local setup required.

---

## 🗂 Dataset

The dataset (`Zomato data .csv`) contains **148 restaurant records** with the following fields:

| Column | Description |
|---|---|
| `name` | Name of the restaurant |
| `online_order` | Whether the restaurant accepts online orders (`Yes` / `No`) |
| `book_table` | Whether the restaurant offers table booking (`Yes` / `No`) |
| `rate` | Customer rating out of 5 (originally formatted as `"4.1/5"`) |
| `votes` | Number of votes the restaurant has received |
| `approx_cost(for two people)` | Approximate cost for two people (in ₹) |
| `listed_in(type)` | Restaurant category (e.g. Buffet, Dining, Cafe) |

---

## 🔬 Analysis Workflow

The notebook (`Analyzing_Zomato_Data.ipynb`) follows a standard EDA pipeline:

1. **Data Loading** — Load the CSV into a Pandas DataFrame.
2. **Data Cleaning**
   - Parse the `rate` column from a string like `"4.1/5"` into a usable numeric value.
   - Confirm the dataset has no missing/NULL values (`df.info()`).
3. **Univariate Analysis**
   - Count plot of restaurant types (`listed_in(type)`).
   - Line plot of total votes grouped by restaurant type.
   - Lookup of the restaurant(s) with the maximum votes.
   - Count plot of online-ordering availability.
   - Histogram of the ratings distribution.
   - Count plot of approximate cost for two people.
4. **Bivariate / Relationship Analysis**
   - **Box plot** comparing ratings between restaurants that do and don't accept online orders.
   - **Heatmap** of a pivot table cross-tabulating restaurant type against online-ordering preference.

---

## 💡 Key Insights

- 🍽️ **Dining is king** — the majority of listed restaurants fall into the "Dining" category, and dining restaurants also receive the highest total votes.
- ⭐ **Most ratings cluster between 3.5 and 4** out of 5.
- 📦 **Online ordering is the minority behavior** — most restaurants in the dataset do not accept online orders, but those that do tend to have **higher ratings** than offline-only restaurants.
- ☕ **Ordering channel varies by category** — dining restaurants lean heavily offline, while cafes see proportionally more online orders.
- 💰 **₹300 for two is the sweet spot** — the most common approximate cost for two people across listed restaurants.

---

## 🚀 Getting Started

### Option A — Run in Google Colab (no setup)

Click the badge below to open and run the notebook directly in your browser:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AmanManiTiwari/Analyzing-Zomato-Data/blob/main/Analyzing_Zomato_Data.ipynb)

### Option B — Run locally

**Prerequisites:** Python 3.8+ and Jupyter.

```bash
# 1. Clone the repository
git clone https://github.com/AmanManiTiwari/Analyzing-Zomato-Data.git
cd Analyzing-Zomato-Data

# 2. (Recommended) create and activate a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 4. Launch the notebook
jupyter notebook Analyzing_Zomato_Data.ipynb
```

Run the cells top to bottom — the notebook reads `Zomato data .csv` from the repository root, so keep the notebook and CSV in the same folder.

---

## 🗂 Project Structure

```
Analyzing-Zomato-Data/
├── Analyzing_Zomato_Data.ipynb   # Main analysis notebook (EDA + visualizations)
├── Zomato data .csv              # Source dataset (148 restaurant records)
└── README.md
```

---

## 🛠 Tools & Technologies

| Purpose | Library |
|---|---|
| Data manipulation | [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/) |
| Visualization | [Matplotlib](https://matplotlib.org/), [Seaborn](https://seaborn.pydata.org/) |
| Environment | Jupyter Notebook / Google Colab |

---

## 🔭 Possible Extensions

- [ ] Correlation analysis between `votes`, `rate`, and `approx_cost(for two people)`
- [ ] Text analysis on restaurant names or categories for naming trends
- [ ] Interactive dashboard (e.g. with Plotly Dash or Streamlit) for exploring the dataset
- [ ] Expand the dataset beyond 148 records for more statistically robust conclusions

---

## 📄 License

This project currently has no explicit license file. Consider adding an [MIT License](https://choosealicense.com/licenses/mit/) to clarify usage rights for contributors and users.

---

## 👤 Author

**Aman Mani Tiwari**
GitHub: [@AmanManiTiwari](https://github.com/AmanManiTiwari)

<div align="center">

If you found this analysis useful, consider giving it a ⭐!

</div>
