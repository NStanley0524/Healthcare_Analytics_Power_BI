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

The dashboard is structured into four key analytical layers, each designed to answer specific operational and strategic questions within the hospital.

---

### 1. Patient Analytics

This section focuses on understanding patient behavior, visit trends, and demographics.

**Key Metrics**
- Total Patients: 30  
- Total Monthly Visits: 41 *(+17.14% vs previous month)*  
- Average Visits per Patient: 1.37  
- Average Visit Duration: 32.32 minutes  
- Readmission Rate: 36.59%  

**Analysis Performed**
- Monthly trend analysis of patient visits  
- Breakdown of new vs returning patients  
- Age group segmentation (0–18, 18–35, 35–60, 60+)  
- Geographic distribution of patients  
- Visit outcome tracking (Recovered, Referred, Ongoing, Deceased)  

**Key Insights**
- Patient visits fluctuate throughout the year, with a noticeable mid-year peak  
- A significant portion of visits are from returning patients  
- Readmission rates are relatively high, indicating potential gaps in follow-up care  
- The majority of patients fall within the 18–35 age group  

**Patient Analytics**

![Patient Page](Images/Patients%20page.png)

---

### 2. Department Analytics

This section evaluates hospital operations at the department level.

**Key Metrics**
- Total Departments: 4  
- Waiting Cases: 34.20%  
- Admission Rate: 66.77%  
- Highest Occupied Department: Pediatrics  

**Analysis Performed**
- Bed occupancy analysis by department  
- Admission vs waiting case distribution  
- Department-level admission volume comparison  
- Heatmap of visits by day of week and hour  

**Key Insights**
- A large percentage of patients remain in waiting status, suggesting operational bottlenecks  
- Pediatrics and Cardiology experience higher occupancy levels  
- Hospital activity peaks during midday hours and weekdays  
- Resource utilization is uneven across departments  

**Department Analytics**

![Department Page](Images/Department%20page.png)

---

### 3. Doctor Performance Analytics

This section analyzes doctor workload and treatment effectiveness.

**Key Metrics**
- Total Doctors: 10  
- Average Visits per Doctor: 4  
- Patient Recovery Rate: 21.05%  
- Top Performing Doctor: Laurie York  

**Analysis Performed**
- Visits per doctor comparison  
- Monthly recovery rate trend analysis  
- Outcome distribution by doctor (Recovered, Deceased, Referred)  
- Performance quadrant analysis (efficiency vs workload)  

**Key Insights**
- Doctor workload is unevenly distributed  
- Higher workloads may correlate with lower recovery rates  
- Some doctors consistently outperform others, indicating best practices  
- Performance quadrant highlights both high-efficiency and overloaded doctors  

**Doctor Analytics**

![Doctor Page](Images/Doctors%20page.png)

---

### 4. Treatment Analytics

This section evaluates treatment effectiveness, cost, and outcomes.

**Key Metrics**
- Total Treatments: 6  
- Treatment Success Rate: 75%  
- Readmission Rate: 20%  
- Average Cost per Treatment: $640  

**Analysis Performed**
- Treatment success rate comparison across categories  
- Monthly treatment trend analysis (e.g. Chemo vs X-ray)  
- Cost vs success relationship analysis  
- Outcome breakdown by treatment type  

**Key Insights**
- Treatment success varies across categories and over time  
- Higher-cost treatments do not always yield better outcomes  
- Some treatments show consistent performance, while others fluctuate  
- Outcome distribution reflects a mix of recovered, referred, and ongoing cases  

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

- Treatment success varies by department — Chemotherapy shows higher treatment success.
- X-Ray is underperforming as a treatment in this hospital .Low treatment success and higher decease cases.
- Some months like March and June show very low trreatment rate across all treatments. Worth nothing.

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

### 5 Use Time-Based Insights to Optimize Staffing and Operations

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

### 6 Expand Patient-Centric Care Using Location and Age Insights

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

