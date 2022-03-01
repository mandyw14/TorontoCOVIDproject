# City of Toronto COVID project 2021

## Background
Not long into the pandemic, it became clear that COVID case numbers varied according to neighbourhoods in the City of Toronto, revealing hot spots and areas of the city that could be priorities. For this project, I saught to examine the case number data according to the neighbourhood. To do this, I took data from the 2016 Canada census for the City of Toronto neighbourhood demographics and used those demographics in a model to predict case counts. Case counts existed as data collected until the end of July 2021, when the data analysis was conducted. 

The City of Toronto experienced a high rate of covid cases through the COVID pandemic. The rate of covid cases hit some neighbourhoods harder than others. As a result, the city made the census 2016 neighbourhood data available that provide insights into the demographics of the neighbhour that might make a neighbourhood more vulnerable. These indicators include education levels, income levels, multigenerational housing, crowded housing, immigrants, and visible minorities. 

## Hypothesis & Implication

The goal of this data project is to determine which, if any of those indicators can be used to predict the total rate of covid cases betweeen March 2020 and June 2021 and determine if some indicators make a neighbourhood more vulnerable. Specifically, the hypothesis for this project is that the neighbourhood indicators can be used to predict rate of positive COVID cases. If a model can be generated to predict covid cases, then it could be used for the future to quickly identify vulnerable populations for in other cities in Canada, should that demographic information be available. 

If true, these data can be used to predict other rates of covid in other cities as the pandemic continues or could be used to predict vulnerability of neighbourhoods during a future pandemic of a contagious disease.

## Data
Data was taken from https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/neighbourhood-profiles/

The data consisted of 2 data sets: 
1) _Case Data_ (cov_cases):  Total number of Positive Covid Cases in the city of Toronto, Canada, separated by the city's 140 neighbourhoods. 

2) _Neighbourhood Indicators_ (cov_ind): The 140 neighbourhoods represent very different demographics in terms of education, income, immigrants, crowded housing, multigenerational housing, and visible minorities, which is available from the 2016 Canada Census. The concern is that any or all of these variables may point to a vulnerability of specific groups of people in getting COVID. 

Data from these two datasets needed be sliced and then joined so that the neighbhour indicators could be used in a regression model to predict rates of covid cases/100 000 people. The demographic independent variables used were:
    
    Low Education (Low_Edu)
    Low Income (Low_Inc)
    Multigeneration Housing (MultiGen_House)
    Crowded Housing (Crowded_House)
    Immigrants (Immigrants)
    Visibile Minorities (Vis_Minorites)

**This new file is included here: covid_dataframe.csv**

## Data Analysis & Results
The analyses can be found in the file **New COVID_data**

Using regression analysis, the best and most efficient model for predicting Rate of covid cases is a model that used Education, Multigenerational Housing, Crowded Housing, and Visible Minorities as independent variables. This represents 4 of the original 6 indicator variables. 73.6% of the variability is explained when all of those 4 variables are included in the model.

However, each of the neighbourhood indicators could be used to predict Rate of covid cases if that was the only data available. They each have significant predictive ability, with income presenting the least amount of power (R-square = .155) and education representing the most R-square =.54).

### Predicting Vulnerable and Resilient Neighbourhoods

Using the model, can we predict the Rate of Covid cases for a fictitious neighbourhood that scores high on all vulnerable indicators?  Here the highest and lowest value of each variable (as gathered with the range above) was used to predict a fictitious vulnerable and resillient community. 


**Vulnerable Community:** The predicted rate is 18 452 per 100 000 people.
**Resilient Community:** The predicted rate is 1582 per 100 000 people.
**Observation:** A community high on all indicator variables has a 11.6 fold increased vulnerability for Rate of covid cases. 

## Conclusions
Neighbourhoods with Low Education Levels, Multigenerational Housing, and Crowded Housing, and higher Visble minorities  all are at a greater risk for covid in the community. Risk of covid rates can be best predicted by including education levels, multigenerational housing, crowded housing, and visible minorites in the regression model.
