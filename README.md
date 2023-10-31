## Analytics Project Startup

It is expected that as a Power BI Data Analyst you will be wearing the hat of a Business Analyst in the idea creation and project startup phase of an analytics project.  

The following assets can be used to document the requirements :

### Requirements Traceability Matrix

This register matrix provides an organized overview of all the requirements for the Power BI Accelerator project and maps them to their corresponding test case IDs. This ensures that each requirement is tested, validated, and tracked through to completion.

| Requirement ID | Requirement Description                                  | Test Cases   | Status       | % Complete  |
|----------------|-----------------------------------------------------------|--------------|--------------|-------------|
| REQ001         | The dashboard must provide a real-time sales overview.    | TC001, TC002 | In Progress  | 50%         |
| REQ002         | Users should be able to filter data by date ranges.       | TC003, TC004 | Completed    | 100%        |
| REQ003         | Inventory levels must be displayed with visual alerts.    | TC005, TC006 | Not Started  | 0%          |
| REQ004         | Data integration from the Integrated Justice Information System (IJIS). | TC007, TC008 | In Progress | 75%         |
| REQ005         | Provide export functionality for all reports in Excel format. | TC009, TC010 | Completed  | 100%        |
| REQ006         | Implement role-based access controls for different user groups. | TC011, TC012 | In Progress | 60%         |
| REQ007         | The dashboard must be mobile-responsive.                  | TC013, TC014 | Not Started | 0%          |

## Guidelines for Register Maintenance

1. **Requirement Addition**: When a new requirement is identified, add it to this register with a comprehensive description.
2. **Test Case Association**: Ensure each requirement is linked to its corresponding test case IDs. This guarantees that requirements are validated through testing.
3. **Status & Completion Tracking**: Regularly update the status and percentage completion of each requirement to keep stakeholders informed.
4. **Review & Documentation**: Periodically review the register for accuracy and document any changes or updates made to the requirements or their associated test cases.

By diligently maintaining this register, we ensure each requirement's progression is transparent, tested, and validated, ensuring the success of our Power BI accelerator.





### Data Source Register

This register provides an overview of all data sources used in the Power BI Accelerator project, detailing specifics, update frequency, status, data ownership, and authentication method for each source.

| Source ID | Data Source Name                        | Description                                                | Type      | Location/Endpoint         | Update Frequency | Status     | Data Owner    | Authentication By       |
|-----------|-----------------------------------------|------------------------------------------------------------|-----------|---------------------------|------------------|------------|---------------|-------------------------|
| #1        | Integrated Offender Management System (IOMS) | System managing offender data and case histories.    | Database  | SQL Server                | Monthly          | Active     | @johndoe      | Windows Auth            |
| #2        | Integrated Justice Information System (IJIS) | System with justice-related information and records. | Database  | Oracle DB                 | Weekly           | Active     | @janedoe      | SQL Auth                |
| #3        | Report Manager                           | Centralized platform for managing all reports.             | Web App   | [Report Manager URL](#)   | On Demand        | Active     | @aliceblue    | Work Account            |
| #4        | NTCS Accommodation Statistics Sheets     | Sheets providing details on accommodation statistics.      | Excel     | SharePoint Link           | Quarterly        | Inactive   | @tomsmith     | Work Account            |
| #5        | NTCS Reception Statistics Sheets         | Sheets detailing reception statistics and metrics.         | Excel     | OneDrive Link             | Bi-Annually      | Active     | @maryjane     | API Token               |

Data Source Management Guidelines

1. **Identification & Addition**: New data sources should be added to this register with comprehensive details.
2. **Validation**: Regular quality checks are crucial to ensure data accuracy and reliability.
3. **Update & Refresh**: Adhere to the documented update frequency and ensure timely data refreshes.
4. **Ownership & Responsibility**: Assign a specific data owner for each source. They will oversee updates, quality checks, and handle data-related issues.
5. **Security & Authentication**: Implement secure authentication methods and review them periodically to mitigate security risks.

By maintaining this register, we aim for transparency, accuracy, and security in our data sources, the backbone of our Power BI reports.

### High Level Table Register (Table or Table Group Level)

| Table Group | Table Name | Source | Mapping | Transformation | Calculation | KPI | Report |
|-------------|------------|--------|---------|----------------|-------------|-----|--------|
| Group A     | Table1     | 2      | 4       | 5              | 3           | 6   | 5      |
| Group A     | Table2     | 3      | 3       | 4              | 5           | 7   | 6      |
| Group B     | Table3     | 1      | 2       | 3              | 4           | 5   | 6      |
| Group B     | Table4     | 5      | 6       | 7              | 8           | 9   | 7      |
| Group C     | Table5     | 4      | 3       | 2              | 1           | 3   | 4      |
| Group C     | Table6     | 6      | 5       | 7              | 6           | 8   | 9      |

### High Level License Assessment (License Level)

| Group        | License/Infrastructure  | Readers | Contributors | Admins | Data Storage (GB) |
|--------------|-------------------------|---------|--------------|--------|-------------------|
| On Prem      | Power BI Report Server2 | 10      | 5            | 2      | 2                 |
| On Prem      | Power BI Report Server2 | 20      | 10           | 4      | 0.5               |
| On Prem      | ODBC Licenses           | -       | -            | 2      | -                 |
| Cloud        | Power BI Pro            | 25      | 12           | 5      | 120               |
| Cloud        | Power Automate          | -       | -            | 2      | -                 |
| Other        | Third Party             | -       | -            | -      | 10                |

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


High Change Management Register (Individual Change Level)

| Change ID | Change Description                                  | Requested By | Date Requested | Impact on Timeline | Adjusted Plan                                         | Status     | Approved By | Date Approved |
|-----------|------------------------------------------------------|--------------|----------------|---------------------|-------------------------------------------------------|------------|-------------|---------------|
| #1        | Addition of a new data source for sales metrics     | @johndoe     | Jan 1, 2023    | +2 days            | Extend data integration phase by 2 days.              | In Review  |             |               |
| #2        | Change in visual design for the dashboard           | @janedoe     | Jan 2, 2023    | +1 day             | Allocate extra day for UI adjustments.                 | Approved   | @tomsmith   | Jan 3, 2023   |
| #3        | Incorporation of historical data for the past 5 years| @aliceblue   | Jan 3, 2023    | +5 days            | Extend data preparation phase by 5 days.               | Rejected   | @tomsmith   | Jan 4, 2023   |

## Change Management Process

1. **Request a Change**: If you identify a need for change, add it to this register with a detailed description and the potential impact on the timeline.
2. **Review**: The project lead will review the change, assessing its impact and feasibility.
3. **Approval**: If the change is deemed necessary, it will be approved, and the plan will be adjusted accordingly. If rejected, the reason will be documented.
4. **Implementation**: Once approved, the change will be incorporated into the project, and team members will be notified of the adjustments.




## Additional Resources

- [Power BI Official Documentation](https://docs.microsoft.com/en-us/power-bi/)
- [Microsoft Certified: Power BI Expert Exam Details](https://learn.microsoft.com/en-us/certifications/power-bi)
- [Sample PL-300 Exam Questions](https://www.microsoft.com/en-us/learning/pl-300.aspx)

## Contact Information

For questions or additional information, please contact:

- Email: [your@email.com](mailto:your@email.com)
- Phone: +1 (123) 456-7890

We look forward to helping you succeed in the Power BI PL-300 exam and advancing your skills in data preparation, modeling, visualization, and deployment!
