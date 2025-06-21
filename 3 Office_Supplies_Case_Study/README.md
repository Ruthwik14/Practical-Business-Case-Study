# Office Supplies Sales Analysis: Driving Business Growth with Data Insights 🚀

## Project Overview 📌

This project presents a comprehensive analysis of historical sales data for a global office supplies retailer. The core objective was to extract actionable business insights to inform strategic decision-making across key departments, including marketing, product development, and operations. By leveraging a data-driven approach, this project aimed to optimize crucial business metrics such as sales performance, profitability, and overall customer experience.

## Data Description 📊

The analysis was conducted using an extensive proprietary dataset comprising thousands of sales records spanning a four-year period.

* **Key Features:** The dataset includes granular information on customer demographics, order specifics (e.g., Order ID, Order Date, Ship Date, Ship Mode), sales performance metrics (Sales, Profit, Discount, Shipping Cost), and product attributes (Category, Sub-Category, Product Name, Product ID). Geographic details like City, State, Country, Region, and Market, alongside Order Priority, are also included.
* **Size:** Approximately 51,000 sales records, encompassing over 3,700 unique products sold across 165 countries and 5 major markets.
* **Source:** Internal retail sales and shipping data provided by the firm.

## Methodology / Approach 🧠

A structured analytical pipeline was rigorously followed to ensure robust and reliable insights:

### 1. Data Cleaning & Preprocessing ✨

* **Data Type Validation:** Verified and corrected data types (e.g., dates, numerical values) in Python, implementing necessary transformations.
* **Missing Value Handling:** Identified and addressed missing values. Notably, Postal Code had 80.51% missing entries and was dropped as it was not central to the analysis.
* **Outlier Detection:** Employed visualizations such as box plots to identify and understand outliers in numerical variables (e.g., Sales, Profit, Discount) to prevent skewed analytical results.
* **Data Consistency:** Performed cleaning for inconsistencies like extra spaces, special characters, or unexpected values, and converted categorical data (e.g., 'Yes'/'No') to numerical formats where appropriate.
* **Duplicate Records:** Identified and managed any duplicate entries within the dataset.

### 2. Feature Engineering 🧩

* Derived new features including Order Month, Order Year, Order Quarter, and Delivery Time (calculated as the difference between Ship Date and Order Date) to facilitate time-series analysis and efficiency assessments.

### 3. Extended Data Dictionary (EDD) 📚

* Generated a comprehensive data dictionary to document data quality observations and define all variables.

### 4. Exploratory Data Analysis (EDA) 🔍

* Conducted detailed univariate analyses for both categorical (object) and numerical variables. Utilized appropriate plots (e.g., bar charts, histograms) and provided insightful commentary on observed distributions.
* Performed bi-variate analyses, including scatter plots to reveal relationships between numerical variables and cross-tabulations for categorical variables, to uncover patterns and guide problem-solving.

### 5. Key Performance Indicator (KPI) Analysis 📈

* **Granularity Assessment:** Determined the count of unique values for Customer ID, Order ID, and Product ID to establish the granularity of the input data.
* **Customer Behavior:** Analyzed the total unique customers over four years and quantified the percentage of single orders versus repeat orders.
* **Order Distribution:** Illustrated the distribution of customers based on their order frequency (e.g., 1 order, 2 orders) to identify key customer engagement patterns.
* **Product Sub-Category Summary:** Prepared a summary for each product sub-category, reporting Total Sales, Total Quantity, Average % Discount, Total Profit, and Total Shipping Cost, to derive actionable insights.
* **Market Performance:** Identified the largest market for the firm and determined the top 3 products by sales within each market.
* **Shipping Efficiency:** Computed and analyzed the frequency distribution of Delivery Time to understand the duration of order shipping and identify delivery patterns.
* **Sales Relationships:** Explored the correlation between Sales and other numerical variables using suitable plots, employing binning for discrete numerical variables to observe relationships effectively.
* **Average/Median Sales by Category:** Calculated average and median sales for various categories of relevant object variables to understand their impact on sales performance.

### 6. Open-ended Questions and Recommendations ✅

