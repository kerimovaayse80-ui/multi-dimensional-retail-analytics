# Business Insights and Analytical Findings

## 1. Executive Summary

This analysis examines **99,457 retail transactions** from shopping malls in Istanbul. The objective is to understand revenue performance across product categories, shopping malls, payment methods, customer gender, and time periods.

The analysis shows that **Clothing is the largest revenue-generating category**, while **Technology has the highest average transaction value**. Mall of Istanbul generates the highest total mall revenue, while Emaar Square Mall has the highest average transaction value among the shopping malls.

Female customers account for a larger share of transactions and therefore generate higher total revenue, although the average transaction values of female and male customers are very similar.

Cash is the dominant payment method across all eight product categories. The month-over-month analysis also shows that revenue growth varies substantially between shopping malls.

These findings demonstrate that retail performance should be evaluated using multiple metrics rather than relying only on total revenue.

---

## 2. Dataset Overview

The dataset contains **99,457 transactions** and includes information about:

- Customer demographics
- Product categories
- Quantity purchased
- Unit price
- Payment method
- Transaction date
- Shopping mall

The dataset contains:

- **8 product categories**
- **10 shopping malls**
- **3 payment methods**
- **2 gender groups**

The initial data-quality analysis found **no missing values and no duplicate rows**.

A transaction-level revenue measure was created using:

`revenue = quantity × price`

This measure was then used throughout the analysis.

---

# 3. Product Category Performance

## 3.1 Total Revenue by Category

The total revenue analysis shows the following ranking:

| Category | Total Revenue |
|---|---:|
| Clothing | $113,996,791.04 |
| Shoes | $66,553,451.47 |
| Technology | $57,862,350.00 |
| Cosmetics | $6,792,862.90 |
| Toys | $3,980,426.24 |
| Food & Beverage | $849,535.05 |
| Books | $834,552.90 |
| Souvenir | $635,824.65 |

### Finding

**Clothing generated the highest total revenue**, at approximately **$114.0 million**. Shoes and Technology followed with approximately $66.6 million and $57.9 million respectively.

Clothing therefore represents the largest revenue contribution among the product categories in the dataset.

### Business Implication

Clothing is an important revenue driver and could be examined further in terms of product assortment, seasonal demand, customer segments, and shopping-mall performance.

However, total revenue should not be interpreted as profit because the dataset does not contain cost or margin information.

---

## 3.2 Average Transaction Revenue by Category

The average transaction revenue differs considerably between categories:

| Category | Average Transaction Revenue |
|---|---:|
| Technology | $11,581.74 |
| Shoes | $6,632.79 |
| Clothing | $3,305.50 |
| Cosmetics | $449.95 |
| Toys | $394.61 |
| Books | $167.55 |
| Souvenir | $127.19 |
| Food & Beverage | $57.49 |

### Finding

**Technology has the highest average transaction value**, even though Clothing has the highest total revenue.

This distinction is important:

- Clothing → highest **total revenue**
- Technology → highest **average transaction revenue**

### Business Implication

Technology transactions have a much higher average value. This suggests that Technology could be examined separately for high-value purchasing patterns, product bundles, and customer purchasing behavior.

The result also demonstrates why total revenue and average transaction value should not be treated as the same metric.

---

# 4. Shopping Mall Performance

## 4.1 Total Revenue by Shopping Mall

| Shopping Mall | Total Revenue |
|---|---:|
| Mall of Istanbul | $50,872,481.68 |
| Kanyon | $50,554,231.10 |
| Metrocity | $37,302,787.33 |
| Metropol AVM | $25,379,913.19 |
| Istinye Park | $24,618,827.68 |
| Zorlu Center | $12,901,053.82 |
| Cevahir AVM | $12,645,138.20 |
| Viaport Outlet | $12,521,339.72 |
| Emaar Square Mall | $12,406,100.29 |
| Forum Istanbul | $12,303,921.24 |

### Finding

**Mall of Istanbul generated the highest total revenue**, with approximately $50.87 million, followed closely by Kanyon at approximately $50.55 million.

### Business Implication

Total revenue provides a useful measure of overall revenue contribution, but it should be evaluated together with transaction volume and average transaction value.

---

## 4.2 Average Transaction Revenue by Shopping Mall

The average transaction values show a different pattern:

| Shopping Mall | Average Transaction Revenue |
|---|---:|
| Emaar Square Mall | $2,578.69 |
| Mall of Istanbul | $2,550.89 |
| Kanyon | $2,550.28 |
| Viaport Outlet | $2,548.10 |
| Zorlu Center | $2,542.08 |
| Cevahir AVM | $2,533.59 |
| Istinye Park | $2,517.01 |
| Metropol AVM | $2,497.78 |
| Forum Istanbul | $2,487.15 |
| Metrocity | $2,485.03 |

