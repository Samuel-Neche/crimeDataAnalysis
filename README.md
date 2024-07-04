# Crime Data Analysis

![Project Image](https://private-user-images.githubusercontent.com/135570337/244950072-9a24ad87-ff89-47c1-a078-2d734330aa44.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjAxMjU3OTAsIm5iZiI6MTcyMDEyNTQ5MCwicGF0aCI6Ii8xMzU1NzAzMzcvMjQ0OTUwMDcyLTlhMjRhZDg3LWZmODktNDdjMS1hMDc4LTJkNzM0MzMwYWE0NC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwNFQyMDM4MTBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hOTdlZTU2ZDViOGNhZGJjYzYxMzM2Y2ZmODUyMjRjZjU4NzQ5Y2FjMGIwMTlhMDIyZWE3ZDYwY2E4MDIwZDQ0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.fNHKrJmCeNTSRnXZOkAeZ3RTcJQIz2G7V3hkYXcYITQ)

## Introduction
In today's world, crime rates have surged, posing complex challenges for law enforcement globally. To tackle these issues head-on, the integration of advanced technologies and data analysis is crucial. This case study delves into how crime data analysis can elevate the effectiveness of law enforcement in a major city.
In collaboration with DataFied Academy (www.datafied.tech)

## Problem Statement
Our client, a big-city police department, is grappled with escalating crime rates and in need for a more proactive crime prevention strategy. The client reach out to Datafied Technologies to seek expertise to leverage data analytics to gain insights into crime patterns, potential crime hotspots, and develop targeted strategies for crime reduction.

## Data Sourcing
The crime data for this analysis was obtained from the open-access dataset provided by the Office for National Statistics (ONS) on their website (http://www.ons.gov.uk/). The data covers reported crimes in UK from 2012 to 2024 and includes details such as crime type, date, and location.

## Data Transformation
The raw crime data underwent cleaning to address missing values. Entries with missing locations were removed, and missing dates were imputed using the median date for the specific crime type. Inconsistent date formats were standardized to DD/MM/YYYY format, corrected the data types of some columns like 'Year' to text instead of default data type. To prepare the data for analysis, a new feature was created by merging the geo data to the crime data using 'force name'.

## Data Modelling
A dimensional data model was chosen for this analysis. The central fact table stores core crime data including ONS Code (foreign key to location dimension), quarter-year (foreign key to date dimension), and offence code (foreign key to offence dimension). The fact table also includes a measure for crime count. The location dimension includes attributes like Force name, ONS Code, and region. The date dimension includes attributes like quarter-year, financial month, financial year, and financial quarter. The offence dimension includes attributes like offence code, offence group, offence subgroup, and offence description. Relationships were established between the fact table and dimension tables using foreign keys.
