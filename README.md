# Customer Personality Analysis
This project aims to perform customer personality analysis using data from a marketing campaign. It includes various data preprocessing steps, clustering using Gaussian Mixture Models, visualization, and association rule mining. The goal is to gain insights into customer behavior and identify patterns and associations among different customer segments.

## Table of Contents
- Installation
- Usage
- Data
- Preprocessing
- Clustering
- Visualization
- Segmentation
- Association Rule Mining

## Installation
To run the code in this project, you need to have the following dependencies installed:

- numpy
- pandas
- matplotlib
- seaborn
- plotly
- scikit-learn
- mlxtend
- dataprep

You can install these dependencies by running the following command:

```python
pip install numpy pandas matplotlib seaborn plotly scikit-learn mlxtend dataprep
```

## Usage

1. Clone the repository or download the code files.
2. Make sure you have the required dependencies installed (see the Installation section).
3. Run the Python script or execute the code in your preferred Python environment.

## Data
The project uses a dataset from a marketing campaign. The data is loaded from the following URL: [marketing_campaign.csv.](https://raw.githubusercontent.com/amankharwal/Website-data/master/marketing_campaign.csv)

The dataset contains information about customers, including their age, education, marital status, income, spending on various product categories, seniority, and other attributes.

## Preprocessing
The code includes several preprocessing steps to clean and transform the data before analysis. Some of the preprocessing steps performed are:

- Calculation of age based on the "Year_Birth" column.
- Creation of the "Spending" column by summing up spending on different product categories.
- Conversion of the "Dt_Customer" column to the "Seniority" column, representing the number of months as a customer.
- Renaming and re-categorizing columns related to marital status, education, and children.
- Removal of missing values and outliers in the "Income" column.
- Standardization and normalization of selected features.

## Clustering
The code performs clustering using Gaussian Mixture Models (GMM) on the standardized and normalized data. It uses the "Income," "Seniority," and "Spending" features for clustering. The number of clusters is set to 4, and the clustering results are assigned labels representing different customer segments.

## Visualization
The code includes visualization using Matplotlib and Plotly. It generates a 3D scatter plot to visualize the clusters based on the "Income," "Seniority," and "Spending" features. Each cluster is represented by a different color.

## Segmentation
The code creates additional segments based on customer attributes such as age, income, and seniority. The segments include:

- Age groups: Young, Adult, Mature, Senior.
- Income groups: Low income, Low to medium income, Medium to high income, High income.
- Seniority groups: New customers, Discovering customers, Experienced customers, Old customers.
- Consumption segments for different product categories: Wines, Fruits, Meat, Fish, Sweets, and Gold.

## Association Rule Mining
The code performs association rule mining using the Apriori algorithm from the MLxtend library. It creates binary indicators for each product category and uses them to mine association rules. The rules are generated based on a minimum support threshold and a maximum length limit. The confidence and lift metrics are used to evaluate the strength of the rules.

The results of association rule mining are shown for a specific product category and segment. It provides insights into the associations between products that are frequently purchased together by customers in the selected segment.

Please note that this README file only provides an overview of the project and its main components. For a detailed understanding of the code, it is recommended to review the actual Python script
