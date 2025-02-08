# Mobile Sales Dashboard using Power BI

## Project Overview

This project involves creating an interactive and insightful dashboard to analyze mobile sales data across various dimensions such as city, brand, and payment methods. The dashboard provides a comprehensive view of sales performance, helping stakeholders make informed decisions.

## Dashboard 

https://github.com/user-attachments/assets/149f3aed-7a2d-4336-ada5-98eb171c9a0f

## Objectives

- **Data Import and Transformation**: Import raw sales data and perform necessary cleaning and transformation using Power Query.
- **Data Modeling**: Establish relationships among tables to create a structured data model for efficient querying.
- **DAX Calculations**: Utilize Data Analysis Expressions (DAX) to create measures and calculated columns for in-depth analysis.
- **Visualization**: Design an interactive dashboard with various visualizations to represent sales data effectively.

## Data Source

The dataset used in this project is `Mobile Sales Data.xlsx`, which contains information on sales transactions, including:

- **Date**: The date of the transaction.
- **City**: The city where the sale occurred.
- **Brand**: The brand of the mobile phone sold.
- **Model**: The specific model of the mobile phone.
- **Quantity**: The number of units sold.
- **Revenue**: The total revenue generated from the sale.
- **Payment Method**: The method of payment used by the customer.
- **Customer Rating**: The rating provided by the customer.

## Data Transformation

Using Power Query, the following transformations were applied:

- **Data Cleaning**: Removed duplicates and handled missing values to ensure data quality.
- **Data Type Conversion**: Converted columns to appropriate data types (e.g., dates, text, numbers).
- **Custom Columns**: Created custom columns where necessary to facilitate analysis.

## Data Modeling

Established relationships between tables to create a star schema, optimizing the data model for analysis. The primary tables include:

- **Sales Fact Table**: Contains transactional data.
- **Dimension Tables**: Includes dimensions such as Date, City, Brand, and Payment Method.

## DAX Calculations

Implemented various DAX measures to enhance analysis:

- **Total Sales**:
  ```DAX
  Total Sales = SUM(Sales[Revenue])
  ```
- **Total Quantity Sold**:
  ```DAX
  Total Quantity Sold = SUM(Sales[Quantity])
  ```
- **Average Selling Price**:
  ```DAX
  Average Selling Price = DIVIDE([Total Sales], [Total Quantity Sold])
  ```
- **Sales YTD**:
  ```DAX
  Sales YTD = TOTALYTD([Total Sales], 'Date'[Date])
  ```
- **Sales LY**:
  ```DAX
  Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
  ```

## Dashboard Visualizations

The Power BI dashboard includes the following visualizations:

- **Total Sales by City**: A map visual displaying revenue distribution across different cities.
- **Monthly Sales Trend**: A line chart showing sales trends over time.
- **Sales by Brand**: A bar chart comparing sales performance among various brands.
- **Payment Method Distribution**: A pie chart illustrating the proportion of sales by different payment methods.
- **Customer Ratings**: A column chart categorizing customer ratings into Good, Average, and Poor.

## Insights

- **Top Performing Cities**: Identified cities with the highest sales volumes.
- **Best-Selling Brands**: Determined which brands are leading in sales.
- **Preferred Payment Methods**: Analyzed customer preferences in payment methods.
- **Sales Trends**: Observed seasonal trends and peak sales periods.
- **Customer Satisfaction**: Assessed customer satisfaction levels based on ratings.

## Conclusion

This project demonstrates the effective use of Power BI for analyzing mobile sales data, providing valuable insights to drive business decisions. The interactive dashboard allows users to explore data across multiple dimensions and gain a deeper understanding of sales performance.

## Files in the Repository

- `Mobile Sales Data.xlsx`: The dataset containing sales transaction records.
- `Mobile sales.pbix`: The Power BI project file with the developed dashboard.
- `Background.jpg`: Background image used in the dashboard design.
- `Icons/`: Directory containing icons utilized in the dashboard.
- `README.md`: Project documentation.

## Getting Started

To explore the dashboard:

1. Clone the repository to your local machine.
2. Open `Mobile sales.pbix` using Power BI Desktop.
3. Interact with the visualizations to gain insights from the data.

For any questions or feedback, feel free to open an issue in this repository.

---

*Note: This project is for educational purposes and is based on fictional data.*