### Finding

**Emaar Square Mall has the highest average transaction revenue**, despite not having the highest total revenue.

### Business Implication

This difference shows that a mall can have a high total revenue because of transaction volume, while another mall can have a higher average purchase value.

For a more complete mall-performance assessment, both metrics should be considered together.

---

# 5. Revenue by Shopping Mall and Category

A shopping mall × category pivot table and heatmap were used to examine how revenue is distributed across product categories within each mall.

### Finding

The heatmap shows a consistent pattern across the shopping malls:

1. **Clothing** generates the highest revenue in each mall.
2. **Shoes** generally represents the second-largest revenue category.
3. **Technology** is also a major revenue contributor.
4. Books, Food & Beverage, and Souvenir generate substantially lower revenue.

Mall of Istanbul and Kanyon show particularly high revenue across several major categories, especially Clothing, Shoes, and Technology.

### Business Implication

The results suggest that category performance is not identical in magnitude across malls. Mall-level category analysis can therefore be useful for evaluating assortment, inventory allocation, and category-specific strategies.

---

# 6. Payment Method Analysis

## 6.1 Revenue and Transaction Distribution

The payment-method analysis compared:

- Total revenue
- Number of transactions
- Average transaction revenue
- Transaction share

Cash generated approximately **$112.83 million** in revenue and accounted for **44,447 transactions**.

Credit Card generated approximately **$88.08 million** from **34,931 transactions**.

Debit Card generated approximately **$50.60 million** from **20,079 transactions**.

### Finding

**Cash is the most frequently used payment method and generates the highest total revenue.**

However, the average transaction values are relatively close:

- Cash: approximately $2,538.58
- Credit Card: approximately $2,521.46
- Debit Card: approximately $2,519.87

### Business Implication

The higher total revenue generated by Cash is primarily associated with its larger transaction volume rather than a substantially higher average transaction value.

---

# 7. Dominant Payment Method by Category

The second bonus analysis compared total revenue generated by Cash, Credit Card, and Debit Card within every product category.

### Result

**Cash is the dominant payment method across all eight categories:**

| Category | Dominant Payment Method |
|---|---|
| Books | Cash |
| Clothing | Cash |
| Cosmetics | Cash |
| Food & Beverage | Cash |
| Shoes | Cash |
| Souvenir | Cash |
| Technology | Cash |
| Toys | Cash |

### Business Implication

The consistency of Cash dominance across categories indicates that payment behavior is relatively stable at the category level in this dataset.

Nevertheless, payment-method dominance should not be interpreted as higher customer spending per transaction because transaction volume also affects total revenue.

---

# 8. Gender-Based Revenue Analysis

## 8.1 Total Revenue

| Gender | Total Revenue | Transaction Share |
|---|---:|---:|
| Female | $150.21M | 59.81% |
| Male | $101.30M | 40.19% |

### Finding

Female customers generated higher total revenue than male customers.

This is consistent with the fact that female customers account for a larger share of transactions.

---

## 8.2 Average Transaction Revenue

The average transaction values are:

- Female: approximately **$2,525.25**
- Male: approximately **$2,534.05**

### Finding

Although female customers generate more total revenue, the average transaction values are very similar.

Therefore, the higher female total revenue should not be interpreted as substantially higher spending per transaction.

### Business Implication

Customer segmentation should consider both **transaction volume** and **transaction value**. Looking only at total revenue could hide the fact that the average purchase values are almost identical.

---

# 9. Revenue by Category and Gender

The gender × category analysis shows that female customers generate higher total revenue in every product category.

Clothing is the largest revenue category for both genders, followed by Shoes and Technology.

### Finding

The same broad category hierarchy appears for both customer groups:

**Clothing → Shoes → Technology**

while the total revenue generated by female customers is higher across each category.

### Business Implication

The results support analyzing category performance together with customer segments rather than looking at gender or category in isolation.

---

# 10. Yearly Revenue Trend

Revenue was aggregated by year and category for 2021, 2022, and 2023.

### Finding

Revenue was relatively stable across most categories between 2021 and 2022.

Clothing remained the largest revenue-generating category in both years, followed by Shoes and Technology.

Several categories, including Shoes and Technology, showed growth from 2021 to 2022, while Clothing experienced a slight decline.

### Important Data Limitation

**2023 is a partial year in the dataset.**

Therefore, the lower 2023 revenue values should not be interpreted as an annual decline. A complete-year comparison would require data covering the full 2023 calendar year.

