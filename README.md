# Loyalty Program Data Analysis

This project is the individual evaluation for **Module 3 of the Adalab Data Analyst bootcamp**. The main objective is to conduct a comprehensive data analysis of a customer loyalty program using two original datasets:

- `df_flights.csv`: Contains information about customer flights.
- `df_loyalty.csv`: Contains information about customers and their participation in the loyalty program.

After cleaning and processing these datasets, we generated a unified dataset:

- `airline_loyalty_programme.csv`: Consolidates customer and flight information, ready for final analysis.

To achieve this, we followed a structured process that includes initial exploration, handling of missing values, and visualization.

---

## Project Structure

1. **Exploratory Data Analysis (EDA)**
   - Loaded the datasets into `pandas` and analyzed their structure (`.info()`, `.head()`, `.columns()`, `.nunique()`).
   - Normalized column names (lowercase and without spaces) for easier data handling.
   - Examined unique values in key columns to identify patterns and potential typographical errors.
   - Identified and managed duplicates in `df_flights`, opting for aggregation via `groupby().agg()` instead of direct removal.

2. **Data Cleaning**
   - Verified the consistency of categorical data and applied normalization (`str.strip().str.lower()`).
   - Reviewed data types and performed necessary conversions for optimization.

3. **Handling Missing Values**
   - Detected missing values in `df_loyalty`, particularly in `salary`, `cancellation_year`, and `cancellation_month`.
   - Imputed `salary` using `IterativeImputer`, after converting `education` and `postal_code` to numeric values to include them in the imputation process.
   - For `cancellation_year` and `cancellation_month`, after analyzing their distribution, we determined that missing values corresponded to **active customers**, so we filled them accordingly.

4. **Visualization and Analysis**
   - Created graphical analyses to answer key questions regarding flight distribution, point accumulation, customer geographic distribution, salary trends by education level, and segmentation by loyalty card type, marital status, and gender.
   - These insights help understand customer behavior and suggest improvements for the loyalty program.
   - **Important:** The loyalty program is exclusively for **residents of Canada**.

---

## Tools Used

This project was developed in **Python** using the following libraries:

- **NumPy**: Numerical array manipulation and mathematical calculations.
- **Pandas**: Data analysis, cleaning, and structured data manipulation.
- **Matplotlib**: Graphical visualization creation.
- **Seaborn**: Statistical graph generation with an enhanced design.
- **Scikit-Learn**: Handling missing values and imputation with:
  - `SimpleImputer`
  - `IterativeImputer`
  - `KNNImputer`
- **OS**: File and directory operations.
- IPython.display: Displaying images and Markdown content within Jupyter Notebooks.


### Additional Configurations

To improve the data analysis experience, we included the following configurations:

```python
pd.set_option('display.max_columns', None)  # Display all columns without truncation
```

Additionally, to prevent `FutureWarning` messages from cluttering the console without affecting code execution, we applied the following setting:

```python
import warnings
warnings.filterwarnings("ignore", category=FutureWarning)
```

To restore default warning settings:

```python
warnings.filterwarnings("default")
```

This keeps the workflow clean while retaining critical alerts.

---

## How to Reproduce the Analysis

To run this analysis on your own environment, follow these steps:

1. Clone this repository:

```bash
git clone https://github.com/your_username/your_repository.git
```

2. Install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Open the **Jupyter Notebook** and execute the code step by step.


---
 **Thanks for checking out this project!** 

 _Elena_

