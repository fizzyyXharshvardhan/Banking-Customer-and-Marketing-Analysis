📊 Banking Customer & Marketing Analytics
Power BI Dashboard Project | GitHub README
A Microsoft Power BI project exploring customer demographics, account balances, loan indicators, and term-deposit marketing campaign outcomes using the UCI Bank Marketing dataset.
⚠️ Data validation note: The original bank-full.csv dataset contains 45,211 records. The current Power BI model was showing approximately 4,521 rows. Check the source file and Power Query filters before publishing final KPI values.
🎯 Project Overview
Banks can use customer and campaign data to understand their customer base and evaluate marketing performance. This interactive report presents customer characteristics and campaign outcomes.
📌 Scope note: The UCI Bank Marketing dataset focuses on direct-marketing campaigns for term-deposit subscriptions. It is not a complete banking transaction dataset.
📄 Dashboard Pages
1. Banking Customer & Marketing Overview
• High-level customer and campaign KPIs
• Customer distribution by age group and job
• Account balance group analysis
• Term-deposit subscription status
• Interactive slicers for exploration
2. Customer Analytics
• Customer demographics by age, education, marital status, and occupation
• Housing-loan indicators across customer groups
• Customer segmentation for exploratory analysis
3. Financial & Banking Analytics
• Account balance analysis
• Housing and personal loan indicators
• Campaign contact analysis
• Previous campaign outcome analysis
🛠️ Tools & Technologies
• Microsoft Power BI Desktop — report building and visualization
• Power Query — data cleaning and transformation
• DAX — measures and calculated columns
• CSV — source data format
🗂️ Dataset
Source: UCI Machine Learning Repository — Bank Marketing
https://archive.ics.uci.edu/dataset/222/bank+marketing
The dataset contains information about customers contacted during a bank's direct-marketing campaign. Common fields include age, job, marital status, education, account balance, housing loan, personal loan, contact method, campaign contacts, previous campaign outcome, and term-deposit subscription.
📎 If you redistribute the dataset with this project, follow the dataset's stated terms and attribution requirements. You may link to the official source instead of committing the raw CSV to GitHub.
🧹 Data Preparation Workflow
• Import the CSV dataset into Power BI.
• Review column names and data types.
• Clean and transform data in Power Query.
• Create age groups and other useful categories where appropriate.
• Build DAX measures for customer counts, balances, campaign contacts, and subscription analysis.
• Create visuals and slicers for interactive exploration.
🧮 Suggested DAX Measures
These examples assume the table is named bank and the balance column is Accounting_balance. Adjust names to match the fields in your Power BI model.
Total Customers =
COUNTROWS(bank)

Total Account Balance =
SUM(bank[Accounting_balance])

Average Account Balance =
AVERAGE(bank[Accounting_balance])

Subscription Rate % =
DIVIDE(
    CALCULATE(
        COUNTROWS(bank),
        bank[Subscription Status] = "Subscribed"
    ),
    COUNTROWS(bank),
    0
)
💡 Format Subscription Rate % as Percentage in Power BI. Clear report slicers and verify the loaded row count before comparing results with the original dataset.
📁 Suggested Repository Structure
Banking-Customer-Analytics/
├── README.md
├── Dataset/
│   └── bank-full.csv                 # Optional; follow source terms
├── PowerBI/
│   └── Banking_Analytics.pbix
├── Screenshots/
│   ├── Executive_Overview.png
│   ├── Customer_Analytics.png
│   └── Financial_Analytics.png
└── Documentation/
    └── Project_Report.pdf            # Optional
🚀 How to Open the Project
• Download or clone this repository.
• Open PowerBI/Banking_Analytics.pbix in Microsoft Power BI Desktop.
• If Power BI asks for the source CSV path, point it to the dataset file on your computer.
• Select Home → Transform data and verify the source file and row count.
• Select Close & Apply, then refresh the report.
• Clear slicers to review unfiltered KPIs.
🔎 Questions the Dashboard Can Explore
• Which customer age groups are most represented?
• How do job, education, and marital status vary across customers?
• How do housing and personal loan indicators relate to subscription outcomes?
• How do previous campaign outcomes and contact frequency vary?
• How do account balances differ across customer segments?
📈 Add specific findings only after verifying the final data and report filters.
⚠️ Limitations
• The dataset concerns direct marketing for term deposits; it does not represent all banking activities.
• Campaign outcomes show associations and do not, by themselves, prove causation.
• Dashboard metrics can change when slicers or filters are applied.
• Validate the final row count and KPI values against the selected source file.
👨🎓 Author
Student Project | BBA Business Analytics
Babu Banarasi Das University, Lucknow, Uttar Pradesh, India
🙏 Acknowledgement
Dataset provided by the UCI Machine Learning Repository. Please refer to the official dataset page for source information and applicable terms:
https://archive.ics.uci.edu/dataset/222/bank+marketing
