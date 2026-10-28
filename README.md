<<<<<<< HEAD
# Insurance Risk & Claims Analysis Dashboard

An interactive **Power BI** dashboard that centralizes policyholder and claims data for an insurance company, giving stakeholders a single place to track performance, spot trends, and identify risk factors.


## Table of Contents

- [Business Problem](#business-problem)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Dashboard Overview](#dashboard-overview)
  - [KPIs](#kpis)
  - [Visualizations](#visualizations)
  - [Dynamic Measure Selector](#dynamic-measure-selector)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Tools & Techniques](#tools--techniques)
- [How to Use](#how-to-use)
- [Project Structure](#project-structure)

---

## Business Problem

An insurance company wants to better understand its **policyholder base** and **claim patterns** to make data-driven business decisions. Policy and claims data are currently scattered across multiple sources, making it difficult for stakeholders to track performance and identify trends.

## Objectives

- Consolidate policy and claims data into one **centralized, interactive dashboard**.
- Track headline KPIs on customer base size, claim cost, claim frequency, and claim severity.
- Go beyond KPIs to **visually explore patterns, relationships, and anomalies** across customer demographics, car details, and claim behaviours.
- Help stakeholders **identify risk factors, understand customer segments, and optimize policy decisions**.

## Dataset

| Item | Details |
|------|---------|
| Source | Excel file|
| Records | 37,542 policies |
| Currency | Ghana Cedi (GH₵) |
| Key fields | Gender, age group, education, marital status, kids driving, car use, car make, car year, coverage zone, claim amount, claim frequency |


---


## Dashboard Overview

### KPIs

| # | KPI | Purpose | Value |
|---|-----|---------|-------|
| 1 | **Total Policies** | Measures the size of the active customer base | 37,542 |
| 2 | **Total Claim Amount** | Tracks the overall financial impact of claims | GH₵188M |
| 3 | **Claim Frequency** | Analyses how often claims are made (average) | 0.5 |
| 4 | **Average Claim Amount** | Assesses claim severity and potential risk exposure | GH₵5.0K |
| 5 | **Gender-wise Total Policies** | Shows customer distribution across genders for segmentation | Male: 18.7K, Female: 18.8K |

### Visualizations

All visuals are built around two dynamic measures: **Total Claim Amount** and **Total Policies**.

| # | Visualization | Chart Type | Purpose |
|---|---------------|-----------|---------|
| 1 | By Car Use | Donut chart | Policy and claim distribution by how cars are used (Private / Commercial) |
| 2 | By Car Make | Bar chart | Identify which car brands have higher policies and claims (brand-based risk) |
| 3 | By Coverage Zone | Donut chart | Evaluate policies and claims by geographic zone for regional risk analysis |
| 4 | By Age Group | Column chart / histogram | Assess policyholder age distribution and which age brackets claim more |
| 5 | By Car Year | Area chart | Analyse how the car's year of manufacture affects policy counts and claims |
| 6 | By Kids Driving | Ribbon chart | Compare the impact of young drivers in the household |
| 7 | By Education | Pie chart | Understand how education level relates to policy adoption and claims |
| 8 | By Education & Marital Status | Matrix heat grid | Explore the combined effect of education and marital status on customer profiles |

### Dynamic Measure Selector

A **"Select measure"** slicer at the top right lets users switch every chart between **Total Claims** and **Total Policies**, so the same layout answers both "where are the claims coming from?" and "where are the customers?"

---

## Key Insights

_Based on the Total Claims view of the dashboard._

- **Overall:** 37,542 policies generated **GH₵188M** in claims, with an average claim of about **GH₵5.0K** and an average claim frequency of **0.5**.
- **Car use:** **Private** vehicles account for the bulk of claims (GH₵150M, ~80%) versus Commercial (GH₵37M).
- **Car make:** **Ford (GH₵16.6M)** and **Chevrolet (GH₵14.8M)** lead in claims, followed by Dodge (GH₵9.3M), Toyota (GH₵9.0M), and GMC (GH₵8.7M).
- **Coverage zone:** Claims are spread almost evenly across Urban (GH₵38M), Suburban, Rural, Highly Rural, and Highly Urban (about GH₵37M each), so geography alone is not a strong differentiator.
- **Age group:** Claims are fairly flat from ages 26–65 (about GH₵35–36M per bracket). The **15–25** group has the lowest total (GH₵17M) and **66–75** is lower (GH₵29M).
- **Car year:** Claims rise sharply for cars manufactured from about **1999 onward**, plateauing around GH₵8–9M per model year, with a peak near GH₵9.7M. Pre-1999 vehicles contribute far less. The drop at 2020 likely reflects incomplete data for the latest model year.
- **Kids driving:** Households with **0 kids driving** account for the largest share (GH₵134M), declining steeply with 1 (GH₵34M), 2 (GH₵16M), and 3 (GH₵4M).
- **Education:** **Bachelors** holders make up about **50%** of claims (GH₵94M), followed by **High School** at about **27.6%** (GH₵52M).
- **Education × marital status:** The **Single** group dominates across most education levels (e.g., GH₵38.7M for Bachelors, GH₵40.2M for High School), while Married Bachelors holders are the next largest segment (GH₵31.1M).
- **Gender:** The customer base is nearly balanced (Male 18.7K vs. Female 18.8K).

## Recommendations

- Review **pricing and underwriting** for the highest-claim car makes (Ford, Chevrolet).
- Target **marketing and retention** at the Single, Bachelors/High School segments, which drive the most volume.
- Investigate why **newer vehicles (post-1999)** show consistently higher claims, and validate the 2020 drop against data completeness.
- Since gender and coverage zone are evenly distributed, focus segmentation on **vehicle, education, and household** factors.


---

## Tools & Techniques

- **Power BI Desktop** for data modelling and dashboard design
- **Power Query** for data cleaning and transformation
- **DAX** for measures (Total Policies, Total Claim Amount, Average Claim Amount, Claim Frequency)
- **Field parameters / disconnected table** for the dynamic measure selector
- Custom dark theme with teal accents and glow-bordered cards

## How to Use

2. Open `Insurance_Risk_Claims_Analysis.pbix` in **Power BI Desktop**.
3. Use the **Select measure** dropdown to toggle between *Total Claims* and *Total Policies*.
4. Click any chart element (a car make, age bracket, zone, etc.) to **cross-filter** the rest of the dashboard.
5. Hover over visuals for tooltips with exact values.

