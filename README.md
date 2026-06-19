# House-Price-Data-Analysis-Visualization
## Overview
This repository contains an exploratory data analysis (EDA) project focused on housing price data using Python.  
The notebook demonstrates how to clean missing values, analyze distributions, detect outliers, explore correlations, and visualize important relationships between housing features and sale prices.

The project is designed for learning and practicing:
- Data cleaning
- Exploratory Data Analysis (EDA)
- Statistical visualization
- Feature relationship analysis
- Basic preprocessing for Machine Learning workflows

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Structure

```bash
├── lesson7.ipynb          # Main analysis notebook
├── README.md              # Project documentation
└── dataset/               # Dataset folder (optional)
```

---

## Dataset

The notebook uses a housing price dataset:

```python
df_clean_HOUSE_PRICE.csv
```

The dataset includes:
- Numerical features (price, area, year built, etc.)
- Categorical features (neighborhood, quality, style, etc.)
- Target variable:
  - `SalePrice`

---

## Features Covered

### 1. Data Inspection
The notebook explores:
- Dataset shape
- Column information
- Data types
- Statistical summaries

```python
df.info()
df.describe()
```

---

### 2. Missing Value Handling

Categorical columns are filled with `"None"` while numerical columns use median imputation.

```python
df[cat_all] = df[cat_all].fillna('None')
df[num] = df[num].fillna(df[num].median())
```

---

### 3. Distribution Analysis

The project visualizes the distribution of housing prices using:
- Histogram
- KDE Plot
- Boxplot

These visualizations help identify:
- Skewness
- Density
- Outliers

---

### 4. Log Transformation

A logarithmic transformation is applied to normalize the target variable:

```python
df['SalePrice_log'] = np.log1p(df['SalePrice'])
```

This improves:
- Distribution symmetry
- Model performance potential
- Outlier handling

---

### 5. Correlation Analysis

The notebook identifies features with the strongest correlation to `SalePrice`.

Visualization includes:
- Correlation matrix
- Heatmap of top correlated features

---

### 6. Advanced Visualizations

The project includes:
- Boxplots
- Violin plots
- Scatter plots
- Regression plots
- Neighborhood-based price comparisons

These help uncover:
- Feature importance
- Trends
- Relationships between variables

---

## Example Visualizations

### Distribution Analysis
- Histogram + KDE
- Boxplot for outlier detection

### Relationship Analysis
- `OverallQual` vs `SalePrice`
- `GrLivArea` vs `SalePrice`

### Correlation Heatmap
Top numerical features correlated with housing prices.

---

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```bash
lesson7.ipynb
```

---

## Learning Objectives

This project is useful for students and beginners learning:
- Data analysis with Pandas
- Data visualization with Seaborn
- EDA workflow
- Missing value treatment
- Correlation analysis
- Feature engineering basics

---

## Future Improvements

Possible next steps:
- Feature encoding
- Machine Learning model training
- Feature scaling
- Cross-validation
- Hyperparameter tuning
- Model deployment

---

## Author

**Zaxro Madrimova**  
Computer Science & Software Engineering Student  
INHA University in Tashkent

---

## License

This project is intended for educational and learning purposes.

