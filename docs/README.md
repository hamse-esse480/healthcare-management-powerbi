# Healthcare Management & Service Utilization Dashboard

An interactive **Power BI portfolio project** for analyzing healthcare service utilization, patient activity, treatment delivery, doctor workload, appointments, billing, and revenue.

The project demonstrates how a cleaned healthcare-management dataset can be transformed into an interactive analytical product using **Power BI, Power Query, data modeling, DAX, and interactive dashboard design**.

---

## Project Overview

This project transforms a cleaned healthcare-management dataset into an interactive Power BI dashboard designed for healthcare operational and analytical reporting.

The report integrates patient, doctor, appointment, treatment, and billing information into a connected analytical model.

The dashboard is organized into seven pages:

1. **Executive Overview** — overall healthcare activity and financial picture.
2. **Patient & Appointment Analysis** — patient characteristics and healthcare-service utilization.
3. **Treatment Analysis** — treatment activity and provider-level treatment patterns.
4. **Billing & Revenue** — billing activity, payment status, treatment-level revenue, and monthly revenue.
5. **Doctor Details** — doctor-level workload, appointments, treatments, patients, and revenue.
6. **Patient Details** — patient-level appointments, treatments, billing, demographics, and revenue.
7. **Details** — detailed billing and treatment records with doctor-based filtering.

The report also uses **drillthrough navigation** to move from summary-level analysis to doctor- and patient-level detail.

---

## Healthcare Analytics Questions

The dashboard was designed to answer questions such as:

* What is the overall volume of patients, appointments, treatments, doctors, and billing activity?
* How is healthcare utilization distributed across patient groups?
* How are appointments distributed by status?
* How does appointment activity vary by month?
* Which treatment types are most frequently delivered?
* How are treatments distributed across doctors?
* How does treatment activity vary over time?
* How does revenue change across months?
* How does revenue vary by treatment type and payment status?
* What patient and doctor information is associated with individual records?

---

## Data Model

The Power BI model contains the following entities:

| Entity                 | Role                                             |
| ---------------------- | ------------------------------------------------ |
| `cleaned_patients`     | Patient demographic and registration information |
| `cleaned_doctors`      | Doctor/provider information                      |
| `cleaned_appointments` | Appointment and service-utilization records      |
| `cleaned_treatments`   | Treatment records                                |
| `cleaned_billing`      | Billing and payment records                      |
| `DateTable`            | Date and time-based analysis                     |
| `Descriptive Analys`   | DAX measures / analytical measures               |

The model connects patient, doctor, appointment, treatment, and billing information, with a dedicated date table supporting monthly and time-based analysis.

---

## Key Measures

The dashboard uses analytical measures including:

* Total Patients
* Total Doctors
* Total Appointments
* Total Treatments
* Total Bills
* Total Revenue
* Average Bill
* Revenue by Treatment

Detailed measure definitions and implementation notes are available in:

**[DAX Measures Documentation →](docs/DAX_Measures.md)**

---

# Key Findings

The following findings are explicitly presented in the Power BI report and represent **descriptive results from the healthcare-management dataset**.

## 1. Patient & Appointment Analysis

### Appointment Pattern by Month

* **September recorded the highest share of appointments: 19.5%.**
* **February recorded the lowest share of appointments: 1.0%.**

This demonstrates substantial variation in appointment activity across months.

### Patient Age Distribution

* **Patients aged 30–44 represented the largest age group, accounting for 34% of patients.**

### Appointment Status

* **51.5% of appointments were classified as either no-show or cancelled.**

This indicates that more than half of the recorded appointments fell into these two non-completed categories.

---

## 2. Treatment Analysis

### Treatment Activity by Month

* **April had the highest share of treatments: 12.5%.**
* **September had the lowest share of treatments: 5.5%.**

### Treatment Type

* **Chemotherapy was the most common treatment type, accounting for 24.5% of treatments.**

### Doctor-Level Treatment Activity

* **Sarah provided the highest number of treatments, with 46 treatments.**

---

## 3. Billing & Revenue Analysis

### Overall Financial Activity

| Indicator         |      Result |
| ----------------- | ----------: |
| **Total Revenue** | **551.25K** |
| **Total Bills**   |     **200** |
| **Average Bill**  |   **2.76K** |

### Monthly Revenue

* Monthly revenue ranged from approximately **28K to 64K**.

### Revenue Dimensions

The dashboard provides additional revenue analysis by:

* Treatment type
* Payment status
* Patient
* Month

---

## 4. Executive Overview

The **Executive Overview** combines the main healthcare-management indicators into a single summary view.

It includes:

* Appointments by month
* Treatments by month
* Appointments by doctor
* Revenue by month
* Hospital branch activity
* High-level KPI indicators

This page provides a starting point for understanding overall healthcare activity before moving into more detailed analysis.

---

## 5. Doctor-Level Analysis

The **Doctor Details** page provides drillthrough analysis for individual doctors.

The analysis includes:

* Doctor profile
* Appointments by month
* Treatments by treatment type
* Appointment details
* Treatment analysis
* Appointment trends
* Patient-level information
* Doctor-related revenue

This allows provider-level activity to be explored beyond the summary dashboard.

---

## 6. Patient-Level Analysis

The **Patient Details** page provides drillthrough information for individual patients.

The analysis includes:

* Patient demographics
* Patient information
* Appointment history
* Treatment history
* Billing history
* Payment status
* Revenue associated with the patient

---

## Main Analytical Conclusions

The dashboard provides the following descriptive findings:

