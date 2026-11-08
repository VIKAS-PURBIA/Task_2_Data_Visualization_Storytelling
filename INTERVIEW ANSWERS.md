# Task 2 - Interview Questions and Sample Answers

The answers below are written in first person so they can be adapted for an internship interview. Keep the wording natural and connect it to the charts in this project.

## 1. What is the importance of data visualization?
Data visualization turns large or complex datasets into patterns that people can understand quickly. It helps identify trends, compare performance, detect outliers, and communicate findings to decision-makers. For example, in this project, the monthly sales line chart makes changes over time easier to spot than reading thousands of rows.

## 2. When do you use a pie chart vs bar chart?
I use a pie or donut chart only when I need to show a simple part-to-whole relationship with a small number of categories. I prefer a bar chart when the goal is to compare values, rank categories, or read small differences because the common baseline makes comparisons clearer. For this sales analysis, bar charts are more useful for category, region, and sub-category comparisons.

## 3. How do you make visualizations more engaging?
I start with a clear business question and choose a chart that answers it. I use descriptive titles, readable labels, consistent formatting, limited colors, and annotations for important findings. I also include context such as the time period, currency, and metric definition. I avoid adding decoration that does not help the audience understand the data.

## 4. What is data storytelling?
Data storytelling combines data, visualizations, and a clear narrative to explain what happened, why it may have happened, and what action should be considered. In this project, the story moves from overall sales performance to category and regional comparisons, then to discount and sub-category profitability, and finally to practical recommendations.

## 5. How do you avoid misleading visualizations?
I use appropriate scales and clear units, start bar charts at zero when comparing magnitudes, label time ranges, and avoid truncated axes that exaggerate differences. I check aggregation levels, missing values, duplicates, and outliers before charting. I also distinguish correlation from causation and disclose dataset limitations.

## 6. What are best practices in dashboard design?
I put the most important KPIs at the top, group related charts logically, use consistent colors and number formats, and keep filters understandable. Each chart should answer one question and have a descriptive title. I remove unnecessary borders and clutter, provide enough whitespace, and make sure the dashboard works for its intended audience.

## 7. What tools have you used for visualization?
For this task, I used Python with Pandas for data preparation and Matplotlib for charts. I am also familiar with Tableau and Power BI concepts such as measures, dimensions, filters, and interactive dashboards. I can use the cleaned CSV in Tableau or Power BI to recreate the same analysis as an interactive report.

---

## 60-second project explanation
I completed a retail sales visualization project using a synthetic Superstore-style dataset. I started by checking data quality, removing duplicate records, standardizing text, converting dates and numeric fields, and handling missing values. Then I created KPIs for sales, profit, profit margin, orders, and customers. I used a line chart for monthly trends and bar charts to compare categories, sub-categories, and regions. I also used a scatter plot and discount-band analysis to examine how discounts relate to profitability. My main recommendation is to evaluate promotions using profit and margin, not sales volume alone. I documented the fact that the data is synthetic so that the findings are not mistaken for actual company performance.
