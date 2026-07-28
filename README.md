# Prism Insurance Analytics Dashboard

[![Power BI](https://img.shields.io/badge/Power_BI-Desktop-yellow.svg)](https://powerbi.microsoft.com/)
[![Power Query](https://img.shields.io/badge/Power_Query-ETL-orange.svg)](https://docs.microsoft.com/en-us/power-query/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An end-to-end business intelligence and data visualization project developed for **Prism Insurance Pvt. Ltd.** The solution focuses on robust data cleaning and transformation entirely within **Power Query**, structuring clean datasets to analyze policyholder demographics, premium revenue distributions, coverage limits, and claim lifecycle statuses across diverse insurance lines.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Dashboard Visual Preview](#dashboard-visual-preview)
- [Dataset Schema & Features](#dataset-schema--features)
- [ETL & Data Transformation (Power Query)](#etl--data-transformation-power-query)
- [Key Performance Indicators (KPIs)](#key-performance-indicators-kpis)
- [Visualizations & Key Insights](#visualizations--key-insights)
- [Installation & Usage](#installation--usage)
- [Project Structure](#project-structure)
- [Author](#author)

---

## Project Overview
Insurance institutions manage extensive volumes of transactional data spanning customer policies, risk coverage limits, and claim payouts. This project establishes an interactive Power BI reporting dashboard designed to give stakeholders deep visibility into core financial metrics, portfolio distribution across insurance types (Travel, Health, Auto, Life, and Home), and claims performance (Rejected, Settled, and Pending).

---

## Dashboard Visual Preview

The dashboard is structured into an executive dark-themed layout featuring clean card visuals, horizontal and area distribution charts, demographic breakdowns, and detailed matrices:
- **Top Summary Cards:** Aggregated metrics for **Premium Amount** (5.97M), **Coverage Amount** (600.33M), and **Claim Amount** (16.90M).
- **Global Slicers:** Interactive filtering capabilities by `PolicyNumber`, `ClaimNumber`, and `CustomerID`.
- **Demographic Breakdown:** Gender split tracking active policy distributions (Female: 5K, Male: 5K).
- **Policy Distribution:** Bar chart ranking premium performance across Travel (2.5M), Health (1.2M), Auto (1.0M), Life (0.7M), and Home (0.6M).
- **Policy Status Split:** Donut chart illustrating active (5.81K / 58.11%) versus inactive (4.19K / 41.89%) policies.
- **Claims Analytics:** Area chart tracking claim volumes by status (Rejected: 4.4K, Settled: 3.4K, Pending: 2.3K) alongside age-group exposure trends (Adult: 8.8M, Elder: 6.4M, Young Adult: 1.7M) and a comprehensive matrix detailing claim amounts across policy types and statuses.

---

## Dataset Schema & Features
The underlying dataset consists of structured policy records containing the following fields:
- **Identifiers:** `PolicyNumber`, `CustomerID`, `ClaimNumber`
- **Demographics:** `Age`, `Gender`
- **Policy Metadata:** `PolicyType` (Auto, Travel, Health, Home, Life), `PolicyStartDate`, `PolicyEndDate`
- **Financial Metrics:** `PremiumAmount`, `CoverageAmount`, `ClaimAmount`
- **Claims Tracking:** `ClaimStatus` (Rejected, Settled, Pending), `ClaimDate`

---

## ETL & Data Transformation (Power Query)
Data preparation and modeling were performed entirely within **Power Query** without utilizing DAX measures, ensuring optimal query performance and data integrity prior to visualization:
- **Data Type Casting:** Standardized numerical fields (`PremiumAmount`, `CoverageAmount`, `ClaimAmount`) and correctly formatted date fields (`PolicyStartDate`, `PolicyEndDate`, `ClaimDate`).
- **Data Cleaning & Handling Missing Values:** Managed null or missing claim dates corresponding to unfiled or rejected claims.
- **Conditional Column Generation:** Created calculated columns for age segmentation (`Adult`, `Elder`, `Young Adult`) and active/inactive status classification directly within Power Query steps.

---

## Key Performance Indicators (KPIs)
- **Total Premium Revenue:** 5.97M across all active and historical policies.
- **Total Coverage Exposure:** 600.33M in underwritten risk coverage.
- **Total Claim Volume:** 16.90M processed across claim categories.
- **Active Policy Ratio:** 58.11% active policies versus 48.89% inactive policies.

---

## Visualizations & Key Insights
* **Dominant Insurance Lines:** Travel insurance leads total premium revenue generation (2.5M), followed by Health (1.2M) and Auto (1.0M).
* **Claims Status Distribution:** Rejected claims account for the highest volume (4.4K), followed by Settled (3.4K) and Pending (2.3K).
* **Age-Group Risk Exposure:** Adult policyholders represent the highest claim financial exposure (8.8M), compared to Elder (6.4M) and Young Adult (1.7M) segments.

---

## Installation & Usage

To explore or run this project locally:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/prism-insurance-analytics.git](https://github.com/your-username/prism-insurance-analytics.git)

   Open the Power BI Dashboard:

        - Download and open the .pbix file using Power BI Desktop.

Review Power Query Steps:

       - Open the Power Query Editor to inspect the applied data transformation steps, custom columns, and schema mappings.

Project Structure

prism-insurance-analytics/
│
├── data/                    # Cleaned dataset source files
├── dashboard/               # Power BI .pbix dashboard file
├── images/                  # Dashboard screenshots and visual exports
├── README.md                # Project documentation
└── LICENSE                  # MIT License
