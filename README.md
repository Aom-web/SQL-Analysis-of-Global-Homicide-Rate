## SQL Analysis of Global Homicide Rate
## Overview
Analysis of homicide rate based on country, year, age group and gender using SQL queries and Excel dashboard visua lization
## Data Source
This data was gotten from kaggle
[Download here] (https://www.kaggle.com/datasets/lucalullo/global-homicide-rates-by-country)

## SQL Queries

### 1. What country had the highest average homicide rate?

```SQL
SELECT country, AVG (homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE sex = 'both'
AND age_group = 'ALL'
GROUP BY country
ORDER BY AVG(homicide_rate) DESC
LIMIT 1;
```
<img width="260" height="57" alt="1" src="https://github.com/user-attachments/assets/1afe3236-3edb-4bda-b5d1-9f87b4870253" />


### 2. Top 5 countries that had the highest average homicide rate?

```SQL
SELECT country, AVG (homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE sex = 'both'
AND age_group = 'ALL'
GROUP BY country
ORDER BY AVG(homicide_rate) DESC
LIMIT 5;
```
<img width="271" height="162" alt="2" src="https://github.com/user-attachments/assets/6bf530b2-392e-4147-9520-0513750a2313" />

### 3. What country had the lowest average homicide rate?

```SQL
SELECT country, AVG (homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE sex = 'both'
AND age_group = 'ALL'
GROUP BY country
ORDER BY AVG(homicide_rate)
LIMIT 1;
```
<img width="248" height="61" alt="3" src="https://github.com/user-attachments/assets/91b7574c-002f-4662-aa62-6d86f4b9ffe0" />

### 4. What year had the highest global average homicide rate?

```SQL
SELECT year, AVG (homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE sex = 'both'
AND age_group = 'ALL'
GROUP BY year
ORDER BY AVG(homicide_rate) DESC
LIMIT 1;
```
<img width="214" height="60" alt="4" src="https://github.com/user-attachments/assets/a0084cfc-e2ff-4ab7-a445-d7e68f3d0097" />

### 5. What year had the lowest global average homicide rate?

```SQL
SELECT year, AVG (homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE sex = 'both'
AND age_group = 'ALL'
GROUP BY year
ORDER BY AVG(homicide_rate)
LIMIT 1;
```
<img width="213" height="58" alt="5" src="https://github.com/user-attachments/assets/7ccaa16a-bab2-4df3-b298-8c58f87afb15" />

### 6. What gender committed the highest average homicide?

```SQL
SELECT sex, AVG(homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE age_group = 'ALL'
AND sex != 'both'
GROUP BY sex
ORDER BY "Average Homicide Rate" DESC
LIMIT 1;
```
<img width="210" height="59" alt="6" src="https://github.com/user-attachments/assets/6caebfd6-8ee4-497f-95bd-5e902743d128" />

### 7. In what year did a female commit the highest average homicide?

```SQL
SELECT year, AVG (homicide_rate) AS "Average Homicide Rate"
FROM Homicide
WHERE sex = 'female'
AND age_group = 'ALL'
GROUP BY year
ORDER BY AVG(homicide_rate) DESC
LIMIT 1;
```
<img width="207" height="58" alt="7" src="https://github.com/user-attachments/assets/225200f5-15ae-4315-b197-cb3d40c81eda" />

## DASHBOARD VISUALIZATION IN EXCEL

<img width="1308" height="639" alt="AVERAGE HOMICIDE RATE" src="https://github.com/user-attachments/assets/db8388e5-c312-48a6-a75f-c9fe64a98677" />
