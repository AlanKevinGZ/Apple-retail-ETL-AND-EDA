# Apple Retail Sales ETL & Exploratory Data Analysis

## Overview

This project focuses on building an ETL pipeline and performing Exploratory Data Analysis (EDA) on a synthetic Apple Retail Sales dataset from Kaggle.

The dataset contains retail sales transactions, product information, store data, categories, and warranty claims across multiple Apple retail locations worldwide.

The goal of the project was to:
- Clean and transform raw retail data
- Build a unified analytical dataset
- Explore business performance metrics
- Analyze sales behavior and warranty claims
- Generate business insights from transactional data

---

## Dataset

Dataset used:

- Sales
- Products
- Categories
- Stores
- Warranty claims

Source:
Apple Retail Sales Dataset (Kaggle)

---

## ETL Process

### 1. Data Extraction
Loaded the following CSV files:
- `sales.csv`
- `products.csv`
- `category.csv`
- `stores.csv`
- `warranty.csv`

---

### 2. Data Transformation

Performed multiple joins to create a unified analytical dataset.

Main transformations included:

- Merging sales with products
- Adding product categories
- Adding store information
- Aggregating warranty claims by sale
- Creating derived business metrics

Example derived metrics:
- `revenue = quantity * price`
- `n_claims = number of warranty claims`

---

### 3. Final Dataset

The final dataset contains:
- Sales information
- Product details
- Store details
- Revenue metrics
- Warranty claim metrics

Main columns:
- sale_id
- sale_date
- store_name
- product_name
- category_name
- quantity
- price
- revenue
- n_claims

---

# Exploratory Data Analysis (EDA)

## Data Validation

Validated:
- Missing values
- Duplicates
- Invalid values
- Revenue distribution

Findings:
- No missing values
- No negative prices or quantities
- Revenue distribution showed positive/right skewness

---

## Revenue Analysis

Analyzed:
- Total revenue
- Revenue distribution
- Average transaction value (ticket)

Key observation:
- Revenue distribution is highly right-skewed, indicating that a small number of transactions generate a significant portion of total revenue.

---

## Store Performance Analysis

Analyzed:
- Top stores by revenue
- Average ticket per store
- Revenue concentration

### Key Findings

- One store showed strong dominance in total revenue.
- `Apple Dubai Mall` appeared both:
  - among the top revenue stores
  - and among the stores with the highest average ticket value.

This indicates:
- High sales volume
- High-value transactions

In contrast:
- Stores like `Apple Yas Mall` and `Apple Union Square`
  had high ticket averages but lower overall revenue.

---

## Warranty Analysis

Integrated warranty claims into the analytical dataset to support product quality analysis.

Metrics analyzed:
- Number of claims
- Claims by product/store/category

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook / Kaggle Notebook

---

## Skills Demonstrated

- ETL pipeline development
- Data cleaning
- Data transformation
- Relational joins
- Aggregation logic
- Feature engineering
- Exploratory Data Analysis
- Business-oriented data interpretation

---

## Project Structure

```bash
├── data/
├── notebooks/
├── README.md
└── outputs/
