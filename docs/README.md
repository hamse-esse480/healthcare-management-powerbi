# Healthcare Management & Service Utilization Dashboard

A Power BI portfolio project for analyzing healthcare service utilization, patient activity, treatment delivery, doctor workload, appointments, billing, and revenue.

## Project Overview

This project transforms a cleaned healthcare-management dataset into an interactive Power BI dashboard designed for operational and analytical reporting.

The report is organized around seven pages:

1. **Executive Overview** — overall healthcare activity and financial picture.
2. **Patient & Appointment Analysis** — patient characteristics and healthcare-service utilization.
3. **Treatment Analysis** — treatments delivered and provider-level treatment activity.
4. **Billing & Revenue** — billing activity, payment status, treatment-level revenue, and monthly revenue.
5. **Doctor Details** — doctor-level workload, appointments, treatments, patients, and revenue.
6. **Patient Details** — patient-level appointments, treatments, billing, demographics, and revenue.
7. **Details** — detailed billing and treatment tables with doctor filters.

The report also uses drillthrough navigation to move from summary analysis to doctor- and patient-level detail.

## Business / Healthcare Questions Addressed

- What is the overall volume of patients, appointments, treatments, doctors, and billing activity?
- How is healthcare utilization distributed across patient groups?
- How are appointments distributed by status?
- Which treatment types are being delivered?
- How are treatments distributed across doctors?
- How does revenue change over time?
- How does revenue vary by treatment type and payment status?
- What patient and doctor details are associated with individual records?

## Data Model

The PBIX contains the following model entities identified from the report definition:

| Entity | Role |
|---|---|
| `cleaned_patients` | Patient demographic and registration information |
| `cleaned_doctors` | Doctor/provider information |
| `cleaned_appointments` | Appointment/service-use records |
| `cleaned_treatments` | Treatment records |
| `cleaned_billing` | Billing and payment records |
| `DateTable` | Date/month analysis |
| `Descriptive Analys` | DAX measures / analytical measures |

The model is designed around connected patient, doctor, appointment, treatment, and billing information, with a dedicated date table supporting time-based analysis.

## Key Measures Used

- Total Patients
- Total Doctors
- Total Appointments
- Total Treatments
- Total Bills
- Total Revenue
- Average Bill
- Revenue by Treatment

See [`DAX_Measures.md`](DAX_Measures.md) for the documented measure logic and implementation notes.

## Dashboard Pages

### 1. Executive Overview
Focuses on high-level KPIs and monthly trends.

Key elements:
- Total Patients
- Total Doctors
- Total Appointments
- Total Revenue
- Monthly revenue
- Monthly treatment activity
- Doctor-level activity
- Hospital branch and appointment-status filters

### 2. Patient & Appointment Analysis
Explores:
- Patient age groups
- Gender distribution
- Appointment status
- Monthly activity
- Hospital branch
- Patient and service utilization measures

### 3. Treatment Analysis
Explores:
- Total treatments
- Treatment types
- Treatments by doctor
- Treatment activity by patient
- Monthly treatment activity
- Hospital branch filtering

### 4. Billing & Revenue
Explores:
- Total revenue
- Total bills
- Average bill
- Revenue by month
- Revenue by treatment type
- Revenue by patient
- Revenue by payment status
- Hospital branch and month filters

### 5. Doctor Details
Provides drillthrough-level analysis for selected doctors:
- Patients served
- Appointments
- Treatments
- Revenue
- Appointment history
- Treatment distribution
- Doctor information

### 6. Patient Details
Provides drillthrough-level analysis for selected patients:
- Demographics
- Age group
- Appointments
- Treatments
- Billing records
- Payment status
- Revenue

### 7. Details
Provides detailed tables for billing and treatment records, with doctor-based filtering.

## Interactivity

The report uses:

- Slicers
- Drillthrough
- Cross-filtering
- KPI cards
- Line charts
- Column charts
- Bar charts
- Donut chart
- Detailed tables

Drillthrough fields include patient ID, doctor ID, and selected analytical measures.

## Data Quality

The source model uses tables prefixed with `cleaned_`, indicating that the analytical model is based on cleaned versions of the source entities.

The documentation in [`Data_Quality.md`](Data_Quality.md) separates confirmed model structure from recommended validation checks so that no unsupported data-quality claim is presented as a measured result.

## Methodology

The analytical workflow is documented in [`Methodology.md`](Methodology.md), covering:

1. Data preparation
2. Data-model organization
3. Date analysis
4. DAX measure development
5. Descriptive analysis
6. Interactive visualization
7. Drillthrough analysis
8. Interpretation

## Key Findings

[`Key_Findings.md`](Key_Findings.md) documents the findings that can be supported directly by the report design and identifies where exact numeric findings should be read from the interactive PBIX rather than guessed from the static report definition.

## Repository Structure

```text
Healthcare-Management-PowerBI/
│
├── Health_Care_Management.pbix
├── README.md
├── Data_Dictionary.md
├── Data_Quality.md
├── Methodology.md
├── DAX_Measures.md
└── Key_Findings.md
```

## Tools & Skills Demonstrated

- Microsoft Power BI
- Power Query / data preparation
- Data modeling
- Relationships and filtering
- DAX measures
- Date-table analysis
- KPI design
- Interactive dashboards
- Drillthrough
- Healthcare service-utilization analysis
- Revenue and billing analysis
- Data documentation

## Portfolio Note

This project demonstrates the ability to move from a cleaned relational healthcare dataset to a documented, interactive analytical product rather than presenting charts alone.

> **Important:** Numeric findings should be reported from the live PBIX/dashboard state. The documentation intentionally avoids inventing values that are not exposed in the report definition.
