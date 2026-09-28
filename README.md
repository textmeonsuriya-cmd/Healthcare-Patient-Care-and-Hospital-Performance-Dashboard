# Healthcare Patient Care and Hospital Performance Dashboard

A Power BI dashboard designed to help hospitals monitor patient care, operational performance, costs, and outcomes in one place.

The dashboard analyzes admissions, patient volume, treatment costs, average length of stay, readmission rate, patient satisfaction, department performance, doctor workload, common diagnoses, and patient outcomes.

> Note: All hospital names, patient records, user emails, and values used in this project are fictional and created for educational purposes.

---

## Project Objective

The goal of this project is to provide hospital management with an interactive dashboard that supports better decisions while protecting sensitive healthcare data.

It demonstrates how Power BI can be used to:

- Monitor hospital and department performance
- Analyze patient admissions and treatment costs
- Track patient outcomes and readmission rates
- View detailed patient admission history using Drillthrough
- Restrict data access using Dynamic Row-Level Security

---

## Dashboard Pages

### 1. Hospital Overview

The main dashboard page includes:

- Total Admissions
- Total Patients
- Total Treatment Cost
- Average Length of Stay
- Readmission Rate
- Average Patient Satisfaction Score
- Department Performance
- Top 5 Doctors by Admissions
- Top 5 Diagnoses by Admissions
- Admissions by Type
- Patient Journey
- Treatment Cost by Hospital
- Monthly Admission Trend
- Patient Summary table

Interactive slicers allow users to filter by:

- Admission Date
- Hospital
- Department
- Doctor
- Diagnosis
- Outcome

### 2. Patient Details

This Drillthrough page displays detailed information for a selected patient, including:

- Patient Name
- Total Admissions
- Total Treatment Cost
- Average Length of Stay
- Average Satisfaction Score
- Admission ID
- Admission Date
- Discharge Date
- Diagnosis
- Doctor Name
- Treatment Cost
- Outcome

---

## Key Features

### Drillthrough

Users can right-click a patient in the **Patient Summary** table and navigate to the **Patient Details** page.

This allows users to move from summary-level insights to individual patient admission history.

### Dynamic Row-Level Security

Dynamic RLS is implemented using the `UsersSecurity` table and the logged-in user's email address through `USERPRINCIPALNAME()`.

| Role | Access |
|---|---|
| Hospital Admin | Can view all hospital data |
| Hospital Manager | Can view data for the assigned hospital only |
| Department Head | Can view data for the assigned department only |
| Doctor | Can view admissions assigned to that doctor only |

### Bookmarks and Tooltips

- A **Reset Filters** button uses a bookmark to restore the dashboard to its default filter state.
- Tooltips provide helpful information when users hover over buttons and visuals.
- A refresh button is included for updating the report data.

---

## Benefits

- Provides a single view of key hospital performance indicators
- Helps identify high-admission departments and common diagnoses
- Supports cost monitoring and trend analysis
- Helps management understand patient outcomes
- Enables patient-level investigation through Drillthrough
- Protects sensitive healthcare information through Dynamic RLS
- Improves access control for different hospital roles

---

## Data Model

The project uses a star-schema-style data model.

### Fact Table

- `Admissions`

### Dimension Tables

- `Hospitals`
- `Departments`
- `Doctors`
- `Patients`

### Security Table

- `UsersSecurity`

---

## Tools Used

- Microsoft Power BI Desktop
- DAX
- Microsoft Excel
- Dynamic Row-Level Security
- Power BI Bookmarks
- Power BI Drillthrough
- Power BI Tooltips

---

## Files in This Repository

```text
Patient Care & Hospital Performance Dashboard.pbix
Healthcare_PowerBI_Dataset.xlsx
README.md
