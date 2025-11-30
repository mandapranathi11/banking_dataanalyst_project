
# Banking Customer Risk Analysis  
**Self-Learning Project | Python, MySQL, Power BI, DAX, Power Query**

A complete end-to-end analytics project focused on identifying high-risk customer segments in a banking dataset. The workflow includes data extraction, cleaning, transformation, risk scoring, SQL modeling, and building an interactive Power BI dashboard.

---

## Project Overview  
This project demonstrates how banks analyze customer behavior to detect potential credit risk.  
Using **Python**, **MySQL**, and **Power BI**, the pipeline includes:

- Data cleaning & transformation  
- Risk score calculation  
- SQL-based storage & analysis  
- KPI creation using DAX  
- Interactive dashboard for portfolio risk management  

---

## Tech Stack  
| Tool | Purpose |
|------|---------|
| **Python** | Data cleaning, analysis, visualizations |
| **MySQL** | Database, SQL analytics |
| **Power BI** | Dashboard + visualization |
| **Power Query** | Data transformation |
| **DAX** | Custom KPIs & measures |

---

## Project Structure  
```

├── data/                 → Raw & cleaned datasets
├── notebooks/            → Python scripts & analysis
├── sql/                  → MySQL schema & queries
├── powerbi/              → Power BI (.pbix) file
├── images/               → Dashboard screenshots
└── README.md

````

---

## Key Features  

### 1. Data Cleaning & Preparation (Python)  
- Handled missing values & outliers  
- Created calculated fields:  
  - Debt-to-Income Ratio  
  - Payment Behavior Flags  
  - Risk Score  
- Encoded categories & normalized variables  

---

### 2. MySQL Data Modeling  
- Customer, loan, and account tables created  
- Segmentation queries and risk filtering  

Example SQL:
```sql
SELECT customer_id, risk_score, loan_amount
FROM customer_risk
WHERE risk_score > 0.7;
````

---

### 3. Risk Analysis with Python

* Identified patterns in income, credit score & loan behavior
* Correlation heatmaps for key variables
* Calculated a rule-based risk score

---

### 4. Power BI Dashboard

**Pages included:**

* **Risk Overview** → KPIs, high-risk % split
* **Customer Segmentation** → Age, income, loan type analysis
* **Loan Performance** → Delinquency, default probability

Example DAX:

```DAX
High Risk Customers =
CALCULATE(COUNTROWS(Customer),
Customer[RiskScore] > 0.7)

Average Risk Score =
AVERAGE(Customer[RiskScore])
```

---

## Insights Generated

* Strong correlation between **loan amount** and **risk score**
* Age group **21–30** showed highest risk concentration
* High-income groups showed lower default probability
* Debt-to-Income ratio and past payment behavior were major risk drivers

---

## What I Learned

* End-to-end data workflow
* SQL data modeling and analytics
* Power BI DAX measures & advanced visuals
* Understanding of credit risk indicators
* Improving storytelling through dashboards

```
