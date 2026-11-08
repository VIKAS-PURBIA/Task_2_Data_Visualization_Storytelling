# Task 2: Data Visualization and Storytelling

## Project objective
Create clear visualizations that communicate a business story, highlight important takeaways, and support practical recommendations. This follows the Task 2 brief: choose appropriate charts, avoid clutter, add context, focus on business insights, and include a summary/storyboard.

## Dataset choice and transparency
This repository uses a **synthetic Superstore-style retail sales dataset** generated with a fixed random seed for reproducibility. It contains 5,025 raw rows and 5,000 cleaned rows across 2023-2025. The assignment permits Superstore.csv or any sales data of your choice. The complete public Superstore CSV was not retrievable in the execution environment, so a synthetic alternative was generated. **Do not present the values or findings as real company results.**

## Main files
- `data/sales_raw_synthetic.csv` - generated raw practice dataset with deliberate data-quality issues.
- `data/sales_cleaned.csv` - cleaned analysis-ready dataset.
- `data/category_summary.csv`, `region_summary.csv`, `subcategory_summary.csv`, `monthly_summary.csv`, `discount_summary.csv` - aggregated analysis tables.
- `data/analysis_metrics.json` - key metrics and cleaning counts.
- `notebooks/Task2_Data_Visualization_Storytelling.ipynb` - step-by-step executable notebook.
- `reports/Task2_Visual_Storytelling_Report.pdf` - visual report and business recommendations.
- `assets/` - chart images used in the report.
- `INTERVIEW_ANSWERS.md` - answers to all seven interview questions plus a project pitch.
- `POWER_BI_TABLEAU_GUIDE.md` - steps, DAX measures, and visual field mapping to recreate the report in Power BI or Tableau.

## Key analysis questions
1. How are sales changing over time?
2. Which product categories and regions contribute most to sales and profit?
3. Which sub-categories create the strongest and weakest profit contribution?
4. How does profit margin vary across discount bands?

## Cleaning workflow
1. Strip whitespace from text columns and standardize empty values.
2. Remove exact duplicate rows.
3. Parse `Order Date` and `Ship Date` as dates.
4. Convert measures such as Sales, Profit, Quantity, Discount, and Postal Code to numeric types.
5. Remove records missing critical order/date/sales/profit fields.
6. Fill missing categorical values with `Unknown` and missing discounts with the median.
7. Create `Profit Margin`, `Order Month`, and `Order Year` fields.

Cleaning results from the generated raw file: **5,025 raw rows**, **25 duplicate rows removed**, **5,000 cleaned rows**, and **0 missing cells** in the final analysis table.

## Key findings (computed from this generated dataset)
- Total sales: **$1,776,336**
- Total profit: **$163,930**
- Overall profit margin: **9.2%**
- Distinct orders: **5,000**
- Sales-leading category: **Technology**
- Profit-leading category: **Technology**
- Sales-leading region: **West**
- Lowest-profit sub-category: **Bookcases**

## Run in Google Colab or Jupyter
### Option A: Google Colab
1. Upload the repository ZIP to Google Drive or extract it locally.
2. Open `notebooks/Task2_Data_Visualization_Storytelling.ipynb` in Colab.
3. Upload `data/sales_raw_synthetic.csv` when prompted, or keep the notebook's expected relative path after extracting the project folder.
4. Run all cells from top to bottom. The notebook recreates the cleaned CSV, summary tables, and charts.

### Option B: Local Jupyter
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```
Open the notebook and run all cells.

## Tools
Python, Pandas, NumPy, Matplotlib, Jupyter Notebook, and ReportLab (for the PDF report). The cleaned CSV can also be imported into Tableau or Power BI to build an interactive dashboard. See `POWER_BI_TABLEAU_GUIDE.md` for measures, visual mappings, and setup steps.

## Recommended dashboard layout in Power BI / Tableau
- Top row: Sales, Profit, Profit Margin, Orders, Customers KPI cards.
- Middle: Monthly sales trend and category sales/profit comparison.
- Bottom: Profit by sub-category, region performance, and discount vs profit.
- Suggested slicers: Order Year, Region, Category, and Segment.

## Important interpretation notes
- Sales and profit are line-item amounts in USD.
- Profit margin = total profit / total sales.
- Orders are counted as distinct Order IDs, not as row count.
- The discount/profit relationship is descriptive; it does not establish causation.
- Synthetic data is suitable for demonstrating a workflow, not for operational decisions. Replace it with an authorized real dataset before making business claims.

## Submission checklist
- [x] Dataset included (raw and cleaned)
- [x] Executable notebook included
- [x] Visual report PDF included
- [x] Chart assets included
- [x] README included
- [x] Interview answers included

