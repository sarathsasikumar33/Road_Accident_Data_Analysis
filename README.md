# Road Accident Data Analysis Using Python & Excel Analytics

**Analyzing historical traffic collision trends, environmental hazard factors, speed limit compliance, junction dynamics, and casualty severity to inform transport safety decisions.**

---

## Project Overview

Road safety and accident prevention present major urban planning, policy, and public health challenges globally. Municipal authorities, traffic safety engineers, and law enforcement agencies require data-driven insights to identify high-risk road corridors, understand compound environmental hazards (e.g., severe weather, lighting, road surface conditions), and evaluate casualty severity patterns.

This project explores a dataset of **50,008 historical road accident records** (`Road Accident Dataset.xlsx`) to identify spatial, temporal, environmental, and infrastructure patterns that contribute to collision severity.

Using **Microsoft Excel, SQL, Python (Pandas, NumPy, Matplotlib, Seaborn), and Power BI**, the project transforms raw, multi-dimensional collision logs into actionable insights and interactive dashboards designed for transport safety administrators and urban planning stakeholders.

---

## Business Problem

Traffic safety administrators and urban planners often struggle to extract clear, evidence-based insights from large volumes of raw accident reports. Key questions include:

* Which combinations of environmental factors (weather, surface condition, lighting) correlate with a higher proportion of serious or fatal casualties?
* How does collision severity vary across different speed limits, road types, and junction controls?
* What spatial disparities exist across local authority districts and police force jurisdictions?
* How do urban and rural accident profiles differ in terms of severity and vehicle involvement?

This project addresses the core question:

> **What critical patterns, high-risk environmental factors, and infrastructure conditions can be identified across historical road accident records to help prioritize traffic safety interventions?**

The analysis provides descriptive and exploratory insights. It identifies empirical associations within the historical collision logs but does not prove direct legal causation or individual driver fault.

---

## Project Objectives

* **Dataset Inspection & Quality Assessment:** Validate the schema, data types, null values, and record completeness of 50,008 incident logs.
* **Severity Profile Analysis:** Quantify overall collision volumes across severity categories (*Minor*, *Major*, *Fatal*) and analyze casualty rates per vehicle involved.
* **Environmental Risk Factor Mapping:** Evaluate compound risk correlations across weather conditions, lighting levels, and road surface states (*Dry*, *Wet/Damp*, *Snow/Ice*).
* **Infrastructure & Speed Zone Evaluation:** Compare casualty distributions across posted speed limits (20–70 mph), road classifications (*Single carriageway*, *Dual carriageway*, *Roundabout*), and junction controls.
* **Urban vs. Rural Comparison:** Contrast collision dynamics, average vehicle involvement, and casualty severity ratios between urban and rural environments.
* **Geospatial & District Hotspot Identification:** Leverage spatial coordinate data (`Latitude` and `Longitude`) to highlight district-level collision clusters.
* **Interactive Dashboard & Visualization:** Develop an end-to-end interactive Power BI dashboard and publication-ready Python graphics to communicate findings clearly.

---

## Dataset Information

