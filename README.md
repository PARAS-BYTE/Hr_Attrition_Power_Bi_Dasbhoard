<img width="936" height="537" alt="image" src="https://github.com/user-attachments/assets/e5bd735c-72f8-4ad9-8b33-8b73b364530e" />
# HR Attrition Dashboard – Power BI Project

## 📌 Project Overview

This project presents an interactive **HR Analytics Dashboard** developed using **Microsoft Power BI Desktop** to analyze employee attrition trends and generate actionable HR insights.

The dashboard helps organizations understand:

* Employee attrition patterns
* Department-wise turnover
* Impact of overtime on attrition
* Job roles with high employee exits
* Gender and age-based attrition analysis

The project uses the **IBM HR Analytics Employee Attrition Dataset** containing 1,470 employee records and 35 attributes. 

---

# 📊 Dashboard Features

* KPI Cards for:

  * Total Employees
  * Attrition Count
  * Attrition Rate
  * Average Income

* Interactive Visualizations:

  * Attrition by Gender
  * Attrition by Department
  * Attrition by Job Role
  * Attrition by OverTime
  * Attrition by Age Group

* Dynamic Filters/Slicers:

  * Gender
  * Department
  * Job Role

---

# 🛠 Tools & Technologies Used

* Microsoft Power BI Desktop
* Power Query Editor
* DAX (Data Analysis Expressions)
* CSV Dataset
* Power BI Service

---

# 📂 Dataset Information

* **Dataset Name:** WA_Fn-UseC_-HR-Employee-Attrition.csv
* **Source:** IBM HR Analytics Dataset
* **Records:** 1,470 Employees
* **Columns:** 35 Attributes

### Important Features

* Age
* Attrition
* Gender
* Department
* JobRole
* MonthlyIncome
* OverTime
* YearsAtCompany

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed using **Power Query Editor**:

* Verified column data types
* Removed constant columns:

  * EmployeeCount
  * Over18
  * StandardHours
* Checked for missing values
* Renamed columns for readability
* Created calculated fields for analysis

---

# 📈 DAX Measures Used

```DAX
Total Employees = COUNT('HR-Attrition'[EmployeeNumber])

Attrition Count = CALCULATE(
    COUNT('HR-Attrition'[EmployeeNumber]),
    'HR-Attrition'[Attrition] = "Yes"
)

Attrition Rate = DIVIDE([Attrition Count], [Total Employees], 0)

Average Income = AVERAGE('HR-Attrition'[MonthlyIncome])

Active Employees = [Total Employees] - [Attrition Count]
```

---

# 🔍 Key Insights

* Overall Attrition Rate: **16%**
* Total Attrition Count: **237 Employees**
* Research & Development department has the highest attrition
* Employees working overtime show significantly higher attrition
* Laboratory Technicians and Sales Executives are the most affected job roles
* Highest attrition observed in the age group **28–32 years**

---

# 🚀 Deployment

The dashboard was published using **Microsoft Power BI Service** for online access and sharing.

### Live Dashboard Link

[Open Power BI Dashboard](https://app.powerbi.com/groups/me/reports/0be1d346-5784-4c2d-ae2b-11943236498d?ctid=f5322753-3586-4ca6-bedd-618429df573c&pbi_source=linkShare&utm_source=chatgpt.com)

---

# 📷 Dashboard Preview

(Add dashboard screenshots here)

---

# 📚 Future Improvements

* Predict employee attrition using Machine Learning
* Real-time HRMS integration
* Mobile responsive dashboard
* Drill-through analysis pages
* Employee sentiment analysis

---

# 📖 References

* IBM HR Analytics Employee Attrition Dataset
* Microsoft Power BI Documentation
* DAX Documentation

---


