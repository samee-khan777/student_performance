# 🎓 Student Performance Dashboard — Power BI Project

An interactive **Power BI Dashboard** designed to analyze student performance across multiple academic and demographic factors.  
This dashboard converts raw student scores into meaningful insights by exploring exam performance, parental education impact, test preparation outcomes, and gender/race-based score patterns.

The goal of this project is to provide a clear understanding of student learning trends and identify key areas that influence academic success.

---

## 🖼️ Dashboard Preview

![Dashboard Preview](./students%20dashboard.png)
![Dashboard Preview 2](./student%20dashboard.png)

---

## 🧠 Key Features

- Overall performance KPIs such as **Average Score**, **Average Math Score**, **Pass Rate**, and **Total Students**
- Score comparison by **test preparation course** (completed vs none)
- Performance analysis by **race/ethnicity**, **gender**, and **parental education level**
- Student categorization into **High**, **Medium**, and **Low** performance groups
- Stylish, colorful theme with interactive slicers for **gender**, **race/ethnicity**, and **test preparation**

---

## 🛠️ Tools Used

- **Power BI** (data modeling, visualization, DAX)
- **Power Query** (data cleaning and transformation)
- **CSV Dataset** (Students Performance dataset)
- **Custom theme + background design**

---

## 📊 Data Highlights

- Dataset includes student scores from **Math**, **Reading**, and **Writing**
- Additional demographic data:
  - Gender  
  - Race/ethnicity  
  - Parental level of education  
  - Lunch type  
  - Test preparation status  
- Columns cleaned + new calculated fields created (Average Score, Performance Category)

---

## 🧮 Key DAX Measures

```DAX
Total Students = COUNTROWS('StudentsPerformance')

Avg Math Score = AVERAGE('StudentsPerformance'[math score])
Avg Reading Score = AVERAGE('StudentsPerformance'[reading score])
Avg Writing Score = AVERAGE('StudentsPerformance'[writing score])

Average Score = 
([math score] + [reading score] + [writing score]) / 3

Pass Rate (Math) =
VAR Passed = CALCULATE(COUNTROWS('StudentsPerformance'), 'StudentsPerformance'[math score] >= 40)
RETURN DIVIDE(Passed, [Total Students], 0)

Top Performers =
CALCULATE(
    COUNTROWS('StudentsPerformance'),
    'StudentsPerformance'[Average Score] >= 85
)
```

---

## 📄 About

This project demonstrates strong skills in:

- **Data cleaning & preprocessing**
- **DAX calculations**
- **Dashboard UI/UX design**
- **Insight extraction**
- **Visualization storytelling**

It serves as an excellent portfolio project for Data Analyst / BI Analyst roles.

---

👤 **Created by [samee khan ](https://github.com/samee-khan777)**
