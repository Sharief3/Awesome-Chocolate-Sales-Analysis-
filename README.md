# Awesome-Chocolate-Sales-Analysis

## Project Objective
To design and develop a comprehensive sales analytics dashboard in Power Bi for a fictional company, Awesome Chocolate, with the goal of providing actionable insights into key business metrics such as sales, boxes, shipments, cost, profit, and employee performance. This end-to-end BI solution covers the entire workflow-from data modeling using a star schema and writing DAX measures, to creating an interactive, visually compelling dashboard complete with tooltips, dynamic views, and filter panels

## Data Set Used
<a href="https://app.powerbi.com/links/iNNMN3jznq?ctid=eb322777-d3cb-4cf3-8785-b55cf5ec11ce&pbi_source=linkShare">Data set</a>

## The Setup
.1. chocolate sales analytics
.2. sales, boxes, costs & profits
.3.sales-person & product performance
.4. low box shipment analysis
.5. save and publish the project

-Dashboard Interaction <a href="Screenshot 2025-08-03 114556.png">View Dashboard</a>



## Process
-	Awesome Chocolate Data Model
-	Data load to Powe Bi
-	Star Schema creation  
-	Creating DAX measures
-	Using the calendar table to make “time intelligence” measures
-	Wireframe design for our dashboard
-	Dashboard page design and theme in Power Bi
-	KPI cards for the Power Bi sales analytics dashboard
-	Fixing the MoM calculation Dax
-	Adding reference labels for the KPI cards
-	Formatting the KPI section
-	Profit% Gauge chart
-	Dynamic trend analysis chart(with field parameters)
-	Shipment analysis (histogram + zoom slider)
-	Sales person performance –Table design product performance Table
-	Bookmark for Product vs. People view
-	Filter panel design 
-	Tooltip panel design
-	 Final version(with two options)

## Dashboard
<img width="1322" height="736" alt="Screenshot 2025-08-03 114556" src="https://github.com/user-attachments/assets/754f8dda-4563-4054-bced-7d68e1e6ad66" />


# Project insights
 
  * The project focuses on **sales analytics for a fictional chocolate company called "Awesome Chocolate"** 
    *  1. It analyzes sales, boxes shipped, costs, and profits, assessing the performance of salespersons and products
    *  2. A special focus is given to "Low Box Shipments" (less than 50 boxes per shipment), calculating their count and percentage
    *  3. simplified star schema, consisting of a central "shipments" fact table and four dimension tables: salesperson, product, geography, and calendar (date)
      
     *  4. The shipment data spans 13 months, from February 1, 2023, to the end of February 2024

  * Key Calculations and Measures (DAX)
 
* The project emphasizes calculating various Key Performance Indicators (KPIs) or measures

  * Basic Measures: Total sales (sum of sales column), total boxes (sum of boxes column), and total shipments (count of rows in the shipments table)
    
  * Cost and Profitability: Total cost calculation involves joining shipment and product data to multiply boxes by cost per box . Total profit is then calculated as total sales minus total costs, and profit percentage is derived from these.

    * Low Box Shipments: `LBS Count` is calculated by counting shipments with less than 50 boxes, and `LBS Percentage` is derived from `LBS Count` divided by `Total Shipments`.
  
  * Time Intelligence: Month-on-month and year-on-year changes for key metrics are calculated using DAX functions like `PREVIOUSMONTH`. The calendar table is marked as a date table in Power BI to facilitate these calculations . Derived columns like month number, month name, and year are added to the calendar table in Power Query for easier analysis and visualization.
  
   * Latest Month Metrics: Specific measures like `Total Sales Latest Month` and `Latest Month-on-Month Sales Change` are created to display current performance figures at a grand total level in card visuals, ensuring dynamic filtering behavior.

      * Profit Target Indicator: A custom measure calculates whether a salesperson's profit percentage meets a defined target, using a binary (or ternary) indicator for conditional formatting

 **Dashboard Design and Features
 
   * Wireframing: The design process begins with a wireframe in PowerPoint, laying out a **summary view at the top** (key numbers with month-on-month changes) and **detailed views below** (product and salesperson performance, trend analysis)
      *Canvas Settings: The report canvas is set to a custom size (e.g., 1080x1920 pixels) for optimal viewing.
      1*New Card Visual: This enhanced visual is used to display multiple key metrics (sales, boxes, shipments, costs, profit) along with their month-on-month changes as reference labels . It allows for extensive styling, including conditional formatting for negative changes.
       *Images/Icons: Small custom icons are added next to measures in card visuals for better context and visual appeal
 * Gauge Chart :Used for the profit percentage indicator, allowing a visual representation of performance against a target
        *Field Parameters: A "measure selector" field parameter is created to allow users to dynamically switch between different measures (sales, boxes, shipments, costs, profit) on a single trend line chart 
      *New Slicer Visual: Provides a modern, button-like interface for the measure selector, with customizable styling for selected and unselected states 
      *Grouping (Histogram): The `boxes` column is grouped into bins to create a histogram showing the distribution of shipment sizes, highlighting the density of low-box shipments
      * Zoom Slider: Enabled on the x-axis of the histogram to allow interactive zooming into specific ranges of box bins during presentation
        
        * Table Formatting: Detailed formatting is applied to tables, including image sizing, row padding, column renaming, and conditional formatting (icons for profit target, data bars for profit percentage
          
      * Bookmarks and Selection Panel: Used to create interactive toggles (people vs. product detail tables) on the same report areas
        
        * Tooltips: A dedicated tooltip page is created for the trend chart, showing a donut chart breakdown of the selected measure by geography for a specific month. Tooltip pages are set to a smaller page type and can have distinct background colors

# The Data Models

. shipments
. geographical dimension
. sales person dimension
. calendar
. product dimension

## Conclusion

 Our analysis of chocolate sale data reveals clear trends in individual performance, profit margin, and product volume distribution lower box shipment (LBS%). Top performing individuals consistently combine high sale volume with strong profit margins and products.





