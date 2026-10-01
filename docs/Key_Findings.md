# Key Findings

## Scope

This file documents the analytical findings that can be supported from the structure and analytical questions embedded in the PBIX report.

The report definition does not expose the rendered numeric values of every visual. Therefore, exact percentages, counts, and monetary values are intentionally not invented here.

## Finding 1 — The dashboard integrates multiple healthcare-management domains

The report combines:

- patients
- doctors
- appointments
- treatments
- billing
- dates

This enables analysis across both service utilization and financial activity.

## Finding 2 — Healthcare utilization is analyzed at multiple levels

The report supports analysis from:

```text
Overall system
   ↓
Patient / doctor / treatment category
   ↓
Individual patient or doctor
   ↓
Detailed appointment / treatment / billing records
```

This is supported by summary pages, drillthrough pages, and detailed tables.

## Finding 3 — Patient characteristics are part of service-utilization analysis

The Patient & Appointment Analysis page uses:

- Age Group
- Gender
- Insurance Provider
- Appointment Status
- Hospital Branch
- Monthly analysis

This allows healthcare activity to be examined alongside patient characteristics.

## Finding 4 — Provider activity is explicitly analyzed

Doctor-level analysis includes:

- Doctor
- Specialization
- Years of experience
- Patients served
- Appointments
- Treatments
- Revenue

The Doctor Details page is designed for provider-level drillthrough.

## Finding 5 — Treatment utilization is a major analytical component

The Treatment Analysis page examines:

- Total Treatments
- Treatment Type
- Treatments by Doctor
- Treatments by Patient
- Monthly Treatment Activity

This supports understanding of service mix and treatment workload.

## Finding 6 — Financial performance is linked to service activity

The Billing & Revenue page connects financial indicators with healthcare activity through:

- Total Revenue
- Total Bills
- Average Bill
- Revenue by Treatment
- Revenue by Patient
- Revenue by Payment Status
- Monthly Revenue

This allows financial analysis to be viewed alongside treatment and patient activity.

## Finding 7 — Time trends are built into the model

The `DateTable` and `Month` field are used across multiple visuals, including:

- monthly revenue
- monthly treatments
- monthly appointments

This provides a consistent time-analysis layer.

## Numeric Findings to Add From the Live Dashboard

For a final portfolio README, record the actual dashboard values for:

| KPI | Value |
|---|---:|
| Total Patients | Read from PBIX |
| Total Doctors | Read from PBIX |
| Total Appointments | Read from PBIX |
| Total Treatments | Read from PBIX |
| Total Bills | Read from PBIX |
| Total Revenue | Read from PBIX |
| Average Bill | Read from PBIX |

## Why Exact Values Are Not Guessed

A professional portfolio should distinguish between:

- what the model actually calculates,
- what the visual displays,
- and what can be verified from the source data.

The PBIX structure confirms the measures and analytical fields, but the static report-definition files do not provide every rendered result. Exact numeric findings should therefore be copied from the live dashboard rather than estimated.
