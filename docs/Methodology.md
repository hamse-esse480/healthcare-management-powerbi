# Methodology

## 1. Project Objective

The project was developed to analyze healthcare-management activity across patients, doctors, appointments, treatments, and billing.

The dashboard focuses on service utilization and operational/financial reporting.

## 2. Data Preparation

The analytical model uses cleaned tables:

- `cleaned_patients`
- `cleaned_doctors`
- `cleaned_appointments`
- `cleaned_treatments`
- `cleaned_billing`

A separate `DateTable` supports monthly analysis.

## 3. Data Modeling

The model connects healthcare entities around common identifiers such as:

- Patient ID
- Doctor ID
- Appointment ID
- Treatment ID
- Dates

The report uses patient, doctor, appointment, treatment, billing, and date entities together to support cross-domain analysis.

## 4. Analytical Layer

The report contains a dedicated measure table named `Descriptive Analys`.

The main measures exposed by the report are:

- Total Patients
- Total Doctors
- Total Appointments
- Total Treatments
- Total Bills
- Total Revenue
- Average Bill
- Revenue by Treatment

These measures provide reusable calculations for KPI cards, charts, tooltips, and drillthrough analysis.

## 5. Descriptive Analysis

The dashboard analyzes:

### Patient utilization
- Number of patients
- Age groups
- Gender
- Insurance provider
- Registration activity

### Appointment utilization
- Appointment volume
- Appointment status
- Monthly activity
- Doctor association

### Treatment utilization
- Treatment volume
- Treatment type
- Doctor-level treatment activity
- Patient-level treatment activity
- Monthly treatment activity

### Financial activity
- Total revenue
- Average bill
- Total bills
- Revenue by treatment
- Revenue by payment status
- Monthly revenue

## 6. Visualization Strategy

Different visual types are used for different analytical purposes:

| Visual | Purpose |
|---|---|
| KPI/Card | High-level totals |
| Line chart | Monthly trends |
| Bar chart | Provider/category comparison |
| Column chart | Category and time comparison |
| Donut chart | Composition/distribution |
| Table | Record-level detail |
| Slicer | Interactive filtering |
| Drillthrough | Record-level investigation |

## 7. Interactivity

The dashboard uses slicers and drillthrough pages to support progressive analysis.

A typical workflow is:

```text
Executive Overview
        ↓
Patient / Doctor / Treatment / Billing Analysis
        ↓
Select a category or record
        ↓
Drillthrough
        ↓
Patient Details / Doctor Details
```

This allows the user to move from summary KPIs to underlying operational details.

## 8. Interpretation Approach

The dashboard should be interpreted as a descriptive healthcare-management analytics product.

It can identify:

- utilization patterns
- workload patterns
- treatment distributions
- billing patterns
- monthly changes
- patient/provider-level differences

It should not be interpreted as causal clinical evidence unless an appropriate epidemiological/statistical study design is added.

## 9. Reproducibility

The repository includes:

- PBIX report
- Data dictionary
- Data-quality documentation
- Methodology
- DAX measure documentation
- Key findings

This makes the analytical workflow easier for another analyst or recruiter to review.

## 10. Limitations

The report definition does not expose the full Power Query transformation history or the exact internal DAX expressions for every measure. Therefore, this documentation distinguishes between confirmed report structure and documented analytical intent.

For a fully reproducible portfolio repository, the next upgrade would be to export:

- Power Query M scripts
- Exact DAX expressions
- Data-quality statistics
- Source-data description
- Relationship/cardinality diagram