* **Record Interpretation:** Clarified the meaning of each record in the dataset and the specific information it captures.
* **Customer Order Volume Trends:** Identified customers who consistently maintained or increased their order volumes over the 4-year period, providing summaries and strategic recommendations for retention programs.
* **Profitability Metric:** Calculated profit return (e.g., profit per dollar of sales) to pinpoint products yielding the highest profit returns over the years.
* **Discount Effectiveness:** Analyzed the impact of discounts on furniture sales and profits using appropriate charts, offering strategic recommendations for optimizing discount policies.
* **Market/Segment Performance:** Assessed the performance of various markets, customer segments, and product categories in terms of sales and profits over time.
* **Product Portfolio Evolution:** Examined shifts in the firm's product portfolio contribution to total yearly sales, highlighting products with improving or declining performance.
* **Delivery Time Analysis:** Evaluated average delivery times for different product categories and countries, considering distinct shipping modes, and proposed actionable improvements.
* **Cyclic Demand Patterns:** Investigated seasonal demand patterns (over 48 months) for specific products (Phones, Chairs, Furnishings, Art) to inform optimized production strategies.

## Key Results and Insights 💡

* **Customer Loyalty:** A significant 65% of customers were repeat buyers, underscoring a strong existing customer base. Granular insights into order distribution by customer provide a foundation for tailored loyalty programs.
* **Market Leadership:** The USCA market emerged as the top performer, especially within the Technology category, with Machines identified as a leading product. This highlights regional strengths and opportunities for targeted expansion.
* **Profitability vs. Discounts:** Furniture products, despite substantial discounts, often exhibited negative profits. This strongly suggests the current discount strategy for furniture is inefficient and requires immediate revision. In contrast, Phones consistently generated significant profits even without aggressive discounting, indicating that alternative incentives (e.g., value-added gifts) might be more effective than price reductions for high-margin items.
* **Shipping Efficiency:** Analysis revealed notable variations in delivery times across different product categories and countries, pinpointing critical areas for supply chain optimization.
* **Product Demand Patterns:** Specific products like Phones, Chairs, Furnishings, and Art demonstrated clear cyclic demand patterns throughout the year. This insight enables proactive inventory management and precise production planning to align with seasonal peaks and troughs.
* **Customer Growth Drivers:** Identification of customers who consistently increased their order volumes provides a clear path for developing highly effective loyalty programs and personalized engagement strategies.

## Tools and Technologies Used 🛠️

* **Programming Language:** Python 🐍
* **Libraries:**
    * `pandas`: For robust data manipulation and analysis.
    * `numpy`: For efficient numerical operations.
    * `matplotlib.pyplot`, `seaborn`: For creating static, publication-quality data visualizations.
    * `plotly.express`, `plotly.graph_objects`, `plotly.figure_factory`: For generating interactive and dynamic visualizations.
* **Development Environment:** Jupyter Notebook 📒
* **Reporting:** Excel (for metric validation and summaries) and PowerPoint (for final presentation of insights) 📊.

## How to Use / Run the Project 🏃‍♀️

To explore this project and reproduce the analysis:

1.  **Clone the Repository:** (If hosted on GitHub) Begin by cloning the project repository to your local machine.
2.  **Prerequisites:** Ensure you have Python installed. All required libraries can be installed via pip:
    ```bash
    pip install pandas numpy matplotlib seaborn plotly
    ```
3.  **Data Location:** Place the `Office Supplies Orders Case Study Data.xlsx` file (or its CSV equivalent) in the same directory as the Jupyter Notebook (`Office_Supplies_Case_Study.ipynb`).
4.  **Run the Notebook:** Open `Office_Supplies_Case_Study.ipynb` in your preferred Jupyter environment (e.g., Jupyter Lab, VS Code with Jupyter extension) and execute the cells sequentially to observe the data cleaning, analysis, visualizations, and derived insights.

## Business Impact / Why This Project Is Valuable 💰

This project powerfully demonstrates my capability to transform raw sales data into actionable business intelligence. The insights derived offer clear pathways for the firm to:

* **Increase Profitability:** By strategically revising discount policies for underperforming categories and focusing resources on high-margin products.
* **Optimize Operations:** By streamlining shipping processes through data-driven identification and resolution of inefficiencies in delivery times.
* **Enhance Customer Engagement:** By developing targeted loyalty programs and personalized marketing strategies based on a deep understanding of customer behavior.
* **Improve Inventory Management:** By adjusting production and stock levels to align precisely with seasonal demand fluctuations, minimizing waste and maximizing sales opportunities.

This project serves as a compelling example of my ability to independently clean, analyze, and interpret complex datasets, consistently delivering strategic recommendations that drive tangible business value and growth.

## Contact Information / About Me 📧

**Ruthwik Devanapalli** 💼
**Senior Data Analyst | Business Consultant**

**Email**: ruthwik.devanapalli@gmail.com
**LinkedIn**: <https://www.linkedin.com/in/ruthwik-devanapalli/>

---

## License 📄

This project is intended for educational, portfolio, and demonstration purposes. Attribution is appreciated when used or adapted.

-----------------------------------------------------------------------------------------------------------------------------------------------