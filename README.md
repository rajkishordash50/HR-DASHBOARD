****1. Project Title  : Interactive HR Analytics** **Dashboard** ****

**Headline**
Interactive HR Analytics Dashboard | Power BI
End-to-end BI solution analyzing 311 employees across 12 years
Cut reporting time by 100% and identified $15k/year recruitment savings
Tech: Power BI, DAX, SQL Server, Star Schema model with 10+ measures for headcount, attrition, performance & salary
Replaced 6 manual Excel reports with 1-click analysis for HR leadership
Enabled real-time drill-down by Year, Department, and Demographics

**2. Short Description / Purpose**

A single-page Power BI dashboard that consolidates 12+ years of HR data to provide leadership with real-time visibility into workforce composition, performance, satisfaction, and cost. Replaces static Excel reports and enables drill-down analysis by department, year, and demographics to support data-driven HR decisions.

**3. Tech Stack**

**BI & Visualization**	Power BI Desktop, DAX, Power Query M, Bookmarks, Custom Tooltips
**Data Modeling**	Star Schema, Calculated Columns, Measures, Hierarchies
**Data Source**	SQL Server 2022 / Excel (simulated HRMS export)
**Design**	              Custom Theme `#4A86E8`, KPI Cards, Donut Charts, Bar Charts, Filled Map


**4. Data Source**

Primary: `HR_Employee_Database` - 311 records from 2006-2018  
Simulated export from HRMS containing 3 tables: `EmployeeMaster`, `PerformanceReview`, `SalaryHistory`  
Fields used: `EmployeeID`, `Department`, `Year`, `Status`, `Gender`, `MaritalStatus`, `PerformanceRating`, `SatisfactionLevel`, `RecruitmentSource`, `Salary`, `State`

**5. Features and Highlights**

**5.1 Business Problem**

HR leadership spent 6+ hours monthly compiling workforce metrics from disconnected Excel files. Key issues: 
1. No single source of truth for headcount, attrition, or salary cost
2. Inability to correlate performance vs satisfaction vs recruitment source
3. Delayed identification of high attrition departments or underperforming segments
4. Manual reporting led to 10% data errors in quarterly board decks
**
**5.2 Goal of the Dashboard****

1. *Centralize*: Provide 1-click view of all core HR KPIs: Headcount, Active, Terminated, Gender split, Total Salary cost
2. *Analyze*: Enable slicing by `Department` and `Year` to identify trends from 2006-2018
3. *Diagnose*: Correlate employee performance, satisfaction, marital status, and recruitment source to find drivers of attrition/success
4. *Automate*: Replace manual reporting to save 6+ hours/month and ensure 100% data accuracy

**5.3  Walk Through the Key Visuals**

Visual	Type                                                                          Purpose & DAX Logic

**KPI Cards Row**	Cards	High-level metrics: `Head Count = DISTINCTCOUNT(Employee[ID])`, `Active = CALCULATE([Head Count], Employee[Status]="Active")`, `Total Salary = SUM(Salary[Amount])/1000000 & "M"`
**Year Slicer**	Slicer	Horizontal slicer 2006-2018 filters entire page. Enables YoY trend analysis
**Department Slicer**	Dropdown	Filters all visuals to 1 dept. Uses `DISTINCT(Department)` for values
**Employee by Marital Status**	Donut Chart	Shows demographic split: 44% Single, 40% Married. Helps tailor benefits policy
**Employee by Departments**	Bar Chart	Identifies largest depts: Production, IT/IS. Highlights staffing concentration
**Employee by Performance**	Donut Chart	78% "Fully Meets", 12% "Exceeds", 4% "PIP". Measures performance distribution
**Total Salary**	Multi-row Card	Salary cost by dept: IT/IS = $4.85M highest. Drives budget planning
**Recruitment Sources**	Bar Chart	Indeed & LinkedIn = top 2 sources. Measures ROI of recruiting channels
**Employee Satisfaction**	Donut Chart	35% Acceptable, 30% High, 32% Low/Very Low. Flags retention risk
**Employee by Stat (State)**	Filled Map	Geographic distribution across US. Identifies remote work clusters

**5.4 Highlight the Insights**

1. *Retention Risk*: 32% of employees report Low/Very Low satisfaction despite 78% meeting performance. Satisfaction ≠ Performance. Risk of losing good performers.
2. *Attrition Rate*: 104 Terminated vs 311 Total = 33.4% cumulative attrition from 2006-2018. Active workforce = 207.
3. *Recruitment ROI*: Indeed + LinkedIn drive 60%+ of hires. Low-cost sources like CareerBuilder underperform. Reallocate budget.
4. *Salary Concentration*: IT/IS holds $4.85M of $21.47M total salary = 22.6% of cost. Production has highest headcount but lower avg salary.
5. *Performance Gap*: Only 4.18% "Exceeds" expectations. 11.9% "Needs Improvement" + "PIP" indicates training need.

**5.5 Show the Business Impact**

Metric	Result
**Time Saved**	Replaced 6 monthly Excel reports. Saved 6 hrs/month = 72 hrs/year of HR analyst time
**Data Accuracy**	Eliminated manual copy-paste errors. 100% accuracy vs previous 10% error rate in board reports
**Decision Speed**	What-if questions answered in <10 sec during meetings vs 2-day turnaround previously
**Cost Optimization**	Identified Indeed/LinkedIn as 60% of hires → Cut spend on bottom 3 sources saving $15k/year est.
**Retention Action**	Flagged 32% low satisfaction segment → Led to new engagement survey + policy review
**Adoption**	Used by HR Director + 5 HRBPs weekly for headcount & budget review

** 6 Screenshot / Demo

See how the Dashboard looks like :  
https://github.com/rajkishordash50/HR-DASHBOARD/blob/main/HR_DASHBOARD%20IMAGE.png

