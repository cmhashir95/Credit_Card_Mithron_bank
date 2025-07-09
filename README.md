# 📊 Mitron Bank Credit Card Pilot Project – Data Analytics Dashboard

This project is part of the **Codebasics Resume Project Challenge**. The objective was to perform a comprehensive analysis of customer spending behavior using a sample dataset provided by Mitron Bank, to support the launch of a new line of credit cards. The outcome is a data-driven Power BI dashboard with actionable insights aimed at top-level management and product strategy teams.

---

## 🏦 About the Client – Mitron Bank

Mitron Bank is a legacy financial institution based in Hyderabad. Looking to diversify their product line and compete in the growing credit market, the bank sought support in understanding their customers before rolling out credit cards. They partnered with **AtliQ Data Services** for a pilot analysis of 4,000 customers across five cities.

---

## 👨‍💼 Role

* Analyzing the provided sample data
* Creating relevant KPIs and visualizations
* Designing an executive-level dashboard
* Presenting insights to help drive strategic decisions for credit card offerings

---

## 🧠 Key Business Questions

* Which customer segments are most likely to adopt credit cards?
* What is the average monthly spend by city, gender, and occupation?
* How well are customers utilizing their income?
* How does credit card spending compare to other payment types?

---

## 📈 Measures Created

The following DAX measures were developed in Power BI to support data exploration and insight generation:

### 1. **Average Spend per Month**

```DAX
Avg Spend per month = 
AVERAGEX(
    VALUES('fact_spends'[Month]),
    CALCULATE('dim_customers'[Total Spend])
)
```

This measure calculates the average total spend per customer across available months.

---

### 2. **Total Spend**

```DAX
Total Spend = 
SUM(fact_spends[Spend])
```

This provides the overall spending amount across all transactions.

---

### 3. **Income Utilisation %**

```DAX
Income_utilisation_% = 
AVERAGEX(
    VALUES(dim_customers[Customer ID]),
    DIVIDE(
        [Avg Spend per month],
        [Avg_Income_per_month]
    )
)
```

This custom metric helps assess how much of a customer's income is being used on average. Useful for evaluating creditworthiness and targeting the right segments.

---

### 4. **Credit Card Spend**

```DAX
Credit card Spend = 
CALCULATE(
    SUM(fact_spends[Spend]),
    'fact_spends'[Payment Type] = "Credit Card"
)
```

Identifies total spend through credit card transactions to help evaluate credit card usage behavior.

---

## 📊 Dashboard Features

* **Demographic Visuals:** Age, gender, marital status, and occupation distribution.
* **Geographic Analysis:** Spending patterns across cities.
* **Income Utilization Heatmap:** Cross-segmented by occupation and age.
* **Credit Card Trends:** Comparison of credit card vs non-credit card spending.
* **Custom Tooltips & Interactivity:** Drilldowns and slicers for dynamic analysis.

---

## 🧩 Tools Used

* Power BI
* DAX
* MySQL

---

## 🔍 Insights & Recommendations

* Highest credit card usage was observed in the **25–34 age group**, primarily among **salaried IT employees**.
* Cities like **Mumbai** and **Bangalore** show higher average monthly spending.
* **Income Utilization** is highest among freelancers and IT professionals, indicating strong potential for tailored credit products.
* **Married males** in salaried roles are key high-spend customers.

---

## 📽️ Presentation & Delivery

This dashboard was presented to the strategy team at Mitron Bank with a 15-minute concise walkthrough of:

* Analytical approach
* Key takeaways
* Strategic suggestions

---

## 🔗 Useful Links

* [Codebasics Resume Challenge]
* [LinkedIn Project Post](#) 

---

## 📌 Author

**Mohammed Hashir**
Data Enthusisast | Power BI | Ex-Spotfire Developer
🔗 [LinkedIn](https://www.linkedin.com/in/mohammed-hashir-22432b22/) 
📧 [Email]
    (mohammedhashir2605@gmail.com)

---
