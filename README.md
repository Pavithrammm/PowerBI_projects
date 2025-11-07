# Revenue Radar - Sales & Profit Tracker

<img width="1312" height="736" alt="image" src="https://github.com/user-attachments/assets/c2d48d98-88fe-4427-9fac-2542d7152768" />

## Overview

This Power BI project is a interactive dashboard for analyzing retail sales and profit data. It provides key insights into total sales, profit margins, year-over-year (YoY) growth, sales by country, product performance, and detailed monthly breakdowns. Built using Microsoft's Financial Sample dataset, it's designed as a beginner-friendly portfolio piece for junior Power BI analysts.

Key features:
- **Executive KPI Page**: High-level metrics like Total Sales, Profit %, YoY Growth, with filters and country breakdown.
- **Product Performance Page**: Overview of sales and profit by product, with monthly trends.
- **Product Details Page**: Drill-through for individual product analysis, including monthly sales tables and charts.

Live Demo: [View on Power BI Service] https://app.powerbi.com/links/vquKhHp6BA?ctid=e0be73a7-0d23-4ad6-9076-c26280bf21b4&pbi_source=linkShare
## Screenshots

### Executive KPI
<img width="1310" height="736" alt="image" src="https://github.com/user-attachments/assets/309a21eb-30e7-4023-b669-55106b1a2bf6" />
 
High-level overview with cards for Total Sales (118.73M), Profit (20.4%), YoY Sales (3.49), year filter, and bar chart for sales by country (USA, Canada, France, Germany, Mexico).

### Product Performance
<img width="1309" height="737" alt="image" src="https://github.com/user-attachments/assets/894b7559-2e84-45b4-8a84-a81cc7c1b45d" />
 
Matrix table showing sales and profit margin % for products (Amarilla, Carretera, Montana, Paseo, Velo, VTT), plus a line chart for monthly sales trends.

### Product Details (Drill-Through Example: Montana)
<img width="1315" height="733" alt="image" src="https://github.com/user-attachments/assets/1aedd11d-26c9-4e23-b9b5-fb5038e471bb" />
 
Detailed view with product name, monthly sales/profit table, and line chart for sales by month.

## Requirements

- **Power BI Desktop**: Free download from [Microsoft](https://powerbi.microsoft.com/desktop/) (Version 2.XX or later).
- **Data Source**: Included in the repo as `Financial Sample.xlsx` (Microsoft's sample dataset).

No additional licenses needed for basic viewing.

## Installation & Setup

1. **Clone the Repository**:
   ```
   git clone https://github.com/Pavithrammm/revenue-radar.git
   cd revenue-radar
   ```

2. **Open the PBIX File**:
   - Launch Power BI Desktop.
   - Open `Revenue_Radar.pbix`.
   - If prompted, refresh the data source (points to `Financial Sample.xlsx` in the repo).

3. **Publish to Power BI Service** (Optional):
   - Sign in to Power BI (free account).
   - Click **Publish** > **My Workspace**.
   - Share publicly via **Publish to Web** for a live link.

## Usage

- **Navigation**: Use page tabs at the bottom (Executive KPI, Product Performance, Product Details).
- **Interactivity**:
  - Filter by year on the KPI page.
  - Right-click (or Ctrl+Click) a product on Product Performance to drill-through to details.
- **Customization**: Edit DAX measures or visuals in Power BI Desktop.

DAX Examples Used:
- Total Sales: `SUM(fact_Sales[ Sales])`
- Profit Margin %: `DIVIDE([Gross Profit], SUM(fact_Sales[ Gross Sales]), 0)`
- YoY Growth %: Uses time intelligence with date table.

## Data Source

- **Dataset**: Microsoft's Financial Sample (Excel file included).
- **Modeling**: Star schema with fact table (Sales) and dimensions (Date, Product).
- **Cleaning**: Handled in Power Query (duplicates removed, date formatting).

## Contributing

Fork the repo, make improvements (e.g., add more visuals or filters), and submit a pull request. Issues welcome!

## License

MIT License. Feel free to use for portfolios or learning. Credit appreciated!
