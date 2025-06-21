# Employee Attrition Analysis: Enhancing Workforce Retention

## Project Overview 📈

Employee attrition poses a significant challenge for organizations, leading to increased costs, reduced productivity, and loss of institutional knowledge. This project addresses the critical business problem of understanding and mitigating employee turnover. By analyzing historical employee data, I aimed to identify the key factors driving attrition and provide actionable insights to improve employee retention strategies, ultimately contributing to a more stable and productive workforce.

## Data Description 📊

The analysis utilized a comprehensive dataset of employee information.

* **Type:** Employee demographic, job-related, and performance data.
* **Size:** 4410 records with 21 features.
* **Source:** The dataset was provided as part of an Employee Attrition Case Study. It included features such as Age, Attrition (target variable), Business Travel, Department, Distance From Home, Education, Education Field, Employee ID, Gender, Job Level, Job Role, Marital Status, Monthly Income, Number of Companies Worked, Percent Salary Hike, Stock Option Level, Total Working Years, Training Times Last Year, Years At Company, Years Since Last Promotion, and Years With Current Manager.

## Methodology / Approach 🔬

My approach followed a structured data analysis pipeline to ensure robust insights:

1.  **Business Objective Understanding:** Clearly defined the project's scope and the core business problem of employee attrition.
2.  **Data Health Review:**
    * **Data Type Validation:** Ensured variables were correctly interpreted (e.g., converting float to integer where appropriate).
    * **Missing Value Handling:** Identified and addressed 28 null values (0.63% of the data) in `NumCompaniesWorked` and `TotalWorkingYears` by dropping the affected records due to their minimal impact on the overall dataset.
    * **Data Cleaning:** Checked for and cleaned extra spaces, special characters, and unexpected values.
    * **Duplicate Check:** Confirmed no duplicate records were present.
    * **Extended Data Dictionary (EDD) Generation:** Created a detailed data dictionary for better data understanding.
3.  **Exploratory Data Analysis (EDA):**
    * **Univariate Analysis:** Explored distributions of individual variables (both numerical and categorical) using suitable plots (e.g., pie charts, histograms).
    * **Bivariate Analysis:** Investigated relationships between variables using scatter plots for numerical data and cross-tabulations for categorical data, including a correlation heatmap to identify strong relationships.
    * **Attrition Rate Analysis:** Examined how attrition rates varied across different bins of numerical variables (e.g., salary, age) and categories of object variables (e.g., department, job role, marital status).
4.  **Key Performance Indicator (KPI) / Metric-Based Questions:** Addressed specific business questions related to attrition drivers, such as the impact of promotions, salary increments, manager relationships, and tenure.
5.  **Open-Ended Questions and Recommendations:** Synthesized findings to identify strong drivers of attrition and proposed actionable strategies for retention.

## Key Results 🎯

The analysis revealed several strong drivers of employee attrition:

* **Age and Tenure:** Younger employees (25-35 years old) and those with shorter tenure (less than 10 years total working experience, especially those with less than 2 years at the company) showed higher attrition rates. Employees who had spent less than one year at the company were particularly prone to leaving.

* **Compensation:**
    * Employees with lower monthly incomes were more prone to leave, likely seeking better compensation.
    * A strong correlation was observed: lower percentage salary hikes directly contributed to higher attrition. Those with less percentage salary hike tended to leave more than those with a higher hike.
    * **Stock Options:** Employees who were excluded from stock options or received fewer stocks as part of their compensation were most likely to leave the company. This was evident from the analysis of `Stock_Option_Level` versus attrition count.
    * **Salary vs. Peers:** Employees with salaries lower than their peers (with similar work experience) were also more likely to leave.

* **Career Progression:** Employees who did not receive promotions were significantly more likely to leave. Specifically, 325 employees who received no promotion left the company.

* **Managerial Relationships:** A notable number of employees with less than 2 years under their current manager contributed to maximum attrition, suggesting potential issues with managerial training or team dynamics.

* **Training:** Employees who spent 2 to 3 years on training often left the company shortly after, indicating a possible gap in retention strategies post-training.

* **Department/Role:** The Research & Development department, particularly Laboratory Technicians, Sales Executives, and Research Scientists, experienced the highest attrition.

* **Marital Status:** Single employees exhibited the largest proportion of leavers.

## Tools and Technologies Used 🛠️

* **Python:** For data loading, cleaning, analysis, and visualization.
* **Pandas:** For data manipulation and analysis.
* **Matplotlib & Seaborn (or similar libraries):** For data visualization (histograms, bar charts, pie charts, heatmaps).
* **Microsoft PowerPoint / PDF:** Used to present the final analysis and recommendations.

## Business Impact / Why this project is valuable 💰

This project provides invaluable insights for human resources and leadership teams to proactively address employee attrition. By understanding the core drivers, organizations can:

* **Optimize Compensation Strategies:** Implement competitive salary structures and transparent increment policies, and consider stock option inclusion to enhance employee value perception.
* **Enhance Career Development:** Develop clearer promotion paths and provide consistent opportunities for growth, especially for long-tenured employees.
* **Improve Managerial Effectiveness:** Invest in manager training programs focused on people handling, mentorship, and team management to foster better employee-manager relationships.
* **Refine Hiring Strategies:** Consider converting internships to full-time opportunities and focusing on retention of early-career employees who often leave to gain more experience.
* **Tailor Training Programs:** Ensure training investments translate into long-term employee commitment, potentially by tying advanced training to career progression opportunities, particularly for employees with more than 3 years at the company.
* **Strategic Interventions:** Implement targeted retention programs for high-risk groups identified through the analysis (e.g., specific departments, younger employees, single employees, and those with low tenure or recent manager changes).

Ultimately, by implementing these data-driven recommendations, companies can reduce turnover costs, improve employee morale, and build a more stable and engaged workforce.

## Contact Information / About Me 📧

**Devanapalli Ruthwik**
**Senior Data Analyst | Business Consultant**

**Email**: ruthwik.devanapalli@gmail.com
**LinkedIn**: <https://www.linkedin.com/in/ruthwik-devanapalli/>

This project is intended for educational, portfolio, and demonstration purposes. Attribution appreciated when used or adapted.