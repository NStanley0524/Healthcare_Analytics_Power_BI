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

## Datasource

The dataset used in this project was a simulated healthcare dataset structured around a hospital scenario. It reflects real-world data patterns and includes details on:

- Patient demographics and visit history  
- Admission and appointment status  
- Departmental allocation and doctor assignments  
- Treatment types, diagnoses, and outcomes  
- Readmission flags and visit duration metrics

The data was pre-cleaned and modeled into a **star schema**, ensuring it's optimized for performance and scalability in Power BI.

> ⚠️ Note: This dataset is fictional and intended for educational and portfolio purposes only. No real patient data is used.

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


## Business Recommendations

### 1 Reduce Readmissions Through Structured Post-Discharge Care

### Problem Identified  
A noticeable portion of patients are **returning or readmitted**, indicating gaps in post-treatment follow-up and continuity of care.

### Action  
Introduce a standardized post-discharge follow-up program.

### How to Implement  
- Create discharge protocols that include:
  - Mandatory follow-up appointments before discharge
  - Clear medication and care instructions logged digitally
- Assign nurses or care coordinators to conduct **48–72 hour post-discharge check-ins** for high-risk patients.
- Track **readmission rates by department and diagnosis** monthly in Power BI.

### Owner  
Hospital Administration / Care Coordination Team

### Expected Impact  
- Reduced readmission rates  
- Improved patient recovery outcomes  
- Lower operational costs from repeat visits  

---

### 2 Alleviate Pressure in High-Demand Departments (Emergency & Cardiology)

### Problem Identified  
**Emergency and Cardiology** departments experience high wait times and near-full bed occupancy.

### Action  
Optimize resource allocation and patient flow in high-demand departments.

### How to Implement  
- Adjust staff scheduling to align with **peak hours and days** identified in the dashboard.
- Introduce fast-track protocols for low-risk emergency cases.
- Redirect non-critical cases to outpatient or less congested departments when possible.
- Monitor bed occupancy and waiting metrics daily using operational dashboards.

### Owner  
Hospital Operations / Department Heads

### Expected Impact  
- Reduced patient wait times  
- Improved patient satisfaction  
- Lower staff burnout in critical departments  

---

### 3 Balance Doctor Workload to Improve Treatment Outcomes

### Problem Identified  
Doctors with **higher patient loads** tend to have slightly lower recovery rates.

### Action  
Redistribute patient assignments more evenly across doctors.

### How to Implement  
- Set workload thresholds per doctor based on historical performance data.
- Use Power BI insights to identify underutilized doctors.
- Introduce rotating schedules or cross-department support during peak periods.
- Include workload balance as a KPI in performance reviews.

### Owner  
Medical Director / Human Resources

### Expected Impact  
- Improved recovery rates  
- More sustainable doctor workloads  
- Better overall quality of care  

---

### 4 Scale Best Practices from High-Performing Doctors

### Problem Identified  
A subset of doctors consistently shows **exceptionally high treatment success rates**.

### Action  
Standardize and replicate best-performing clinical practices.

### How to Implement  
- Analyze treatment methods, visit durations, and diagnostic patterns of top-performing doctors.
- Document these methods into **clinical best-practice guidelines**.
- Introduce peer learning sessions and internal training led by high performers.
- Track department-level improvements after implementation.

### Owner  
Clinical Leadership / Quality Assurance Team

### Expected Impact  
- Higher overall treatment success rates  
- Reduced variability in patient outcomes  
- Faster skill development across staff  

---

### 5 Strengthen Oncology Treatment Outcomes

### Problem Identified  
**Oncology** treatments show lower-than-average success rates compared to other departments.

### Action  
Conduct targeted performance and process reviews within Oncology.

### How to Implement  
- Break down oncology outcomes by:
  - Treatment type  
  - Visit duration  
  - Readmission status  
- Introduce multidisciplinary case reviews for complex oncology cases.
- Invest in early-detection programs and patient education for oncology-related conditions.
- Monitor oncology KPIs separately on executive dashboards.

### Owner  
Oncology Department Head / Hospital Leadership

### Expected Impact  
- Improved oncology treatment outcomes  
- Earlier intervention and diagnosis  
- Enhanced patient trust and care quality  

---

### 6 Proactively Manage Chronic Illness Growth Trends

### Problem Identified  
Cases of **chronic illnesses** such as hypertension are steadily increasing.

### Action  
Shift from reactive treatment to preventive care programs.

### How to Implement  
- Launch chronic disease management clinics or programs.
- Schedule routine follow-ups and monitoring for chronic patients.
- Partner with community health organizations for lifestyle and wellness education.
- Track chronic illness visit trends and outcomes quarterly.

### Owner  
Public Health Unit / Preventive Care Team

### Expected Impact  
- Reduced long-term hospital visits  
- Better patient quality of life  
- Lower long-term healthcare costs  

---

### 7 Use Time-Based Insights to Optimize Staffing and Operations

### Problem Identified  
Hospital activity peaks at specific **hours and weekdays**, causing uneven workload distribution.

### Action  
Align staffing and operational capacity with demand patterns.

### How to Implement  
- Adjust nurse and doctor shift rosters based on hourly and weekday trends.
- Increase diagnostic and support staff availability during peak periods.
- Use Power BI alerts to flag unusually high activity in real time.

### Owner  
Hospital Operations / Workforce Planning Team

### Expected Impact  
- Smoother hospital operations  
- Shorter patient wait times  
- Improved staff efficiency and morale  

---

### 8 Expand Patient-Centric Care Using Location and Age Insights

### Problem Identified  
Most patients come from **nearby urban areas**, with distinct age group patterns.

### Action  
Tailor services and outreach programs to dominant patient demographics.

### How to Implement  
- Design age-specific care programs (e.g., pediatrics education, geriatric care plans).
- Collaborate with local clinics and pharmacies in high-density patient areas.
- Track outreach effectiveness by monitoring visit trends post-initiative.

### Owner  
Hospital Strategy / Community Outreach Team

### Expected Impact  
- Stronger community engagement  
- Increased preventive care uptake  
- Improved patient loyalty and outcomes  

---


## Future Enhancements

- Add **Row-Level Security (RLS)** to restrict views by department.
- Enable **scheduled data refresh** through Power BI Gateway.
- Include **patient feedback/survey data** for quality of care insights.
- Embed **interactive Q&A visual** for natural language queries.
- Publish and share via **Power BI Service** for broader stakeholder access.