---

# 11. Month-over-Month Revenue Growth

For the first bonus analysis, monthly revenue was calculated for each shopping mall.

The previous month's revenue was obtained using `shift(1)`, and MoM growth was calculated as:

`MoM Growth = ((Current Month Revenue - Previous Month Revenue) / Previous Month Revenue) × 100`

The average MoM growth by shopping mall was:

| Shopping Mall | Average MoM Growth |
|---|---:|
| Emaar Square Mall | +6.12% |
| Zorlu Center | +3.51% |
| Viaport Outlet | +2.79% |
| Forum Istanbul | +2.15% |
| Cevahir AVM | +2.08% |
| Metrocity | +1.59% |
| Metropol AVM | +1.48% |
| Istinye Park | +0.80% |
| Kanyon | +0.30% |
| Mall of Istanbul | -0.15% |

### Finding

Average monthly revenue growth varies across shopping malls. Emaar Square Mall has the highest average MoM growth in the analyzed period, while Mall of Istanbul has a slightly negative average.

### Important Data Limitation

The March 2023 period is incomplete in the dataset. Comparing a partial March with a complete February can create artificially large negative MoM values.

For this reason, incomplete March 2023 data was excluded when calculating the average MoM growth by shopping mall.

This is an important example of why **data completeness must be considered before interpreting time-series metrics**.

---

# 12. Cross-Analysis: Key Patterns

Several patterns become clear when the different analyses are considered together.

### Pattern 1 — Revenue concentration

Clothing, Shoes, and Technology account for the majority of revenue compared with the remaining categories.

### Pattern 2 — Total revenue vs. transaction value

The category with the highest total revenue is not the category with the highest average transaction value.

Clothing leads total revenue, while Technology leads average transaction value.

### Pattern 3 — Customer volume vs. spending per transaction

Female customers generate more total revenue because they account for more transactions, while male and female average transaction values are very similar.

### Pattern 4 — Payment volume vs. payment value

Cash generates the highest total revenue because it is used more frequently. Average transaction values across payment methods are relatively similar.

### Pattern 5 — Mall performance requires multiple metrics

Mall of Istanbul has the highest total revenue, while Emaar Square Mall has the highest average transaction value.

These differences show that different performance metrics can produce different perspectives on the same business.

---

# 13. Business Recommendations

Based on the descriptive findings, several areas could be investigated further:

### 13.1 Focus on high-revenue categories

Clothing, Shoes, and Technology represent the strongest revenue-generating categories. Further analysis could examine their seasonal patterns, customer segments, and mall-level performance.

### 13.2 Investigate high-value transactions

Technology has the highest average transaction value. Additional analysis could identify whether this is driven by quantity, unit price, specific malls, or customer segments.

### 13.3 Use customer volume and transaction value together

Gender and payment-method analysis shows that total revenue can be strongly influenced by transaction volume. Future segmentation should therefore include both transaction count and average transaction value.

### 13.4 Compare malls using multiple KPIs

Total revenue, transaction volume, average transaction value, and MoM growth should be analyzed together when evaluating shopping mall performance.

### 13.5 Investigate payment behavior

Cash is dominant across all categories. Future analysis could investigate whether payment preferences vary by mall, gender, age group, or transaction value.

---

# 14. Limitations

The analysis has several limitations:

1. **Revenue is not profit.** Cost, margin, and operating-expense information is not available.
2. **2023 is a partial year**, so it cannot be directly compared with complete years.
3. **March 2023 is incomplete**, which affects monthly comparisons.
4. The dataset provides transaction-level information but does not provide detailed product-level identifiers.
5. Observed relationships are descriptive and do not establish causal relationships.
6. The analysis is based only on the variables available in the dataset.

---

# 15. Conclusion

The Istanbul shopping dataset provides several useful insights into retail revenue patterns.

**Clothing is the largest revenue-generating category**, while **Technology has the highest average transaction value**. At the shopping-mall level, **Mall of Istanbul has the highest total revenue**, while **Emaar Square Mall has the highest average transaction value**.

Female customers generate higher total revenue because they account for a larger share of transactions, while average transaction values between genders remain very similar.

Cash is the dominant payment method across all eight categories and also has the highest transaction volume.

The MoM analysis demonstrates that revenue changes from month to month and that performance varies between shopping malls. At the same time, the incomplete 2023 data highlights the importance of checking data coverage before drawing conclusions from time-series analysis.

Overall, the project demonstrates how combining **category, customer, payment, mall, and time-based analysis** can provide a more complete understanding of retail performance.
