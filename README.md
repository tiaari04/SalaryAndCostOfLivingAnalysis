# Global Data Science Salary Analysis

## Overview
Analysis of global data science salaries combined with country-level cost-of-living indices to compare nominal compensation with real purchasing power across countries. All salaries were standardized to CAD using a fixed USD/CAD exchange rate.

## Key Findings

* High-paying data science roles are heavily concentrated in the United States, reflecting the density of large tech companies in North America
* Compensation has grown year-over-year between 2021 and 2023, with the salary distribution shifting noticeably higher
* Large companies offer stronger entry-level compensation than small or medium-sized ones
* Salary variability increases with experience - senior roles show a much wider compensation range than junior roles
* After adjusting for cost of living, countries like New Zealand, Israel, and Russia offer stronger real purchasing power than the US despite lower nominal salaries

## Process
### Data Cleaning

* Removed columns unrelated to compensation or company characteristics
* Excluded records with invalid salary values and missing company size data
* Converted all salaries from USD to CAD using a fixed exchange rate (1 CAD = 0.722 USD)

### Feature Engineering

* salary_in_cad — standardized salary for cross-country comparison
* real_salary — nominal salary adjusted by cost-of-living index to approximate purchasing power

### Analysis

* Geographic distribution of roles and salaries by country
* Entry-level salary trends broken down by company size and year
* Median salary by experience level (median used to reduce outlier influence)
* Year-over-year salary growth via line chart and histogram comparison (2021 vs. 2023)
* Experience vs. salary scatterplot within large companies
* Nominal vs. real salary comparison across all countries


## Tools & Libraries

* pandas — data cleaning, filtering, groupby aggregations, pivot tables
* numpy — currency conversion and statistical calculations
* plotly.express — bar charts, line charts, histograms, scatterplots


## Data Sources

* **Salary data**: global data science compensation records
* **Cost of living**: country-level cost-of-living index merged on company location

## Limitations

* **US-Heavy Dataset** — The data is heavily skewed toward US-based companies, which affects the reliability of conclusions about other countries. Findings about nations like New Zealand or Israel are based on significantly fewer records than US findings.
* **Country-Level Cost-of-Living Index** — The purchasing power adjustment treats each country as having uniform living costs. In reality, costs vary significantly within countries (e.g. a data scientist in New York vs. rural Ohio), which this analysis cannot capture.
* **Limited Time Range** — The dataset only covers 2020–2023, so the observed upward salary trend may reflect post-COVID hiring.
