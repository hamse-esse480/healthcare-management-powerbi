# Data Dictionary

This dictionary documents the fields that are exposed by the Power BI report definition through visuals, slicers, drillthrough filters, and analytical measures.

## `cleaned_patients`

Patient-level information.

| Field | Role / Meaning |
|---|---|
| `patient_id` | Unique patient identifier used for drillthrough and patient analysis |
| `first_name` | Patient first name used in patient-level analysis |
| `gender` | Patient gender |
| `Age` | Patient age |
| `Age Group` | Derived age-group category used in dashboard analysis |
| `date_of_birth` | Patient date of birth |
| `registration_date` | Patient registration date |
| `insurance_provider` | Patient insurance provider |

## `cleaned_doctors`

Doctor/provider information.

| Field | Role / Meaning |
|---|---|
| `doctor_id` | Doctor identifier used for drillthrough |
| `first_name` | Doctor first name |
| `specialization` | Doctor specialization |
| `hospital_branch` | Hospital/branch associated with the doctor |
| `years_experience` | Doctor years of experience |

## `cleaned_appointments`

Appointment/service-use information.

| Field | Role / Meaning |
|---|---|
| `appointment_id` | Appointment identifier |
| `appointment_date` | Date of appointment |
| `patient_id` | Patient associated with appointment |
| `doctor_id` | Doctor associated with appointment |
| `status` | Appointment status |

## `cleaned_treatments`

Treatment/service information.

| Field | Role / Meaning |
|---|---|
| `treatment_id` | Treatment identifier |
| `appointment_id` | Appointment associated with treatment |
| `treatment_type` | Type/category of treatment |
| `treatment_date` | Date of treatment |
| `doctor_id` | Doctor associated with treatment |
| `patient_id` | Patient associated with treatment |

## `cleaned_billing`

Billing and payment information.

| Field | Role / Meaning |
|---|---|
| `bill_id` | Bill identifier |
| `patient_id` | Patient associated with bill |
| `treatment_id` | Treatment associated with bill |
| `payment_status` | Payment status |
| `payment_method` | Payment method |
| `bill_date` | Billing date |
| `amount` | Billing/revenue amount |

## `DateTable`

Dedicated time-analysis table.

| Field | Role / Meaning |
|---|---|
| `Month` | Month-level grouping used in monthly trend visuals |

## `Descriptive Analys`

Analytical measure table.

The report references these measures:

- `Total Patients`
- `Total Doctors`
- `Total Appointments`
- `Total Treatments`
- `Total Bills`
- `Total Revenue`
- `Average Bill`
- `Revenue by Treatment`

## Data Types

The exact underlying Power BI data types are not fully exposed through the report-definition JSON used for this documentation. Therefore, this dictionary documents semantic roles rather than guessing storage types.

## Modeling Note

Identifiers such as patient ID, doctor ID, appointment ID, treatment ID, and bill ID should be treated as keys/identifiers rather than continuous analytical measures.
