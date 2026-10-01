# DAX Measures

The PBIX report references a dedicated measure table named `Descriptive Analys`.

The report definition confirms the following measures. Because the internal compressed Power BI model does not expose every original DAX expression in readable form, the formulas below are documented semantic equivalents based on the fields used by the report. They should be checked against the Measures pane in Power BI before being presented as the original source code.

## 1. Total Patients

**Purpose:** Count unique patients.

```DAX
Total Patients =
DISTINCTCOUNT ( cleaned_patients[patient_id] )
```

## 2. Total Doctors

**Purpose:** Count unique doctors/providers.

```DAX
Total Doctors =
DISTINCTCOUNT ( cleaned_doctors[doctor_id] )
```

## 3. Total Appointments

**Purpose:** Count appointment records.

```DAX
Total Appointments =
COUNTROWS ( cleaned_appointments )
```

## 4. Total Treatments

**Purpose:** Count treatment records.

```DAX
Total Treatments =
COUNTROWS ( cleaned_treatments )
```

## 5. Total Bills

**Purpose:** Count billing records.

```DAX
Total Bills =
COUNTROWS ( cleaned_billing )
```

## 6. Total Revenue

**Purpose:** Sum billing amounts.

```DAX
Total Revenue =
SUM ( cleaned_billing[amount] )
```

## 7. Average Bill

**Purpose:** Calculate the average billing amount.

```DAX
Average Bill =
AVERAGE ( cleaned_billing[amount] )
```

## 8. Revenue by Treatment

**Purpose:** Show revenue in the current treatment/filter context.

A semantic implementation is:

```DAX
Revenue by Treatment =
[Total Revenue]
```

When `treatment_type` is placed on a visual axis, filter context evaluates revenue separately for each treatment type.

## Measure Design Principles

The project uses measures rather than hard-coded values so that KPIs and charts respond to:

- Hospital branch
- Month
- Gender
- Appointment status
- Doctor
- Patient
- Treatment type
- Other report filters

## Important Validation Note

The measure names above are directly confirmed from the report definition. The exact original DAX expressions are not reproduced where the compressed model did not expose them as readable source text.

Before publishing the DAX code as the project's exact source code, open the PBIX and verify each measure in:

**Model view → `Descriptive Analys` → Measures**

This distinction keeps the GitHub documentation technically honest.
