# E-Commerce Sales Data Analysis Project

##  Project Overview

This project performs an in-depth analysis of sales data from an e-commerce platform specializing in clothing items (Pants, Dresses, and Sweaters). The dataset spans from May 1st, 2016, to April 1st, 2019. The goal is to extract actionable insights, understand key sales drivers, and build predictive models to optimize commercial performance and strategic decision-making.

##  Objectives

- **Optimize Commercial Performance:** Uncover trends, patterns, and opportunities to increase sales and improve operational efficiency.
- **Forecast Future Sales:** Predict future sales volumes based on historical data for better inventory and resource planning.
- **Identify Key Influencing Factors:** Determine the elements (product features, market conditions, promotions) that significantly impact sales results.
- **Support Strategic Decision-Making:** Provide accurate analyses to guide pricing, marketing, and inventory management strategies.
- **Increase Profitability:** Develop optimal sales strategies by focusing on the most profitable products or customer segments.
- **Achieve Business Targets:** Monitor and adjust sales strategies to ensure the achievement of company goals.

##  Dataset

The dataset contains sales data for three product categories, each with the following features:

- **S (Sales):** Total sales in billions of Yuan.
- **X4 (Page Views):** Total number of pages viewed on the platform in billions.
- **X8 (Additional Purchases):** Number of times additional items were added to carts before checkout, in tens of millions.
- **X9 (Customer Group Index):** An aggregate index reflecting customer group behavior or segmentation, in hundreds of thousands.
- **X10 (Transaction Index):** A global index of transactions on the platform, in millions.

**Sheets:** `Pants sales`, `Dress sales`, `Sweater sales`

##  Analysis Process

The project follows a structured data analysis pipeline:

1.  **Data Collection:** Loaded and examined the Excel file containing three separate sheets for each product category.
2.  **Sampling:** Applied Simple Random Sampling (60%) on each category to create manageable yet representative subsets for analysis.
3.  **Duplicate Removal:** Checked for and removed duplicate entries to ensure data integrity.
4.  **Missing Value Handling:** Implemented mean imputation to address any missing numerical values, preserving the dataset's size and distribution.
5.  **Outlier Detection:** Used Interquartile Range (IQR) method and boxplot visualization to identify and analyze outliers.
6.  **Feature Scaling:** Standardized all numerical features (mean=0, std=1) to ensure equal weighting in subsequent analyses.
7.  **Feature-Sales Relationship:** Visualized the relationship between each feature and sales using scatter plots and trend lines.
8.  **Correlation Analysis:** Created heatmaps to quantify the correlation between all variables and sales.
9.  **Hypothesis Testing:** Conducted Student's t-tests to compare mean sales between each pair of product categories (Pants vs. Dresses, Pants vs. Sweaters, Dresses vs. Sweaters).
10. **Dimensionality Reduction:** Performed Principal Component Analysis (PCA) to reduce data complexity while retaining essential variance.
11. **Sales Prediction:** Built Linear Regression models for each product category to predict future sales, evaluated using Root Mean Squared Error (RMSE).

##  Tech Stack

- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy
##  How to Run

1.  **Clone the repository** (or download the files).
    ```bash
    git clone <your-repo-url>
    cd E-Commerce-Sales-Analysis
    ```

2.  **Set up a Python environment** and install the required libraries.
    ```bash
    pip install -r requirements.txt
    # Alternatively, install key libraries manually:
    # pip install pandas numpy matplotlib seaborn scikit-learn scipy openpyxl
    ```

3.  **Place the Dataset:** Ensure the `DataSetVentes.xlsx` file is in the root directory of the project.

4.  **Open and Run the Jupyter Notebook:**
    ```bash
    jupyter notebook Sales_Analysis_Notebook.ipynb
    ```
    Execute the cells sequentially to reproduce the entire analysis.

##  Key Findings

- **Strong Correlations:** Variables X8 (Additional Purchases) and X10 (Transaction Index) showed very strong positive correlations with sales across all product categories.
- **Significant Sales Differences:** Hypothesis testing (t-tests) confirmed that the mean sales between Pants, Dresses, and Sweaters are statistically significantly different from each other.
- **Effective Dimensionality Reduction:** PCA revealed that 3 principal components were sufficient to explain nearly 100% of the variance in the data for all categories.
- **Accurate Predictions:** Linear Regression models achieved good predictive accuracy with low RMSE scores, providing a reliable tool for sales forecasting.
