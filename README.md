# HR Analytics and Employee Attrition Dashboard (Power BI + MySQL)

## 📊 Overview
This project analyzes HR data to extract insights around **employee compensation**, **job satisfaction**, and **attrition trends**. It simulates the role of a **HR Analyst**, using MySQL for data transformation and Power BI for dashboarding.

---

## 🛠️ Tools & Technologies
- **MySQL Workbench** – For querying and transforming raw data
- **Power BI Desktop** – For creating interactive dashboards
- **Dataset** – [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

---

## 📁 Dataset Summary
The dataset includes employee details such as:
- Job Role, Department, Monthly Income
- Attrition (Yes/No)
- Work-Life Balance, Job Satisfaction
- Salary Hike, Years at Company, etc.

---

## 📂 Folder Structure
├── README.md ├── SQL │ └── HR_Analysis.sql ├── PowerBI │ └── HR_Attrition_Analysis.pbix ├── Images │ └── Overview_Dashboard.png │ └── Attrition_Dashboard.png


---
## 🧮 SQL Workflow

Below are a few of the SQL queries used for data preparation:

```sql
SELECT JobRole, SUM(MonthlyIncome) AS TotalCompensation
FROM hr_data
GROUP BY JobRole;
```
```sql
SELECT Department, ROUND(AVG(MonthlyIncome), 2) AS AvgIncome
FROM hr_data
GROUP BY Department;
```


```sql
SELECT Gender, COUNT(*) AS Count
FROM hr_data
GROUP BY Gender;
```
```sql

SELECT WorkLifeBalance, Attrition, COUNT(*) AS Count
FROM hr_data
GROUP BY WorkLifeBalance, Attrition; 
```

---

## 📊 Power BI Dashboard Pages

### ✅ Page 1: Employee Overview
A general snapshot of the workforce.

**Visuals Included:**
- 🧑‍🤝‍🧑 **Employees by Gender** (Donut Chart)
- 📌 **KPIs**: Total Employees, Avg Monthly Income, Avg Day Rate, Job Satisfaction
- 💰 **Average Monthly Income by Department** (Bar Chart)
- 💼 **Total Compensation by Job Role** (Bar Chart)


![ALt text](https://github.com/Uneeba-Irfan/-HR-Analytics-and-Employee-Attrition-Dashboard-Power-BI-MySQL-/blob/main/Overview.png)

### ❌ Page 2: Employee Attrition Analysis
Focuses on understanding patterns and possible causes behind employee turnover.

**Visuals Included:**
- 📉 **Attrition Distribution** (Donut Chart)
- ⚖️ **Attrition by Work-Life Balance** (Stacked Bar Chart)
- 🧑‍💼 **Attrition by Job Role** (Bar Chart)
- 📈 **Salary Hike vs Time at Company** (Scatter Plot)
- 📊 **Attrition by Age** (Histogram)
![Alt text](https://github.com/Uneeba-Irfan/-HR-Analytics-and-Employee-Attrition-Dashboard-Power-BI-MySQL-/blob/main/Attrition.png)
## 📌 Key Insights
- 💼 **Sales Executives** contribute the highest to total compensation.
- 💰 Highest average monthly income observed in **Sales** and **Human Resources** departments.
- ⚖️ Most employees rate their **Work-Life Balance** as 3 or 4, yet attrition still exists within those groups.
- 👶 **Younger employees** (ages **25–35**) show higher rates of attrition.
- 📉 Employees with **lower salary hikes** or **fewer years at the company** tend to leave more frequently.

---

## 🚀 How to Use
1. 📥 **Clone** the repository.
2. 🧮 **Run the SQL queries** from `HR_Analysis.sql` using **MySQL Workbench**.
3. 📊 **Open** the `.pbix` file in **Power BI Desktop**.
4. 🧭 Use **filters** to drill down by **Department** and **Job Role**.


