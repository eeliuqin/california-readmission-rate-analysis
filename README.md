# Analysis of California 30-Day Inpatient Readmission Rates, 2011-2020
## Objective
This is a project to analyze all-cause unplanned 30-day hospital readmission rates of California statewide and counties, for years 1999-2008.

## Hypothesis
Age of patients, race/ethnicity of patients, payer type, county, population to LTC (Long Term Care) type facility ratio, and population to FDR (First Tier, Downstream, and Related Entities defined by CMS) type facility ratio are associated with hospital readmission.

## Language and Tools
Language: Python
Libraries: Pandas, Numpy, Matplotlib, Seaborn, Plotly, Requests, Json, Scipy
Tools: AWS S3, AWS SageMaker

## Step 1 Obtaining the Data
I uploaded below data files to AWS S3 for online analyzing. The data files are from 1 main dataset and 2 subdatasets:
[**California All-Cause Unplanned 30-Day Inpatient Readmission Rates**](https://data.chhs.ca.gov/dataset/all-cause-unplanned-30-day-hospital-readmission-rate-california): It's the main dataset, which contains the statewide number and (unadjusted) rate for all-cause, unplanned, 30-day inpatient readmissions in California hospitals from 2011 to 2020 (contains first three quarters for Year 2015). Data are categorized by age, sex, race/ethnicity, expected payer and county.

[**California Licensed and Certified Healthcare Facility Listing**](https://data.chhs.ca.gov/dataset/healthcare-facility-locations): This dataset was recently updated in December, 2022. It includes California healthcare facilities that are operational and have a current license issued by the California Department of Public Health (CDPH) and/or a current U.S. Department of Health and Human Services’ Centers for Medicare and Medicaid Services (CMS) certification.

[**California County Population 2020-2021**](https://www.census.gov/data/tables/time-series/demo/popest/2020s-counties-detail.html): This dataset includes county population of California in 2020-2021.

## Step 2 Data Cleaning and Manipulation
I checked data from unknown counties, removed outliers, cleaned each dataset and merged them into one dataframe by the shared column `County`.

## Step 3 Analyze
I analyzed the readmission rate by Age, Sex, Race-Ethinicity, Payer, and County. Here are the corresponding charts:
<p align="center">
  <img alt="By Age" src="images/by-age.png" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="By Sex" src="images/by-sex.png" width="45%">
</p>

## Step 4 Provide Recommendations
