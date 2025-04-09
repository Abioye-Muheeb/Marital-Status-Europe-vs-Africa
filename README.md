# Marital Status in Europe vs Africa Analysis

### Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning-Preparation](#data-cleaningpreparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Scope](#scope)
- [Data Visualizations](#data-visualizations)
- [Key Insights](#key-insights)
- [Conclusion-Findings](#conclusionfindings)





### Project Overview

This project aims to analyze and visualize disparities in marital status and age demographics across selected African and European countries from 1966 to 2011. The study examines trends in marriage, divorce, singlehood, widowhood, and consensual unions, segmented by age groups, sex, and region, to identify patterns and differences over time.

### Data Sources

Marital Data : The dataset used for this analysis is the "Marital_status_by_Age.csv" file, containing detailed information about marital status of each selected countires.

### Tools

- Excel - Data Cleaning
- Power BI - Creating reports


### Data Cleaning/Preparation
in the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions, such as:

- To compare significant disparity of marital status based on gender between Europe and Africa countries.
- To compare significant disparity of marital status based on age between Europe and Africa countries.
- To compare significant disparity of marital status between Europe and Africa countries over time.

### Data Analysis 

Including some intresting code/features worked with

```Power BI (DAX)
Married Rate = 
DIVIDE(
CALCULATE(SUM(Marital_status_by_Age[Total Population]), Marital_status_by_Age[Marital status] = "Married"),
        SUM(Marital_status_by_Age[Total Population]),
    0
)
```

```Power BI (DAX)
Country Classification = 
SWITCH(
    TRUE(),
    Marital_status_by_Age[Country] IN { "Austria", "Belgium", "Denmark", "Germany", "Italy",  "Netherlands"}, "Europe",
    Marital_status_by_Age[Country] IN { "Algeria", "Egypt", "Ethiopia", "Kenya", "Morocco", "Ghana"}, "Africa",
    "N/A"
    )
```



 ### Scope 

- Time Period - 1966 to 2011
- Regions - Africa and Europe
- Demographics - Segmented by sex (men and women) and age groups (Young: 15-24, Adult: 25-39, Middle Age: 40-54, Older Age: 55-65+)
- Marital Status Categories - Married, Single, Widowed, Divorced, Separated, Consensual Union, Divorced/Separated

### Data Visualizations

The project includes three main dashboards:

1.	Age-Based Disparities :
	  - Bar charts showing total population by marital status and age group.
	  - Line graphs tracking population trends by age group over time.
	  - Pie chart summarizing population distribution across age categories.
	  - Comparison of married population by age group and sex.
	  - Bar chart comparing marriage rates by age group and region.

2. Marital Status Disparities :
	  - Pie chart and bar charts showing population distribution by marital status.
	  - Line graphs tracking trends in married, divorced, single, widowed, and consensual union rates over time, segmented by region.
	  - Table summarizing total population by age group and marital status.
	  
3.  Continent-Based Disparities :
	  - Bar chart comparing marriage rates by sex and continent.
	  - Line graphs showing trends in marriage, divorce, single, widowed, consensual union, and separation rates by continent over time.
	  - Pie chart illustrating the total population split between Africa and Europe.


### Key Insights

1.  Marital Status Trends :
    - Marriage is the most common status across all age groups, with the Middle Age (40-54) group having the highest married population (26K). Divorce and widowhood are more prevalent in older age groups.
    - Marriage rates have generally declined over time in both regions, while divorce and single rates have increased, particularly in Europe.

2.  Age and Sex Distribution :
    - The older age group (55–65+) and adults (25–39) dominate the population, with the young (15–24) having a higher single population.
    - The population is nearly evenly split between men and women, with slight variations in marital status distribution.
    - Younger populations (15-24) are more likely to be single, while middle-aged groups (40-54) have the highest marriage rates.

3.  Regional Differences :
    - Africa shows a higher marriage rate (69.51% for men, 63.39% for women) compared to Europe (58.10% for men, 56.79% for women). Divorce and single rates are higher in Europe, while consensual unions are more common in Africa.
    -  Africa shows a stronger tendency toward marriage and widowhood, while Europe has higher rates of divorce and singlehood, reflecting cultural and societal differences.

4.  Time Trends :
    - Marriage rates have generally declined in both regions since the 1970s, while divorce and single rates have increased, particularly in Europe. Widowhood rates have fluctuated, with a noticeable peak in Africa around the 1980s.
5.  Population Breakdown :
    - The total population is 119K, with 59K men and 61K women. Africa accounts for 44.72% of the population, while Europe accounts for 55.28%.
 
 
### Conclusion/Findings

This project provides a comprehensive view of how marital status and age demographics have evolved in Africa and Europe over a 45-year period. The findings highlight significant regional differences in marriage and divorce trends, as well as the impact of age and sex on marital status. These insights can inform social policy, demographic studies, and further research into cultural and economic factors influencing marital behavior.
