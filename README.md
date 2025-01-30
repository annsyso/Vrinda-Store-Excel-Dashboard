# Vrinda Store Excel Dashboard

<img width="1231" alt="image" src="https://github.com/user-attachments/assets/9b5166a6-9383-450c-9ccc-b1e24a2ba898" />


## Objective
Vrinda Store wants to create an annual sales report to understand their customers and grow their sales for the next year. The goal is to analyze data from 2022 to make predictions and inform business decisions for 2023.

## Sample Questions for Analysis
The dashboard aims to answer key business questions, including:
- Which month had the highest sales and orders?
- Who purchased more based on gender?
- What are the top states contributing to orders?
- Which channel has the greatest ROI for sales?
- What is the highest-selling category?

---

## Step-by-Step Process

### 1. Data Cleaning
- **Duplicate Raw Data:** Always keep a copy to reference in case of errors.
- **Identify and Remove Duplicates:** Ensure data integrity before proceeding.
- **Filter Columns:** Review all column categories to identify necessary cleaning steps.
- **Key Cleaning Tasks:**
  - Standardize gender values (e.g., different strings denoting gender).
  - Normalize string cases in the item column.
  - Convert `Qty` to consistent integer format.
  - Normalize case for `Ship City` values.
  
#### Example: Standardizing Gender Column
```excel
=IF(E2="W", "Women", E2)
```

#### Example: Cleaning Quantity Column
```excel
=IF(ISNUMBER(F2), F2, VALUE(F2))
```

---

### 2. Data Processing
- **Create Age Groups:** Categorize customers by age for easier analysis.
  
#### Example: Age Grouping Formula
```excel
=IF(E2>=50, "Senior", IF(E2>=30, "Adult", "Teenager"))
```

- **Isolate Month for Analysis:** Extract the month from the date column.
  
#### Example: Extracting Month Name
```excel
=TEXT(DATE(2000,H2,1),"MMM")
```

---

### 3. Data Analysis
- **Pivot Table & Charts:**
  - Create a pivot table with `Month` as rows and total sales + order count.
  - Generate a **Pivot Combo Chart**:
    - Bar chart for total sales.
    - Line chart for total order count.
- **Further Analysis:**
  - Compare sales between **men and women**.
  - Count and analyze different **order statuses**.
  - Identify **top five states** by sales volume.
  - Analyze **age & gender spending trends**.
  - Evaluate **sales performance by channel**.

---

### 4. Building the Dashboard
- **Add Pivot Charts to the Dashboard**
- **Integrate Slicers** for:
  - Month
  - Category
  - Channel
- **Connect Slicers** to all charts to allow dynamic filtering.

---

## Insights & Recommendations
### Key Findings:
- Women are the dominant buyers across all age groups.
- Adults (30-49 years) are the highest-spending customer segment.
- Amazon is the most profitable sales channel.

### Business Strategy Moving Forward:
- **Target women aged 30-49** for marketing campaigns.
- **Focus on top three states** with the highest sales.
- **Increase ad spend on Amazon** to maximize sales growth.

---

## Conclusion
The Vrinda Store Excel Dashboard provides valuable insights into customer demographics, purchase trends, and high-performing sales channels. By leveraging these findings, the store can allocate resources effectively and optimize strategies for 2023 growth.

