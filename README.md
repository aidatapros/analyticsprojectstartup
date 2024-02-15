## Analytics Project Startup

The creation of a Power BI report is mashup of data to meet the requirements of a business use case.    Business requirements inform data requirements and the output of data requirements is a specification that a Power BI developer can use as the blueprint for the work.  The high level sequence of all steps followed in the creation of a Power BI report follow this key sequence.

1. Idea Creation
2. Business Requirements
3. Data Requirements
4. Power BI License and Usage Estimate
5. Data Preparation
6. Data Model
7. Data Visualisation
8. Sharing and Collaboration

## 1. Idea Creation

An idea creation or concept on a page is thought usually through multiple workshops with the custodians of the business case (the people that will be using the Power BI report).  It can be beneficial at this early stage to stage maintaining a list of high level requirements in MOSCOW format (Must have, Should have, Could hve, Won't have) to start forming a written down view of the purpose of doing this work.   A Power BI Data Analyst may sometimes wear the hat of a Business Analyst in the early stages of creating a Power BI report if there is not one assigned to the project.

## 2. Business Requirements

The following assets can be used to help identify the requirements and therefore the data sources and lower level details :

![image](https://github.com/aidarwin/analyticsprojectstartup/assets/103006306/498464a4-3a47-42d4-9db5-3beb407dbfb0)

### Business Requirements - MOSCOW Format

This table captures project requirements using the MOSCOW format, with high level requirements gathered at a workshop assembled into individual Requirements and grouped by Requirement Group.  If you don't have any requirements yet other that to discovery your data to be able to help define requirements then Data Discovery is your requirement.

| Requirement Group        | Requirement ID | Requirement Name         | Must Have | Should Have | Could Have | Won't Have |
|--------------------------|----------------|--------------------------|-----------|-------------|------------|------------|
| A. Group 1               | B01            | Requirement Name 1       | ✅       |             |            |            |
| A. Group 1               | B02            | Requirement Name 2       | ✅       |             |            |            |
|--------------------------|----------------|--------------------------|-----------|-------------|------------|------------|
| B. Group 2               | X01            | Requirement Name 3       | ✅       |            |            |            |
| B. Group 2               | X02            | Requirement Name 4       | ✅       |            |            |            |
| B. Group 2               | X02            | Requirement Name 5       | ✅       |            |            |            |
| B. Group 2               | X03            | Requirement Name 6       |          |             | ✅         |            |
| B. Group 2               | X03            | Requirement Name 7       |          |             | ✅         |            |
|--------------------------|----------------|--------------------------|-----------|-------------|------------|------------|
| C. Group 3               | R01            | Requirement Name 8       | ✅       | ✅          |            |            |
| C. Group 3               | R02            | Requirement Name 9       | ✅       | ✅           |            |            |
|--------------------------|----------------|--------------------------|-----------|-------------|------------|------------|


- ✅ Must Have: Critical requirements that must be implemented.
- ✅ Should Have: Important requirements that should be considered.
- ✅ Could Have: Desirable requirements that could be implemented if resources allow.
- ✅ Won't Have: Requirements that are explicitly excluded from the current scope.

## 3. Data Requirements

Update this table with your project's specific requirements and priorities.

### Requirements Traceability Matrix

This register matrix provides an organized overview of all the requirements for the Power BI Accelerator project and maps them to their corresponding test case IDs. This ensures that each requirement is tested, validated, and tracked through to completion.  Each requirement will inform data requirements and how the data will be validated in testing.  By diligently maintaining this register, we ensure each requirement's progression is transparent, tested, and validated, ensuring the success of our Power BI accelerator.

| Requirement ID | Requirement Description                                  | Test Cases   | Status       | % Complete  |
|----------------|-----------------------------------------------------------|--------------|--------------|-------------|
| REQ001         | The dashboard must provide a real-time sales overview.    | TC001, TC002 | In Progress  | 50%         |
| REQ002         | Users should be able to filter data by date ranges.       | TC003, TC004 | Completed    | 100%        |
| REQ003         | Inventory levels must be displayed with visual alerts.    | TC005, TC006 | Not Started  | 0%          |
| REQ004         | Data integration from the Integrated Justice Information System (IJIS). | TC007, TC008 | In Progress | 75%         |
| REQ005         | Provide export functionality for all reports in Excel format. | TC009, TC010 | Completed  | 100%        |
| REQ006         | Implement role-based access controls for different user groups. | TC011, TC012 | In Progress | 60%         |
| REQ007         | The dashboard must be mobile-responsive.                  | TC013, TC014 | Not Started | 0%          |
| REQ008         | Data will be sourced from X,Y,Z source systems and manually entered data will be captured through Excel in Teams channel.                  | TC015, TC016 | Not Started | 0%          |

Guidelines for Requirements Traceability Register Maintenance

1. **Requirement Addition**: When a new requirement is identified, add it to this register with a comprehensive description.
2. **Test Case Association**: Ensure each requirement is linked to its corresponding test case IDs. This guarantees that requirements are validated through testing.
3. **Status & Completion Tracking**: Regularly update the status and percentage completion of each requirement to keep stakeholders informed.
4. **Review & Documentation**: Periodically review the register for accuracy and document any changes or updates made to the requirements or their associated test cases.


### Data Source Register

This register provides an overview of all data sources used in the Power BI Accelerator project, detailing specifics, update frequency, status, data ownership, and authentication method for each source.  This is a high level list of data sources you will connect to in order to then select tables to bring into the Power Query Editor.  By maintaining this register, we aim for transparency, accuracy, and security in our data sources, and inform the first step in Preparation of Data in Power BI - "Get Data". 

| Source ID | Data Source Name                        | Description                                                | Type      | Location/Endpoint         | Update Frequency | Status     | Data Owner    | Authentication By       |
|-----------|-----------------------------------------|------------------------------------------------------------|-----------|---------------------------|------------------|------------|---------------|-------------------------|
| #1        | Fleet Management System | System for tracking and managing fleet vehicles on the move.    | Database  | SQL Server                | Monthly          | Active     | @johndoe      | Windows Auth            |
| #2        | Asset System | System for managing financial asset information. | Database  | Oracle DB                 | Weekly           | Active     | @janedoe      | SQL Auth                |
| #3        | Report Manager                           | Centralised platform for viewing data in Paginated printable reports.             | Web App   | [Report Manager URL](#)   | On Demand        | Active     | @aliceblue    | Work Account            |
| #4        | Health and Safety Workplace Statistics Sheets     | Sheets providing manually entered details on workplace incidents.      | Excel     | SharePoint Link           | Quarterly        | Inactive   | @tomsmith     | Work Account            |
| #5        | Public Holiday Calendar         | Sheets recording public holidays for each rostering group.         | Excel     | OneDrive Link             | Bi-Annually      | Active     | @maryjane     | API Token               |

Data Source Management Guidelines

1. **Identification & Addition**: New data sources should be added to this register with comprehensive details.
2. **Validation**: Regular quality checks are crucial to ensure data accuracy and reliability.
3. **Update & Refresh**: Adhere to the documented update frequency and ensure timely data refreshes.
4. **Ownership & Responsibility**: Assign a specific data owner for each source. They will oversee updates, quality checks, and handle data-related issues.
5. **Security & Authentication**: Implement secure authentication methods and review them periodically to mitigate security risks.


### High Level Table Register (Table or Table Group Level)

This is a lower level list of datasets you will bring into the Power Query Editor.

| Table Group | Table Name | Source | Mapping | Transformation | Calculation | KPI | Report |
|-------------|------------|--------|---------|----------------|-------------|-----|--------|
| Group A     | Table1     | 2      | 4       | 5              | 3           | 6   | 5      |
| Group A     | Table2     | 3      | 3       | 4              | 5           | 7   | 6      |
| Group B     | Table3     | 1      | 2       | 3              | 4           | 5   | 6      |
| Group B     | Table4     | 5      | 6       | 7              | 8           | 9   | 7      |
| Group C     | Table5     | 4      | 3       | 2              | 1           | 3   | 4      |
| Group C     | Table6     | 6      | 5       | 7              | 6           | 8   | 9      |

### High Level Table Register (Table or Table Group Level)

The design of the database schema or semantic model, including the use of a central table and how to best join to filter tables, needs to be evaluated against specific reporting requirements, the volume of data, and the performance considerations.

Declare the grain of the fact table
Describe the filter tables

Now test this design against these considerations to check the desing of the data model can meet the project objectives:

## 4. Power BI License and Usage Estimate

Reporting Requirements: Ensure that the design meets the reporting requirements of your application. Are you able to retrieve the necessary data efficiently? Does it support the types of queries and reports you need to generate?

Data Volume: Consider the volume of data in your database. If you have a large amount of data, the efficiency of your queries becomes even more critical. Ensure that the schema and indexing are optimized for performance.

Indexing: Proper indexing is crucial for performance in a reporting database. Make sure that appropriate indexes are defined on the columns used in joins and where clauses to speed up query execution.

Query Complexity: Evaluate the complexity of the queries you need to run. If your queries involve multiple joins and aggregations, it's essential to design your schema and indexes to handle these efficiently.

Maintenance: Consider the maintenance aspect of your schema. Many-to-many relationships can be complex to manage, and you'll need to ensure data integrity, especially if records are frequently added or updated.

Denormalization: Depending on your reporting needs, you might consider denormalizing some data to improve query performance. Denormalization can involve duplicating data in a reporting table to reduce the need for complex joins.

Reporting Tools: The choice of reporting tools and software can also impact your design. Some reporting tools may work better with specific database structures, so you should consider the tools you plan to use.

Testing and Optimization: Always test the performance of your reporting queries and continuously optimize them as needed. Database profiling and query optimization techniques can help identify and address performance bottlenecks.

Future Scalability: Consider whether your design can scale to accommodate future data growth and evolving reporting requirements.

In summary, the design of a central table joined to multiple tables in many-to-many relationships can work well for reporting if it's properly optimized for performance and meets your specific requirements. It's important to carefully analyze your use case, data volume, and query complexity to determine if this design is suitable or if any adjustments, such as denormalization or additional indexing, are needed to ensure efficient reporting.

### High Level License Assessment (License Level)

| Group        | License/Infrastructure  | Readers | Contributors | Admins | Data Storage (GB) |
|--------------|-------------------------|---------|--------------|--------|-------------------|
| On Prem      | Power BI Report Server2 | 10      | 5            | 2      | 2                 |
| On Prem      | Power BI Report Server2 | 20      | 10           | 4      | 0.5               |
| On Prem      | ODBC Licenses           | -       | -            | 2      | -                 |
| Cloud        | Power BI Pro            | 25      | 12           | 5      | 120               |
| Cloud        | Power Automate          | -       | -            | 2      | -                 |
| Other        | Third Party             | -       | -            | -      | 10                |

## 5. Data Preparation

When we know our data requirements, our work begins in the Data Preparation stage as the key component of effort to get right before we move onto creating a concise and flexible Data Model.   Power Query Editor is where you will spend time shaping the data into the right structure.  Then in the Power BI Desktop Model editor is where you define the model - Relationships between the tables, Storage mode for Tables and Calculations.   This all needs to be right before we create visuals.  Access to data is always the first challenge and usually begins with a high level discussion with those who are already using those data sources.  Testing the connection works and ensuring you have access to the correct data is the first step in data preparation phase.  This can inform or help articulate requirements and when used with a data dictionary, will help determine the precise specification of where you need to source your data from. 

In the data preparation step, a high level understanding or statement about "The Grain" of the data should already be known.

## 6. Data Model



## 7. Data Visualisation

### Visual Design

Wallpaper :

A blank canvas is the usual starting place for your Power BI Report.   It will help to get your canvas looking like a professional dashboard before you start.  This immediately gets you and your clients thinking about how the data needs to look.

![Concept 1 Wallpaper Starter](https://github.com/aidarwin/analyticsprojectstartup/assets/103006306/8910d20f-0740-47cb-803c-26790ce15e73)

Click anywhere on your blank page, select the page settings and change the following attributes in the Canvas settings to apply your visual canvas :
1. Click Browse and location your canvas image
2. Select on Fit to Page
3. Set the transparency to 0%
![image](https://github.com/aidarwin/analyticsprojectstartup/assets/103006306/3e4d3405-f2f1-4a8a-9247-bdc43d658ec6)

Report Theme :

Apply a Report Theme to tie together all of the other visual design as per your customer branding guidlines.  A report theme allows you to predefine the colours used through the report to ensure they are consistent with client branding guidelines.

https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-report-themes


### DAX Calculation & KPI Register: Power BI Accelerator Project

This document provides an overview of all DAX calculations and KPIs utilized in the Power BI Accelerator project. It outlines the purpose, formula, and context of each calculation and KPI to ensure clarity and consistency across the project.

| Calc ID | Calculation Name     | Description                                          | DAX Formula                                                      | Context/Usage                       |
|---------|----------------------|------------------------------------------------------|------------------------------------------------------------------|-------------------------------------|
| #1      | Total Sales          | Computes the total sales across all products.        | `Total Sales = SUM(Sales[SalesAmount])`                          | Used in monthly sales dashboard.    |
| #2      | Average Sales        | Calculates the average sales per product.            | `Average Sales = AVERAGE(Sales[SalesAmount])`                    | Used in product performance report. |
| #3      | YoY Growth           | Year-over-Year growth comparison for sales.          | `YoY Growth = (Total Sales - [Total Sales LY]) / [Total Sales LY]` | Used in annual sales trend analysis.|
| #4      | Total Customers      | Counts the total number of unique customers.         | `Total Customers = COUNTAX(ALL(Customers[CustomerID]), Customers[CustomerID])` | Used in customer insights report.   |

### Key Performance Indicators (KPIs)

| KPI ID | KPI Name               | Description                                        | DAX Formula or Measure                                        | Target Value | Context/Usage                       |
|--------|------------------------|----------------------------------------------------|---------------------------------------------------------------|--------------|-------------------------------------|
| #1     | Monthly Sales Target   | Compares monthly sales against the target.         | `[Total Sales]`                                               | 500,000      | Monthly sales performance dashboard.|
| #2     | Customer Growth Rate   | Monthly growth rate of acquiring new customers.    | `Customer Growth = ([Total Customers] - [Total Customers LY]) / [Total Customers LY]` | 10%          | Customer growth analysis report.    |
| #3     | Sales Conversion Rate  | Percentage of leads that converted into sales.     | `Conversion Rate = [Total Sales] / COUNT(Leads[LeadID])`      | 25%          | Used in sales funnel analysis.      |
| #4     | Product Return Rate    | Percentage of sold products that were returned.    | `Return Rate = COUNT(Returns[ReturnID]) / [Total Sales]`      | Below 5%     | Quality control dashboard.          |

Guidelines for Calculation and Register Maintenance

1. **Addition**: When introducing a new DAX calculation or KPI, ensure it's added to this register with comprehensive details.
2. **Validation**: Regularly validate the formulas to ensure they provide accurate results.
3. **Review**: Periodically review the KPIs against actual performance and adjust targets as necessary.
4. **Documentation**: Document any changes or updates made to existing calculations or KPIs.

By maintaining this register, we aim for clarity, accuracy, and consistency in our DAX calculations and KPIs, ensuring the reliability and relevance of our Power BI reports.
## 8. Sharing and Collaboration

Roles and Permission register.

To do...

Handover to Support knowledge base.

To do...

High Change Management Register (Individual Change Level)

| Change ID | Change Description                                  | Requested By | Date Requested | Impact on Timeline | Adjusted Plan                                         | Status     | Approved By | Date Approved |
|-----------|------------------------------------------------------|--------------|----------------|---------------------|-------------------------------------------------------|------------|-------------|---------------|
| #1        | Addition of a new data source for sales metrics     | @johndoe     | Jan 1, 2023    | +2 days            | Extend data integration phase by 2 days.              | In Review  |             |               |
| #2        | Change in visual design for the dashboard           | @janedoe     | Jan 2, 2023    | +1 day             | Allocate extra day for UI adjustments.                 | Approved   | @tomsmith   | Jan 3, 2023   |
| #3        | Incorporation of historical data for the past 5 years| @aliceblue   | Jan 3, 2023    | +5 days            | Extend data preparation phase by 5 days.               | Rejected   | @tomsmith   | Jan 4, 2023   |

### Change Management Process

1. **Request a Change**: If you identify a need for change, add it to this register with a detailed description and the potential impact on the timeline.
2. **Review**: The project lead will review the change, assessing its impact and feasibility.
3. **Approval**: If the change is deemed necessary, it will be approved, and the plan will be adjusted accordingly. If rejected, the reason will be documented.
4. **Implementation**: Once approved, the change will be incorporated into the project, and team members will be notified of the adjustments.




### Additional Resources

- [Power BI Official Documentation](https://docs.microsoft.com/en-us/power-bi/)
- [Microsoft Certified: Power BI Expert Exam Details](https://learn.microsoft.com/en-us/certifications/power-bi)
- [Sample PL-300 Exam Questions](https://www.microsoft.com/en-us/learning/pl-300.aspx)

### Contact Information

For questions or additional information, please contact:

- Email: peter@aidarwin.com.au

We look forward to helping you succeed in your Analytics Project Startup!
