# Loyalty Program Data Analysis

## Project Description
This project analyzes data from an airline loyalty program, exploring the relationship between different variables such as education level, salary, loyalty card type, flight distance, and points accumulation. Data cleaning, exploration, and visualization techniques have been applied to extract key insights.

## Technologies Used
This project was developed in **Python** using the following libraries:

- **NumPy**: Numerical array manipulation and mathematical calculations.
- **Pandas**: Data analysis, cleaning, and structured data manipulation.
- **Matplotlib**: Creation of graphical visualizations.
- **Seaborn**: Statistical graph generation with an enhanced design.
- **Scikit-Learn**: Handling missing values and imputation with:
  - `SimpleImputer`
  - `IterativeImputer`
  - `KNNImputer`
- **OS**: For file and directory operations.

Additional configurations:
- **`pd.set_option('display.max_columns', None)`**: To display all columns without truncation.

## Data Exploration and Cleaning
### Data Loading
The data comes from two initial CSV files:
- `Customer Loyalty History.csv`: Contains customer loyalty information, including loyalty levels and demographic data.
- `Customer Flight Activity.csv`: Contains customer flight history, including distances traveled and points accumulated.

Both datasets were processed, cleaned, and combined to generate a consolidated file:
- `airline_loyalty_programme.csv`: Contains cleaned and structured data ready for analysis.

- Missing values and duplicates were removed.
- Column names and categorical values were normalized.
- Missing values in `salary` were imputed using **IterativeImputer**.
- Data was analyzed to detect possible inconsistencies.

## Visualizations and Analysis
Various charts were created to visualize customer distribution, booked flights, the relationship between flight distance and accumulated points, and other key aspects of the loyalty program.

## How to Reproduce the Analysis
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

