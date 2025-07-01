# Customer Monthly Charges Analysis

This project performs exploratory and statistical analysis on a customer transaction dataset with a focus on **Monthly Charges**, **churn behavior**, and **distributional insights**.

---

## Table of Contents

- [Dataset Overview](#dataset-overview)
- [Summary Statistics](#summary-statistics)
- [Skewness & Kurtosis](#skewness--kurtosis)
- [Visualizations](#visualizations)
  - [Monthly Charges Distribution](#monthly-charges-distribution)
  - [Churn Rate by Charge Bucket](#churn-rate-by-charge-bucket)
  - [Sampling Distribution of the Mean](#sampling-distribution-of-the-mean)
  - [Correlation Heatmap](#correlation-heatmap)
  - [Boxplot + Histogram](#boxplot--histogram)
  - [Charge Bucket Distribution](#charge-bucket-distribution)
- [Outlier Detection](#outlier-detection)
- [Probability & Hypothesis Testing](#probability--hypothesis-testing)
- [Technologies Used](#technologies-used)
- [Outputs](#outputs)
- [Author](#author)

---

## Dataset Overview

The dataset contains customer information such as:

- `MonthlyCharges`: Monthly billing amount
- `Churned`: Whether the customer churned (Yes or No)
- `TenureMonths`: Number of months the customer has stayed

---

## Summary Statistics

### Central Tendency:
- **Mean**: 72.91  
- **Median**: 71.18  
- **Mode**: 65.32  

### Dispersion:
- **Standard Deviation**: 31.83  
- **Variance**: 1012.99  
- **Range**: 323.82  
- **IQR**: 25.96  

---

## Skewness & Kurtosis

- Skewness indicates if the distribution is symmetric.
- Kurtosis tells us how peaked the distribution is.

**Skewness**:
- CustomerID: `0.000000`
- MonthlyCharges: `4.140285`
- TenureMonths: `0.065376`

**Kurtosis**:
- CustomerID: `-1.200000`
- MonthlyCharges: `28.574482`
- TenureMonths: `-1.303213`

---

## Visualizations

### Monthly Charges Distribution
*Plot saved in `plots/monthly_charges_distribution.png`*

### Churn Rate by Charge Bucket
*Plot saved in `plots/churn_rate_by_bucket.png`*

### Sampling Distribution of the Mean
*Plot saved in `plots/sampling_distribution.png`*

### Correlation Heatmap

**Correlation matrix:**

|                | MonthlyCharges | TenureMonths |
|----------------|----------------|---------------|
| MonthlyCharges | 1.000000       | 0.028376      |
| TenureMonths   | 0.028376       | 1.000000      |

*Heatmap saved in `plots/correlation_heatmap.png`*

### Boxplot + Histogram
*Plot saved in `plots/boxplot_histogram.png`*

### Charge Bucket Distribution
*Plot saved in `plots/charge_bucket_distribution.png`*

---

## Outlier Detection

### IQR Method - Outliers Detected:
CustomerID MonthlyCharges TenureMonths Churned ChargeBucket
25 177.33 66 Yes Very High
44 191.94 53 No Very High
86 179.88 62 Yes Very High
126 341.43 46 No Very High
145 225.60 23 Yes Very High

**Total outliers (IQR method)**: 5

### Z-Score Method:
**Total outliers (Z-score method)**: 5

---

## Probability & Hypothesis Testing

### Churn Probability:
- **P(Churned = Yes)**: 0.30

### T-Test: Churned vs Non-Churned Customers
- **T-Statistic**: 0.69  
- **P-Value**: 0.4917  
- **Conclusion**: No significant difference in charges between churned and not churned customers.

---

## Technologies Used

- Python 3.10+
- Pandas
- Seaborn
- Matplotlib
- SciPy

---

## Outputs

All visualizations are saved in the `plots/` folder.

---



