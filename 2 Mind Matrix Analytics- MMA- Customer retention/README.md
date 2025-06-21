# Customer Retention Analysis for a Financial Services Company

## 📌 Project Overview

This project addresses a common and critical business problem in the financial services industry: customer retention and churn prevention. Retaining existing customers is significantly more cost-effective than acquiring new ones, and even small improvements in retention can lead to substantial revenue growth.

The primary goal of this analysis was to understand customer behavior patterns, identify key factors influencing customer activity or inactivity (churn), and provide data-driven recommendations to help ABC Bank retain its valuable customer base. The analysis aimed to uncover which variables are significant in predicting customer duration and how well these variables describe customer tenure and activity.

## 📊 Data Description

The dataset used for this analysis contains anonymized information about customers of a financial services company, sourced from their internal CRM system. It includes comprehensive details such as:

* **Demographic Attributes:** Age, gender, and customer segment (e.g., College, Individual, VIP).
* **Financial Indicators:** Gross income, number of credit cards, and number of loans.
* **Behavioral Data:** Customer activity status recorded at two distinct time points (separated by 6 months).
* **Relationship Duration:** The total length of the customer's relationship with the company in days.

**Key Details:**

* **Size:** Approximately 54,000 initial records.
* **Format:** CSV.
* **Source:** Internal CRM system (anonymized for this case study).

### Data Health & Quality

A thorough data health review was conducted, ensuring the reliability of the dataset. Key findings and actions included:

* All variables were read into Python with appropriate data types (Integer, Float, Object).
* No missing values were identified across any variables.
* Outliers were identified in numerical features such as 'age' (ranging from 2 to 112) and 'gross_income' (ranging from $2,336 to $7,089,412). These were carefully analyzed and handled to prevent skewing results.
* Data cleaning was performed to eliminate extra spaces and address any unexpected values. Categorical values like 'Yes/No' were standardized to '1/0' for consistent analysis.
* Duplicate records were identified and removed, resulting in a clean dataset of approximately 52,800 unique customer records. An Extended Data Dictionary (EDD) was generated to comment on data quality and define each variable clearly.

## 🔍 Methodology / Approach

This project followed a comprehensive, end-to-end analytical approach, aligning with best practices in data science and business analytics:

1.  **Business Objective Understanding:** Gained a clear understanding of the client's problem (customer churn) and translated it into specific analytical questions.
2.  **Data Health Review:** Performed an in-depth assessment of data quality, including checks for variable types, missing values, outliers, and data cleanliness. Corrective steps, such as duplicate removal and data standardization, were implemented.
3.  **Feature Engineering:** Created a new, more intuitive feature, `duration_years`, by converting customer duration from days into years.
4.  **Exploratory Data Analysis (EDA):**
    * **Univariate Analysis:** Explored the distributions of individual variables using suitable plots (e.g., bar plots for categorical variables like 'gender' and 'customer_segment'; histograms for numerical variables like 'age' and 'gross_income') to understand their characteristics.
    * **Bi-variate Analysis:** Examined relationships between pairs of variables, utilizing scatter plots for numerical variables and cross-tabulations for categorical variables to uncover initial patterns.
5.  **Key Performance Indicator (KPI) / Metric Analysis:** Addressed specific, pin-pointed business questions, including:
    * Analyzing the percentage of active customers before and after a 6-month period.
    * Categorizing and counting customers into four key types: those who remained active, remained inactive, became inactive, or became active.
    * Comparing key metrics (average gross income, age, duration, number of credit cards, number of loans) across these four customer types, as well as across different gender groups and customer segments (College, Individual, VIP).
    * Calculating the percentage of customers in each segment that fell into the four activity change categories.
6.  **Open-ended Business Questions & Hypothesis Testing:** Tackled more qualitative business questions, requiring deeper analysis and hypothesis testing:
    * Investigated which customer segments (College, Individual, VIP) are expected to remain active or inactive in the future.
    * Assessed which customer segments are more prone to becoming inactive.
    * Determined which male/female customer groups exhibit more stable or volatile activity levels.
    * Statistically evaluated the impact of Income, Age, and Duration on customer activity/inactivity using relevant tests (e.g., T-tests). Specifically, a T-test was performed to assess the relationship between `duration_years` and `alltime_active_inactive` status.
7.  **Insights and Recommendations:** Synthesized findings into clear, actionable insights and formulated strategic recommendations for customer retention.

## 📈 Key Results

* **Data Integrity:** The dataset was robust and clean, with no missing values, allowing for reliable analysis. Outliers in age and gross_income were identified and managed appropriately.
* **Customer Activity Dynamics:** Detailed counts and percentages for customers who remained active/inactive or changed their status provided a clear picture of customer churn and retention rates.
* **Gender vs. Activity Stability:** While a slight numerical difference in activity variation was observed between female (0.25) and male (0.24) customers, this difference was not statistically significant, suggesting similar stability across genders.
* **Customer Segment Activity Predictions (Future Outlook):**
    * **Active Customers:** VIP customers are most likely to remain active (17.9%).
    * **Inactive Customers:** Individuals are most likely to remain inactive (97.4%).
    * **Becoming Inactive:** Individuals are most likely to become inactive (97.4%).
