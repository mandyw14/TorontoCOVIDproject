# COVIDproject2021
Predicting COVID case counts using Toronto neighborhood demographics
This project took data from the 2016 Canada census for the City of Toronto neighbourhood demographics and used those demographics in a model to predict case counts during the 2020 pandemic. Case counts were data collected through till the end of July 2021. 

The City of Toronto experienced a high rate of covid cases through the COVID pandemic. The rate of covid cases hit some neighbourhoods harder than others. As a result, the city made the census 2016 neighbourhood data available that provide insights into the demographics of the neighbhour that might make a neighbourhood more vulnerable. These indicators include education levels, income levels, multigenerational housing, crowded housing, immigrants, and visible minorities. 

The goal of this data project is to determine which, if any of those indicators can be used to predict the total rate of covid cases betweeen March 2020 and June 2021 and determine if some indicators make a neighbourhood more vulnerable. If successful, these data can be used to predict other rates of covid in other cities as the pandemic continues or could be used to predict vulnerability of neighbourhoods during a future pandemic of a contagious disease.

Data was taken from https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/neighbourhood-profiles/

The data consisted of 2 data sets: 
1) _Case Data_ (cov_cases):  Total number of Positive Covid Cases in the city of Toronto, Canada, separated by the city's 140 neighbourhoods. 

2) _Neighbourhood Indicators_ (cov_ind): The 140 neighbourhoods represent very different demographics in terms of education, income, immigrants, crowded housing, multigenerational housing, and visible minorities, which is available from the 2016 Canada Census. The concern is that any or all of these variables may point to a vulnerability of specific groups of people in getting COVID. 

Data from these two datasets needed be sliced and then joined so that the neighbhour indicators could be used in a regression model to predict rates of covid cases/100 000 people.

The hypothesis for this project is that the neighbourhood indicators can be used to predict rate of positive COVID cases. If a model can be generated to predict covid cases, then it could be used for the future to quickly identify vulnerable populations for in other cities in Canada, should that demographic information be available. 
