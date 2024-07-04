# Crime Data Analysis

![Project Image](https://private-user-images.githubusercontent.com/135570337/244950072-9a24ad87-ff89-47c1-a078-2d734330aa44.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjAwODI1MDQsIm5iZiI6MTcyMDA4MjIwNCwicGF0aCI6Ii8xMzU1NzAzMzcvMjQ0OTUwMDcyLTlhMjRhZDg3LWZmODktNDdjMS1hMDc4LTJkNzM0MzMwYWE0NC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwNFQwODM2NDRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02Nzg5NjY1ZDVkMTZkMzgwNTg5YjQxNDRlOTY3N2I4NTYwYmZkYWJjZjU1ZjMzYjg5ZTNmMjU3OGFmYTgwZGIwJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.m4-giylAzj067yP3pTCd0ahdrob3xHrm9NAsCRdfRYw)

## Introduction
In today's world, crime rates have surged, posing complex challenges for law enforcement globally. To tackle these issues head-on, the integration of advanced technologies and data analysis is crucial. This case study delves into how crime data analysis can elevate the effectiveness of law enforcement in a major city.
In collaboration with DataFied Academy (www.datafied.tech)

## Problem Statement
Our client, a big-city police department, is grappled with escalating crime rates and in need for a more proactive crime prevention strategy. The client reach out to Datafied Technologies to seek expertise to leverage data analytics to gain insights into crime patterns, potential crime hotspots, and develop targeted strategies for crime reduction.

## Data Sourcing
The crime data for this analysis was obtained from the open-access dataset provided by the Office for National Statistics (ONS) on their website (http://www.ons.gov.uk/ons). The data covers reported crimes in UK from 2012 to 2024 and includes details such as crime type, date, and location.

## Data Transformation
The raw crime data underwent cleaning to address missing values. Entries with missing locations were removed, and missing dates were imputed using the median date for the specific crime type. Inconsistent date formats were standardized to YYYY-MM-DD format. To prepare the data for analysis, a new feature was created by combining the 'crime type' and 'location' categories. Additionally, the time of day for each crime was extracted from the timestamp.

## Data Modelling
A dimensional data model was chosen for this analysis. The central fact table stores core crime data including location (foreign key to location dimension), date (foreign key to time dimension), and crime type (foreign key to crime type dimension).  The fact table also includes a measure for crime count. The location dimension includes attributes like city, ONS Code, and region. The time dimension includes attributes like year, month, day of week, and hour of day. The crime type dimension includes attributes like violent crime type, property crime type, and specific offense categories. Relationships were established between the fact table and dimension tables using foreign keys.
