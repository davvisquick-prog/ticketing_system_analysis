# IT Service Desk Ticketing System | Funnel Analysis

**Tools:** SQL (MySQL Workbench) · Python (ETL Pipeline) · Tableau · Excel  
**Domain:** IT Service Management | Help Desk Operations  
**Data:** Synthetic dataset modeled after real IT service desk ticketing structures

---

## The Problem

IT service desks handle hundreds of support requests daily, but without visibility into ticket flow and resolution patterns, teams face slow response times, growing backlogs, and poor end-user satisfaction.

This project answers one core question: **Where are tickets getting stuck, and why?**

---

## Key Findings

- Tickets stall most frequently at the escalation stage — the biggest bottleneck in the support pipeline
- A significant gap exists between assigned licenses and active users across several software tools
- Peak volume periods reveal clear staffing mismatches that contribute to backlog buildup
- Agent-level performance varies considerably, pointing to training and workload distribution opportunities

---

## Questions Answered

| # | Question | Approach |
|---|----------|----------|
| 1 | What are the most common ticket categories? | Aggregated ticket volume by category and priority level |
| 2 | What is the average resolution time by priority and category? | Calculated mean resolution time across ticket segments |
| 3 | Where do tickets get stuck in the pipeline? | Built funnel analysis to quantify stall points at each stage |
| 4 | Which agents have the highest and lowest resolution rates? | Compared agent throughput and resolution metrics |
| 5 | How do ticket volumes and resolution times trend over time? | Month-over-month trend analysis across all ticket types |

---

## Workflow

**1. ETL Pipeline (Python)**  
Built an automated pipeline to extract raw ticketing data, transform and standardize fields, and load a clean, analysis-ready dataset — removing duplicates, resolving missing timestamps, and normalizing categories.

**2. Data Cleaning & Validation (SQL)**  
Standardized ticket categories, corrected inconsistent timestamp fields, and validated records for accurate aggregation.

**3. Data Modeling (SQL)**  
Structured ticket lifecycle data by mapping each ticket's journey from creation through assignment, escalation, and resolution.

**4. Metric Development (SQL)**  
Built KPIs including average resolution time, first-response time, SLA compliance rate, ticket backlog volume, and agent throughput.

**5. Funnel Analysis**  
Quantified drop-off and stall points at each pipeline stage to reveal where tickets accumulate without action.

**6. Visualization & Storytelling (Tableau)**  
Dashboards surface resolution trends, category breakdowns, priority distributions, and agent performance comparisons.

---

## Dashboards

> 📊 [View on Tableau Public](https://public.tableau.com/views/ITServiceDeskAnalytics/FromTicketstoInsightsITServiceDeskAnalytics?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
---

## Recommendations

- Implement tiered routing rules to auto-assign tickets by category and priority
- Establish clearer escalation criteria and SLA thresholds to address the escalation bottleneck
- Increase staffing during peak volume periods identified through trend analysis
- Introduce regular agent performance reviews using dashboard metrics
- Automate follow-up workflows for tickets exceeding target resolution times

---

## About the Data

This project uses a synthetically generated dataset designed to mirror real IT service desk operations. All ticket records, agent names, and resolution data are simulated to demonstrate end-to-end analytical and engineering workflow.
