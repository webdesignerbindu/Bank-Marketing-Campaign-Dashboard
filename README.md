# Bank-Marketing-Campaign-Dashboard
This repository contains a Power BI dashboard and a PDF report analysing a bank’s marketing campaign.  
The goal is to identify high‑performing customer segments, evaluate campaign efficiency, and recommend strategies to improve future marketing efforts.

---

## 📁 Repository Contents

📄 dashboard.pbix     → Power BI file
📄 dashboard.pdf      → Final report (exported as PDF)
📄 README.md          → Project documentation
📁 images/            → Dashboard screenshots (optional)


---

## Project Overview

The dashboard visualises customer demographics, contact history, and subscription outcomes to help the bank:

- Understand campaign performance  
- Identify high‑conversion customer segments  
- Optimise contact strategies  
- Improve marketing ROI  

This project demonstrates end‑to‑end analytics skills using Power BI, DAX, and data storytelling.

---

## Executive KPIs

The following KPIs were selected for executives because they reflect campaign **scale**, **success**, and **efficiency**:

- **Total Customers Contacted**
- **Total Subscribed**
- **Conversion Rate**
- **Avg Contacts per Customer**
- **Avg Contacts per Success**

These KPIs provide a high‑level view of campaign performance and resource utilisation.

---

## DAX Measures Used
Total Customers =
COUNTROWS('Bank Target Marketing')

Total Subscribed =
SUM('Bank Target Marketing'[SubscribedFlag])

Conversion Rate =
DIVIDE(
    SUM('Bank Target Marketing'[SubscribedFlag]),
    COUNTROWS('Bank Target Marketing')
)

Avg Contacts per Customer =
AVERAGE('Bank Target Marketing'[campaign])

Avg Contacts per Success =
VAR SubscribedRows =
    FILTER(
        'Bank Target Marketing',
        'Bank Target Marketing'[SubscribedFlag] = 1
    )
RETURN
    AVERAGEX(
        SubscribedRows,
        'Bank Target Marketing'[campaign]
    )

## Customer Segment Insights
Conversion Rate by Age Group
60+ age group converts the highest
Younger customers (18–29) also respond well

Conversion Rate by Education
The tertiary education group performs best

Conversion Rate by Job
Students and retirees' roles convert strongly

Conversion Rate by Contact Method
Cellular contact is the most effective channel

## Recommended Target Segment
Primary: Age 60+

Secondary: Students & Retirees

Best Contact Channel: Cellular

These segments deliver the strongest conversion rates and require fewer contact attempts.

## Recommendations
Focus on high‑conversion age groups

Prioritise cellular outreach

Reduce repeated contact attempts

Personalize messaging

Improve data quality

Dashboard Preview

📂 How to Use
Download the .pbix file

Open in Power BI Desktop

Explore the interactive visuals and filters

## screenshots of the dashboard:
<img width="1016" height="580" alt="kpi" src="https://github.com/user-attachments/assets/96f6de42-4510-4dbe-b9ac-6f5372fa6be9" />

<img width="974" height="558" alt="segment" src="https://github.com/user-attachments/assets/97ba1d6b-052d-44e2-b45d-207ccea74901" />

👩‍💻 Author
Bindu Lokesh  