1. **Appointment activity varied strongly by month**, with September recording the highest share (19.5%) and February the lowest (1.0%).

2. **Patients aged 30–44 formed the largest patient age group**, representing 34% of patients.

3. **No-shows and cancellations accounted for 51.5% of appointments.**

4. **Treatment activity varied by month**, with April recording the highest share (12.5%) and September the lowest (5.5%).

5. **Chemotherapy was the most common treatment type**, representing 24.5% of treatments.

6. **Sarah recorded the highest treatment volume**, with 46 treatments.

7. **The healthcare system recorded 551.25K in total revenue across 200 bills**, with an average bill of 2.76K.

8. **Monthly revenue varied between approximately 28K and 64K.**

---

## Dashboard Pages

### 1. Executive Overview

Focuses on high-level healthcare and financial indicators.

**Key elements:**

* Total Patients
* Total Doctors
* Total Appointments
* Total Revenue
* Monthly Revenue
* Monthly Treatment Activity
* Doctor-Level Activity
* Hospital Branch
* Appointment Status

### 2. Patient & Appointment Analysis

Explores:

* Patient age groups
* Gender distribution
* Appointment status
* Monthly activity
* Hospital branch
* Patient and service-utilization measures

### 3. Treatment Analysis

Explores:

* Total treatments
* Treatment types
* Treatments by doctor
* Treatment activity by patient
* Monthly treatment activity
* Hospital branch filtering

### 4. Billing & Revenue

Explores:

* Total revenue
* Total bills
* Average bill
* Revenue by month
* Revenue by treatment type
* Revenue by patient
* Revenue by payment status
* Hospital branch and month filters

### 5. Doctor Details

Provides drillthrough-level analysis for selected doctors:

* Patients served
* Appointments
* Treatments
* Revenue
* Appointment history
* Treatment distribution
* Doctor information

### 6. Patient Details

Provides drillthrough-level analysis for selected patients:

* Demographics
* Age group
* Appointments
* Treatments
* Billing records
* Payment status
* Revenue

### 7. Details

Provides detailed billing and treatment tables with doctor-based filtering.

---

## Interactivity

The report uses several Power BI interactive features:

* Slicers
* Drillthrough
* Cross-filtering
* KPI cards
* Line charts
* Column charts
* Bar charts
* Donut charts
* Detailed tables

Drillthrough fields include **Patient ID**, **Doctor ID**, and selected analytical dimensions.

---

## Methodology

The analytical workflow followed these stages:

```text
Healthcare Dataset
        ↓
Data Preparation
        ↓
Data Model Organization
        ↓
Relationships & Date Table
        ↓
DAX Measure Development
        ↓
Descriptive Analysis
        ↓
Interactive Dashboard Design
        ↓
Drillthrough Analysis
        ↓
Findings & Interpretation
```

Detailed methodology is available in:

**[Methodology Documentation →](docs/Methodology.md)**

---

## Data Quality

The analytical model uses tables prefixed with `cleaned_`, indicating that the dashboard is built from cleaned versions of the source entities.

The data-quality documentation separates:

* Confirmed model structure
* Documented cleaning information
* Recommended validation checks

This approach avoids presenting unsupported data-quality claims as measured results.

**[View Data Quality Documentation →](docs/Data_Quality.md)**

---

## Data Dictionary

The data dictionary documents the variables and fields used within the healthcare-management dataset and explains their analytical roles.

**[View Data Dictionary →](docs/Data_Dictionary.md)**

---

## Tools & Skills Demonstrated

### Tools

* Microsoft Power BI
* Power Query
* DAX
* GitHub

### Technical Skills

* Data preparation
* Data cleaning
* Data modeling
* Relationships and filtering
* DAX measure development
* Date-table analysis
* KPI development
* Interactive dashboard design
* Drillthrough analysis
* Cross-filtering
* Healthcare service-utilization analysis
* Revenue and billing analysis
* Data documentation

---

## Portfolio Interpretation

This project demonstrates the ability to move from a cleaned relational healthcare dataset to a **documented, interactive analytical product** rather than presenting charts alone.

The analytical workflow connects:

```text
Healthcare System
       ↓
Patients & Appointments
       ↓
Treatment Utilization
       ↓
Doctor Workload
       ↓
Billing & Revenue
       ↓
Patient / Doctor Drillthrough
```

This structure demonstrates how healthcare data can be organized to support both **high-level monitoring** and **record-level exploration** within a single Power BI model.

---

## Repository Structure

```text
Healthcare-Management-PowerBI/
│
├── Health_Care_Management.pbix
├── README.md
│
└── docs/
    ├── Data_Dictionary.md
    ├── Data_Quality.md
    ├── Methodology.md
    ├── DAX_Measures.md
    └── Key_Findings.md
```

### Documentation

* **[Data Dictionary →](docs/Data_Dictionary.md)**
* **[Data Quality Assessment →](docs/Data_Quality.md)**
* **[Methodology →](docs/Methodology.md)**
* **[DAX Measures →](docs/DAX_Measures.md)**
* **[Detailed Key Findings →](docs/Key_Findings.md)**

---

## Important Note

The percentages and values reported in the **Key Findings** section are taken from the **Key Findings text embedded in the PBIX report**, rather than being estimated.

These are **descriptive findings from this healthcare-management dataset**. They should not be interpreted as causal clinical findings or as evidence of clinical effectiveness.

Numeric findings should be interpreted within the context of the dataset, dashboard definitions, filters, and reporting period.
