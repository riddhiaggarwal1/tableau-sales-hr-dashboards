# Interactive Sales & HR Analytics Dashboards (Tableau)

Two interactive Tableau dashboards built for my MSc Data Analytics (BSBI, Berlin).

## HR Workforce Insights Dashboard (`hr_attrition_dashboard.twb`)

![HR Workforce Insights Dashboard](images/hr_dashboard.png)

**Question:** where is the company losing employees, and what does the workforce look like?

**Data:** *IBM HR Analytics Employee Attrition & Performance* (Kaggle), 1,470 employees

**What I built:** 8 linked views covering attrition by department, job role, gender and overtime, plus age, gender and income breakdowns. They're combined into one dashboard for HR leaders.

**Custom metric: attrition rate by job role.** I wrote this calculated field myself:
```
SUM(IF [Attrition] = "Yes" THEN 1 ELSE 0 END) / COUNT([EmployeeNumber])
```

![Attrition rate by job role](images/hr_attrition_rate_by_role.png)

**Key findings**
- **Sales Representatives have by far the highest attrition: about 40%** leave, compared with 2.5% of Research Directors and 4.9% of Managers.
- Laboratory Technicians (24%) and HR staff (23%) are the next most at-risk roles.
- By department, Sales (20.6%) and Human Resources (19.0%) lose more people than R&D (13.8%).
- The roles with the highest attrition are also the lowest paid. Sales Representatives earn the least on average (≈£2.6k/month), while Managers earn ≈£17.2k/month and Research Directors ≈£16.0k/month.
- The workforce is 60% male. Attrition is slightly higher for men (17.0%) than for women (14.8%).

**Recommendation:** focus retention efforts on entry-level, lower-paid roles (Sales Representatives and Lab Technicians), for example through pay reviews and clearer progression paths.

## Sales Performance Dashboard (`sales_dashboard.twb`)
- Four views: revenue vs target, product Pareto chart, deal-size breakdown, and regions & customers
- **Data:** *Sample Sales Data* (Kaggle)

## How to open
Open the `.twb` files in Tableau Desktop or Tableau Public. When Tableau asks for the data, point it to the Kaggle dataset (the data files are not included).

**Tools:** Tableau, calculated fields, KPI design, data storytelling
