# Crime Data Analysis

![Project Image](https://img.freepik.com/free-photo/back-view-man-planning-hacker-attack-dark-room-man-writing-wall-with-stickers-photographs-red-threads-planning-conspiracy-hacking-concept_74855-24330.jpg?t=st=1720189987~exp=1720193587~hmac=5cae072af7469f9da560716f4c164a429faec32581afec58fed68869ad838715&w=1380)

## Introduction
In today's world, crime rates have surged, posing complex challenges for law enforcement globally. To tackle these issues head-on, the integration of advanced technologies and data analysis is crucial. This case study delves into how crime data analysis can elevate the effectiveness of law enforcement in a major city.
This project is in collaboration with DataFied Academy (www.datafied.tech)

## Problem Statement
Our client, a big-city police department, is grappled with escalating crime rates and in need for a more proactive crime prevention strategy. The client reach out to Datafied Technologies to seek expertise to leverage data analytics to gain insights into crime patterns, potential crime hotspots, and develop targeted strategies for crime reduction.

## Data Sourcing
The crime data for this analysis was obtained from the open-access dataset provided by the Office for National Statistics (ONS) on their website (http://www.ons.gov.uk/). The data covers reported crimes in UK from 2012 to 2024 and includes details such as crime type, date, and location.
### Webisite Preview
![image](https://github.com/Samuel-Neche/crimeDataAnalysis/assets/117985333/d3f5a8ec-acbd-4752-953b-6163c8f053c4)


## Data Transformation
The raw crime data underwent cleaning to address missing values. Entries with missing locations were removed, and missing dates were imputed using the median date for the specific crime type. Inconsistent date formats were standardized to DD/MM/YYYY format, corrected the data types of some columns like 'Year' to text instead of default data type. To prepare the data for analysis, a new feature was created by merging the geo data to the crime data using 'force name'.
### Dataset before Cleaning
![image](https://github.com/Samuel-Neche/crimeDataAnalysis/assets/117985333/80f89ff8-9600-4629-ac6e-f295e8320efc)


### Dataset after cleaning
![image](https://github.com/Samuel-Neche/crimeDataAnalysis/assets/117985333/5f084b42-61ee-4725-b3cf-bc4b10ca1923)


## Data Modelling
A dimensional data model was chosen for this analysis. Dimensions with which to break down the analysis were identified. Hence, new tables for identified dimensions were created. These included:

- offenceDim
- dateDim
- locationDim
- crimeDataFact

The crimeDataFact table stores core crime data including ONS Code (foreign key to location dimension), quarter-year (foreign key to date dimension), and offence code (foreign key to offence dimension). The fact table also includes a measure for crime count. The location dimension includes attributes like Force name, ONS Code, and region. The date dimension includes attributes like quarter-year, financial month, financial year, and financial quarter. The offence dimension includes attributes like offence code, offence group, offence subgroup, and offence description. Relationships were established between the fact table and dimension tables using foreign keys.

![image](https://github.com/Samuel-Neche/crimeDataAnalysis/assets/117985333/0a76fc38-4a8e-47bc-8f62-8c6e817fb392)
