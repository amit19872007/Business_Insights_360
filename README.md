# Business_Insights_360
## Project Overview 
AtliQ Hardware, a fast-growing consumer electronics company operating across multiple countries, has relied on traditional methods like MS Excel and Power Point for data analysis and visualization. However, this approach led to less accurate and time-consuming decision-making processes. To address these challenges, they're transitioning to PowerBI for data analytics. This shift aims to facilitate faster, more accurate, and data-driven decision-making across finance, sales, marketing, and supply chain aspects.

You can access the report from [here](https://www.novypro.com/project/atliq-hardware-business-insight-360-power-bi-1)

## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- Power query
- DAX studio (for optimizing the report)
- Project charter file

## Key Learnings:
### Power BI
- Softskills (How to carry out the discussions, expectation management, stake holder management, etc.)
- Data modeling
- Data analysis and techniques
  - Creating calculated columns
  - Creating measures using DAX language
  - Using Bookmarks to switch between two visuals
  - Page navigation with buttons
  - Using divide function to prevent zero division errors
  - Creating date table using m language
  - Dynamic titles based on the applied filters
  - KPI indicators
  - Conditional formatting the values in visuals using icons or background color
- Data validation techniques
- UAT (User Acceptance Technique)
- Use of PowerBi services
- Report publishing to PowerBI services
- Setting up personal gateway to set up the auto refresh of data
- PowerBi App creation
- Collaboration, workspace, access permissions in PowerBi services

## GitHub 

- Uploading Large size files using GitHub LFS
- Tracking the particular type of file extensions for LFS NB

## Company Information
AtliQ hardware is a global company, sells computer, computer accessories and Network devices through following channels:
  - Retailers
  - Direct
  - Distributors
Company was relying on traditional methods of analysis Excel and PowerPoint for visulation. This approach is time consuming and error prone. To address these challenges, they're transitioning to PowerBI for data analytics.

**This shift aims to facilitate faster, more accurate, and data-driven decision-making across finance, sales, marketing, and supply chain aspects.**

### Questions to ask before starting with dashboard

- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be time dead-line of the project?
- do the stakeholders expecting pre-view before the actual release?
- What are all the hopes stakeholders have out of this project?
- what are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- what are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- what are all the resources/ data needed to build this dashboard?
- is there any inputs from stakeholders in terms of design and views of the dashboard?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

### Dataset **Understanding.**

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

## Importing data into PowerBi

- As we used MySql Database, imported datasets from database to PowerBI (need to provide access rights / credentials)
