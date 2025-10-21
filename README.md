# OVERVIEW

This project showcases a comprehensive Power BI dashboard developed for **St. Augustine General Hospital**, a large multi-specialty hospital offering emergency, cardiology, pediatrics, and oncology services.

I led the full design and development of a reporting solution that provides critical insights into **patient care**, **departmental efficiency**, **doctor performance**, and **treatment outcomes**.

The objective was to simulate a real-world healthcare scenario where hospital leadership needs interactive, visual tools to make data-driven decisions and monitor performance in real time.

---

## 🔗 Live Dashboard

You can interact with the fully published Power BI dashboard here:

[View on Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiM2E4ODhjZTYtYmVmYy00N2FkLTg0N2MtYzUzODIyMTlhZWUyIiwidCI6ImZmMGYzZTNhLTNlNTMtNDU0Zi1iMmI1LTZjNjg3NTNiOGVlNCJ9)

> *(Best viewed on desktop for full functionality. Ensure pop-ups are allowed.)*

---

## Project Objectives

The project was built to address the following business objectives:

- How do **patient visits trend** month by month across the year?
- What are the proportions of patients who are *waiting*, *admitted*, or *discharged*?
- Which **departments** have the highest bed occupancy or waiting cases?
- How is the **doctor workload** distributed, and what are their treatment success rates?
- How many **treatment types** are offered, and how successful are they by department?
- What are the trends in **chronic illnesses** such as diabetes and hypertension?
- What **times and days** see the most hospital activity?
- Where are patients **coming from**, and what is their **age group** distribution?

---

## Tools & Technologies

| Tool | Use |
|------|-----|
| **Power BI Desktop** | Data modeling, dashboard creation |
| **Power Query** | Data transformation and cleaning |
| **DAX** | Business logic and KPIs |
| **Star Schema Modeling** | Scalable, optimized data architecture |
| **Power BI Service** | For live publishing, sharing, and cloud-based report consumption |

---

## Data Model Overview

The Power BI data model was built using **Star Schema** principles for performance and scalability:

- **Fact Tables**: Patient Visits  
- **Dimension Tables**: Patients, Doctors, Departments, Treatments

**Key Columns Include**:
- `VisitID`, `PatientID`, `DoctorID`, `DepartmentID`, `TreatmentID`
- `Admission Status`, `Appointment Status`, `Visit Outcome`, `Treatment Success`, `Diagnosis`, `Readmitted`, `Visit Duration`

Below is an illustration of the data model:

![Data Model](Images/Data%20model.png)

> All data was transformed using **Power Query**, and core business calculations were implemented in **DAX**.

---

## Analytical Approach

### 1. **Patient Analytics**

- Monitor key stats: total visits, new vs returning, and readmissions.
- Track patient demographics: age groups and originating locations.
- Analyze monthly visit trends and visit outcomes (e.g., recovered, deceased).
- View visit types, statuses, and patient distribution over time.

**Patient Analytics**

![Patient Page](Images/Patients%20page.png)

---

### 2. **Departmental Efficiency**

- View department-level KPIs: bed occupancy, waiting vs admitted percentages.
- Identify which departments are under pressure due to high demand.
- Explore a heatmap of visit activity by hour and weekday.
- Track admission outcomes per department.

**Department Analytics**

![Department Page](Images/Department%20page.png)

---

### 3. **Doctor Performance Analytics**

- Monitor doctors' workload: number of patients, visits, and outcomes.
- Evaluate doctor performance based on recovery, deceased, and referral rates.
- View average treatment success per doctor and identify top performers.

**Doctor Analytics**

![Doctor Page](Images/Doctors%20page.png)

---

### 4. **Treatment Outcomes Analytics**

- Track total treatment types offered and their success rates.
- Observe treatment outcome trends by department and illness type.
- Monitor chronic illness trends over time (e.g., diabetes, hypertension).
- Analyze average visit duration and unsuccessful treatment rates.

**Treatment Analytics**

![Treatment Page](Images/Treatment%20page.png)

---

## Dashboard Highlights

| Area | Description |
|------|-------------|
| **Patient Overview** | Stats on visits, readmissions, locations, and patient types |
| **Departmental Efficiency** | Admission status, occupancy %, peak periods, wait times |
| **Doctor Insights** | Recovery %, doctor visits, treatment success rates |
| **Treatment Analytics** | Chronic illness trends, treatment success %, duration & cost |

---

## Key Business Insights

### 1. Patients

- A significant percentage of visits are from returning patients, some with chronic conditions.
- Readmission rates highlight potential gaps in post-discharge care.
- Most patients come from nearby urban areas — great for location-based outreach.

### 2. Departments

- Emergency and Cardiology departments show high wait times and full occupancy.
- Pediatrics sees higher recovery rates, but lower visit volumes.

### 3. Doctors

- Some doctors handle disproportionately more patients than others.
- Doctors with higher workloads tend to have slightly lower recovery rates.
- A few doctors consistently show outstanding success rates across multiple treatments.

### 4. Treatments

- Treatment success varies by department — Oncology shows lower than average.
- Chronic illness cases like hypertension are increasing steadily over time.
- Treatments for flu and asthma have very high recovery rates.

---

## Future Enhancements

- Add **Row-Level Security (RLS)** to restrict views by department.
- Enable **scheduled data refresh** through Power BI Gateway.
- Include **patient feedback/survey data** for quality of care insights.
- Embed **interactive Q&A visual** for natural language queries.
- Publish and share via **Power BI Service** for broader stakeholder access.