| Attribute | Details |
| :--- | :--- |
| **Dataset Name** | Road Accident Dataset (Cleaned & Structured) |
| **Dataset Source** | [Kaggle Dataset](https://www.kaggle.com/datasets/imsaed/road-accident-dataset-cleaned-and-structured) |
| **File Format** | Excel (.xlsx) / CSV (.csv) |
| **Number of Records** | 50,008 rows |
| **Number of Columns** | 20 columns |
| **Geographical Scope** | UK Municipalities / Local Authority Districts & Police Forces |
| **Time Period Covered** | 2021 – 2022 |
| **Unit of Observation** | Single traffic collision incident (`Accident_Index`) |
| **Domain** | Public Safety Analytics / Transportation Infrastructure Analytics |

### Key Dataset Fields

* `Accident_Index` – Unique incident key.
* `Accident Date` & `Time` – Incident date and timestamp.
* `Accident_Severity` – Incident severity grade (*Minor*, *Major*, *Fatal*).
* `Number_of_Casualties` – Total number of casualties resulting from the collision.
* `Number_of_Vehicles` – Total count of vehicles involved.
* `Speed_limit` – Posted speed limit (mph) for the road segment.
* `Road_Type` – Infrastructure layout (*Single carriageway*, *Dual carriageway*, *Roundabout*, etc.).
* `Junction_Control` & `Junction_Detail` – Traffic control mechanism and junction geometry.
* `Light_Conditions` – Illumination level at the time of collision.
* `Weather_Conditions` – Atmospheric weather conditions recorded at the scene.
* `Road_Surface_Conditions` – Surface state (*Dry*, *Wet or damp*, *Snow*, *Frost or ice*, *Flood*).
* `Carriageway_Hazards` – Physical hazards present on the roadway (e.g., dislodged loads, animals).
* `Urban_or_Rural_Area` – Regional context classification (*Urban* vs. *Rural*).
* `Latitude` & `Longitude` – GIS coordinates for mapping collision density.
* `Local_Authority_(District)` & `Police_Force` – Local administrative jurisdiction.
* `Vehicle_Type` – Primary vehicle class involved (*Car*, *Bus/Coach*, *Motorcycle*, *Van*, *Bicycle*).

---

## Tools and Technologies

* **Microsoft Excel** – Initial dataset inspection, cell formatting validation, quick pivots, and metadata verification.
* **SQL (SQLite / PostgreSQL)** – Structured queries, grouping, cross-tabulations, and aggregated risk profiling.
* **Python** – Core analytical data wrangling, cleaning, missing value handling, and exploratory analysis.
* **Pandas & NumPy** – Tabular data processing and statistical operations.
* **Matplotlib & Seaborn** – Statistical visualizations, correlation matrices, and distribution charts.
* **Power BI** – Multi-page interactive dashboard creation, dynamic slicers, DAX metrics, and spatial visual maps.
* **Jupyter Notebook** – Execution and documentation of Python scripts.
* **GitHub** – Version control, repository hosting, and portfolio presentation.

---

## Project Workflow

1. **Dataset Ingestion & Inspection:** Load `Road Accident Dataset.xlsx`, verify the 50,008 row count, validate schema types, and inspect summary distribution metrics.
2. **Data Cleaning & Preprocessing:**
   * Recode missing values in high-null fields (`Carriageway_Hazards` ~98.8% null) to `"None/No Hazard"`.
   * Parse date strings and standardize fractional timestamps into 24-hour time bins.
   * Standardize categorical values and remove trailing whitespace/case inconsistencies.
3. **Exploratory Data Analysis (EDA):** Examine accident volume across severity tiers, evaluate casualty ratios per vehicle type, and calculate average casualties by speed limit zone.
4. **Environmental & Structural Hazard Profiling:** Perform multi-variable cross-tabulations to evaluate how wet surfaces, dark lighting, and adverse weather impact accident severity.
5. **Urban vs. Rural Comparative Analysis:** Measure differences in collision volume, average speed limits, and fatal casualty proportions across urban and rural zones.
6. **SQL Query Development:** Author structured SQL scripts to extract district rankings, high-risk speed zone counts, and junction hazard statistics.
7. **Interactive Dashboard Creation:** Build a multi-tab Power BI report (`Overview`, `Environmental Hazards`, and `Spatial & Infrastructure Analytics`).
8. **Documentation & Reporting:** Synthesize findings, state analytical limitations, and outline evidence-based safety policy recommendations.

---

## Planned Analytical Areas

| Analysis Focus | Key Questions Explored |
| :--- | :--- |
| **Severity Distribution** | What is the proportion of Minor, Major, and Fatal accidents across the 50,008 recorded incidents? |
| **Environmental Risk Factors** | How do adverse weather conditions (rain, fog, snow) and wet/icy road surfaces correlate with collision severity? |
| **Speed Limits & Infrastructure** | Which posted speed limit zones (30, 40, 60, 70 mph) and road types display the highest casualty density? |
| **Junction Analysis** | What junction controls (*Auto traffic signal*, *Give way*) and geometries (*Roundabout*, *Crossroads*) experience the most multi-vehicle collisions? |
| **Urban vs. Rural Dynamics** | How do accident frequencies and severity proportions differ between high-density urban areas and open rural roadways? |
| **Vehicle Type Impact** | How do casualty rates vary when vulnerable road users (motorcycles, bicycles) or commercial vehicles are involved? |
| **Geospatial Hotspots** | Which local authority districts and police force jurisdictions record the highest concentration of serious accidents? |

---

## Expected Value and Insights

This analytical project provides key value for transportation safety stakeholders by:

* Identifying high-risk speed zones and road types requiring targeted infrastructure improvements (e.g., traffic calming, junction redesign).
* Highlighting high-hazard environmental scenarios (e.g., wet roads during dark hours) to inform public safety awareness campaigns.
* Providing municipal traffic authorities with district-level rankings to optimize police enforcement resource allocation.
* Offering an interactive Power BI dashboard that enables non-technical stakeholders to dynamically slice accident metrics by location, severity, and road condition.

---

## Repository Structure

```text
Road-Accident-Data-Analysis/
│
├── data/
│   ├── raw/
│   │   └── Road Accident Dataset.xlsx
│   └── processed/
│       └── road_accident_cleaned.csv
│
├── notebooks/
│   └── Road_Accident_Analysis.ipynb
│
├── sql/
│   └── accident_analysis_queries.sql
│
├── powerbi/
│   └── Road_Accident_Safety_Dashboard.pbix
│
├── reports/
│   ├── Road_Accident_Data_Analysis_SRS.docx
│   └── Project_Final_Report.docx
│
└── README.md
```

* `data/raw/` – Contains the original dataset (`Road Accident Dataset.xlsx`).
* `data/processed/` – Stores cleaned, standardized working datasets generated during analysis.
* `notebooks/Road_Accident_Analysis.ipynb` – Jupyter Notebook detailing Python inspection, cleaning, EDA, and Seaborn visualizations.
* `sql/accident_analysis_queries.sql` – SQL scripts used for data aggregation, cross-tabulations, and statistical groupings.
* `powerbi/Road_Accident_Safety_Dashboard.pbix` – Power BI report featuring interactive filters, KPIs, and GIS mapping.
* `reports/` – Formal project documentation including the Software Requirements Specification (SRS) and Final Report.
* `README.md` – Project landing page, technical overview, dataset details, and workflow summary.

---

## Scope and Limitations

* **Reporting Bias:** The dataset covers formally reported police collision logs; minor, unrecorded crashes are absent.
* **Missing Field Coverage:** The `Carriageway_Hazards` field contains high null rates (~98.8%), indicating hazards were absent or unrecorded in most cases; analysis treats nulls as `"None/No Hazard"`.
* **Lack of Driver Demographics:** Key human factor variables—such as driver age, experience level, seatbelt usage, or toxicity results—are not present in the dataset.
* **Observational Findings:** Findings describe statistical associations within historical records and do not establish direct legal causality or fault.

---

## Project Status

**Phase 1 – Project Proposal, SRS, and Initial Dataset Inspection**

* Project scope, business problem, and technical pipeline defined.
* Dataset inspected and confirmed (50,008 records, 20 columns).
* Software Requirements Specification (SRS) completed.
* Next Phase: Data cleaning execution, exploratory analysis, SQL query implementation, Power BI dashboard design, and final report synthesis.
* 

