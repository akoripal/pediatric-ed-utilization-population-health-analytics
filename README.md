pediatric-ed-utilization-population-health-analytics

Population health analytics dashboard analyzing pediatric emergency department utilization, asthma-related ED demand, and primary care access across communities using population-normalized healthcare metrics.

This project uses pediatric healthcare utilization data from the UPMC Pediatric Population Health dataset provided through the University of Pittsburgh's Record Research Request Service (R3) covering 2016–2019 across census block groups in Allegheny County, Pennsylvania.

The analysis identifies communities with elevated pediatric emergency department utilization, potential gaps in primary care access, and clinical drivers of pediatric emergency demand.

Dashboard

The Power BI dashboard visualizes pediatric healthcare utilization patterns and enables stakeholders to identify high-priority intervention communities.

Project Objective

The goal of this project is to analyze pediatric healthcare utilization patterns across communities and identify population health insights that can support healthcare planning and preventative care programs.

The dashboard answers key healthcare analytics questions:

Which communities have the highest pediatric emergency department utilization?

How does primary care utilization relate to emergency department demand?

What clinical factors (such as asthma) drive pediatric ED visits?

Are low-acuity (non-urgent) ED visits increasing over time?

Where are the largest pediatric populations located?

Dataset Description

The analysis integrates multiple datasets related to pediatric healthcare utilization.

Emergency Department Dataset

Source: UPMC Pediatric Emergency Department Data

Includes:

Pediatric emergency department visit counts

Asthma-related ED visits

Low-acuity ED visits

ED utilization by census geography

File:

data/r3_ed_opendata.csv
Primary Care Utilization Dataset

Source: UPMC Primary Care Utilization Data

Includes:

Pediatric primary care visit rates

Primary care utilization by census block group

File:

data/r3_primarycare_opendata (1).csv
Final Analytical Dataset

The final dataset was engineered by integrating the ED dataset and primary care dataset along with pediatric population estimates.

Features include:

census tract identifiers (Geo_FIPS)

pediatric population

pediatric ED visit counts

asthma-related ED visits

low-acuity ED visits

primary care utilization rates

File:

data/pediatric_population_health_dataset.csv
Data Processing Pipeline

The project follows an end-to-end analytics workflow.

Raw Healthcare Data
      ↓
Data Cleaning & Transformation (Python / Pandas)
      ↓
Population Health Metric Engineering
      ↓
Analytical Dataset
      ↓
Power BI Population Health Dashboard

Data transformations were performed using Python in:

notebook/Pediatric_ED_Utilization_Project.ipynb

Key transformations include:

merging ED and primary care datasets

aggregating data by census geography

calculating population-normalized healthcare metrics

preparing data for dashboard visualization

Population Health Metrics

The dashboard includes several population health indicators.

Pediatric ED Visit Rate
ED Visits per 1,000 Children

Measures overall pediatric emergency department demand.

Asthma ED Visit Rate
Asthma-related ED visits per 1,000 children

Asthma is one of the most common drivers of pediatric emergency department utilization.

Low-Acuity ED Visit Rate
Low-acuity (non-urgent) ED visits per 1,000 children

Indicates emergency visits that could potentially be managed through primary care or urgent care settings.

Primary Care Utilization Rate
Primary care visits relative to pediatric population

Used to assess community-level access to outpatient pediatric healthcare.

Key Insights
1. Pediatric ED utilization varies significantly across communities

Several census tracts demonstrate substantially higher pediatric ED visit rates, suggesting disparities in healthcare access or higher disease burden.

These communities may benefit from targeted population health interventions.

2. Asthma is a major driver of pediatric emergency utilization

Certain communities show elevated asthma-related ED visits, indicating opportunities for preventative care programs such as:

school-based asthma education

improved inhaler access

environmental health interventions

3. Low-acuity ED visits are increasing over time

From 2016–2019, the analysis shows a steady increase in low-acuity pediatric ED visits, suggesting that some emergency department demand involves non-urgent conditions.

Healthcare systems could potentially reduce ED utilization through:

urgent care alternatives

telehealth triage

expanded primary care access

4. Pediatric population distribution highlights intervention priorities

Combining pediatric population distribution with ED utilization rates identifies high-impact communities where population health programs could benefit the largest number of children.

Tools & Technologies

Python
Pandas
Jupyter Notebook
Power BI

Analytics techniques used include:

healthcare utilization analysis

population-normalized rate calculations

community-level population health analytics

interactive dashboard development

Repository Structure
Power BI/
    Population_Health_Analytics.pbix

data/
    r3_ed_opendata.csv
    r3_primarycare_opendata (1).csv
    pediatric_population_health_dataset.csv

notebook/
    Pediatric_ED_Utilization_Project.ipynb

images/
    dashboard.png

This repository demonstrates a full analytics workflow:

Raw Healthcare Data
      ↓
Data Cleaning & Integration
      ↓
Population Health Metrics
      ↓
Interactive Power BI Dashboard
Potential Applications

This analysis framework can support:

hospital population health teams

community health planning initiatives

healthcare utilization monitoring

preventative pediatric healthcare programs

Author

Anurag Koripalli
Purdue University
Business Analytics & Information Management