* **Stability/Volatility by Gender:**
    * **Stability:** Male customers showed slightly less variation (0.24) in activity status compared to female customers (0.25), suggesting marginally more stability, though not statistically significant.
    * **Volatility:** Female customers showed slightly more variation (0.25) in activity status compared to male customers (0.24), implying marginally more volatility, but again, not statistically significant.
* **Limited Impact of Core Demographics on Activity:** Statistical analysis (T-tests) revealed that gross_income and age did not have a statistically significant direct impact on customer activity status. This implies that other, potentially uncaptured, factors might be stronger drivers of churn.
* **Duration and Activity Status:**
    * The average duration for active customers was approximately 9.06 years, while for inactive customers, it was approximately 7.20 years.
    * A T-test comparing `duration_years` between 'active' and 'inactive' customers yielded a T-statistic of 37.95 and a P-value of 0.0. Since the P-value (0.0) is less than the significance level of 0.05, we reject the null hypothesis. However, the interpretation here is critical: **this statistically significant difference indicates there *is* a relationship between duration and activity status, specifically that active customers, on average, have longer durations.** The previous conclusion "Therefore there is no relation between duration and activity status" and "As the p-value is zero there is no significant impact of duration on the customer activity" is inaccurate given the very small p-value, which suggests a strong statistical difference. A very low p-value implies that the observed difference in duration between active and inactive customers is highly unlikely to have occurred by chance. Thus, duration *does* have a statistically significant impact, and active customers tend to have been customers for a longer time.
* **Income and Loan Behavior:** Customers with a gross income of less than $287,000 showed a higher propensity for holding loans, indicating a specific demographic for targeted loan product offerings.
* **Untapped Credit Card Market:** A significant opportunity was identified as over 90% of the customer base (more than 50,000 out of ~52,800 records) did not possess a credit card, highlighting a large segment for new credit card promotions and product launches.

## 🛠️ Tools and Technologies Used

* **Python:**
    * `Pandas` for efficient data manipulation and cleaning.
    * `NumPy` for numerical operations.
    * `Matplotlib` and `Seaborn` for static data visualization.
    * `Plotly` for interactive and dynamic plots.
    * `SciPy` for advanced statistical analysis.
* **Jupyter Notebook:** The primary environment for conducting the end-to-end analysis, documenting code, and presenting findings.
* **Microsoft Excel:** Utilized for initial data inspection, quick metric calculations, and data dictionary generation.
* **Microsoft PowerPoint:** Used for developing the final business presentation, summarizing insights, and providing strategic recommendations to the client.

## ▶️ How to Use / Run the Project

To explore the analysis and replicate the results:

1.  **Clone the repository:** `git clone [Your Repository URL]`
2.  **Navigate to the project directory:** `cd [Project Directory]`
3.  **Install required Python packages:**
    ```bash
    pip install pandas numpy matplotlib seaborn plotly scipy
    ```
4.  **Open the main notebook:** `Exploratory Data Analysis -Customer Retention Dataset.ipynb`
5.  **Run the notebook cells in order:** This includes all steps from data import and cleaning to EDA, statistical analysis, and visualization.

All detailed code, analytical steps, visualizations, and commentary are embedded directly within the Jupyter Notebook cells.

## 💼 Business Impact / Why This Project is Valuable

This analysis delivers actionable insights crucial for improving customer retention strategies in the financial services sector, translating data into tangible business value:

* **Enhanced Customer Understanding:** Provides the bank with a deeper, data-backed understanding of its customer base by segmenting customers and analyzing their behavior patterns.
* **Targeted Retention Strategies:** Enables the design of more effective and personalized retention campaigns for different customer segments, particularly identifying those with low product engagement or specific financial behaviors (e.g., loan holders with lower income). Specific strategies include:
    * Targeting customers based on segments, age groups, and income levels.
    * Initiating better loan offerings for customers with incomes less than $287,000.
* **Product Development & Cross-Selling Opportunities:** The low credit card ownership rates reveal a significant, untapped market opportunity for launching new credit card products or intensifying promotional efforts to increase adoption among existing customers, driving new revenue streams.
    * This includes placing more strategies to attract the use of the bank's products for customers with incomes greater than $287,000, who currently purchase fewer products.
* **Data-Driven Decision Making:** Empowers the bank to make informed strategic decisions across product development, marketing, and customer support functions, leading to improved customer lifetime value and reduced churn.
* **Scalability:** The established analytical framework is robust and adaptable, allowing it to be easily re-applied to future datasets or different customer cohorts for continuous monitoring and optimization of retention efforts.

**Conclusion:** While some features in the current dataset did not show a direct statistically significant relationship with customer activity status (e.g., income and age), `duration_years` *does* have a statistically significant relationship, with active customers having demonstrably longer tenures. This suggests a need for more comprehensive data or advanced ML models for more robust predictions and recommendations, leveraging duration as a key indicator.

## 📬 Contact Information / About Me

**Ruthwik Devanapalli**
Senior Data Analyst | Business Consultant

📧 ruthwik.devanapalli@gmail.com

## 📝 License

This project is intended for educational, portfolio, and demonstration purposes. Attribution appreciated when used or adapted.