# Data Quality

## Purpose

This document records the data-quality approach for the Healthcare Management Power BI project.

The PBIX uses cleaned analytical tables:

- `cleaned_patients`
- `cleaned_doctors`
- `cleaned_appointments`
- `cleaned_treatments`
- `cleaned_billing`

## Confirmed From the PBIX

The report uses:

- Patient IDs
- Doctor IDs
- Appointment IDs
- Treatment IDs
- Bill IDs
- Appointment dates
- Treatment dates
- Bill dates
- Patient demographic fields
- Doctor/provider fields
- Payment fields
- Treatment categories
- A dedicated `DateTable`

These fields are actively used in visuals, slicers, tables, measures, and drillthrough pages.

## Quality Checks

For a production analytical workflow, the following checks should be performed before publication:

### 1. Missingness

Check for blank values in:

- Patient identifiers
- Doctor identifiers
- Appointment identifiers
- Treatment identifiers
- Bill identifiers
- Dates
- Treatment type
- Appointment status
- Payment status
- Billing amount

### 2. Duplicate Keys

Validate uniqueness where the model expects a unique identifier:

- `patient_id`
- `doctor_id`
- `appointment_id`
- `treatment_id`
- `bill_id`

### 3. Referential Integrity

Check that:

- Every appointment references a valid patient.
- Every appointment references a valid doctor.
- Every treatment references a valid appointment.
- Every billing record references a valid treatment.
- Date fields connect correctly to the date-analysis logic.

### 4. Numeric Validation

Check:

- Billing amount is numeric.
- Billing amount is not unexpectedly negative.
- Age values are within a plausible range.
- Years of experience are non-negative.
- Counts and totals reconcile between tables and measures.

### 5. Category Consistency

Review:

- Gender categories
- Appointment status categories
- Payment status categories
- Payment methods
- Treatment types
- Doctor specializations
- Hospital branches

### 6. Date Validation

Check:

- Appointment dates
- Treatment dates
- Bill dates
- Patient registration dates
- DateTable coverage
- Month sorting and chronological order

## Interpretation of the `cleaned_` Prefix

The use of `cleaned_` table names indicates that the report is intentionally built on cleaned analytical tables. However, the report definition alone does not expose a complete audit log of every transformation or every row-level quality result.

Therefore, this repository does **not** claim specific percentages of missing data, duplicates, or invalid records unless those statistics are explicitly calculated and documented.

## Recommended Portfolio Upgrade

For an even stronger portfolio version, add a small Power Query/data-quality summary containing:

- Row count by table
- Missing-value count
- Duplicate-key count
- Invalid-date count
- Invalid numeric-value count
- Referential-integrity exceptions

That would turn the quality section from a methodology description into a reproducible data-quality audit.
