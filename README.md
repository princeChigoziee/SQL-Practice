# SQL-Practice
## Country Data Analysis SQL Project

## Project Overview
**Project Title**: Country Data Analysis

**Database**: `country_db`

This project is designed to demonstrate my SQL skills and techniques typically used by data analysts. The project involves a country database and it was use to showcase my performance, exploratory data analysis (EDA) and answering some specific SQL queries.

## Project Structure
### Data Analysis & Finding
The following SQL queries were developed to answer specific questions:

1. **Select all the coloumns in the country data tutorial**

```
    SELECT * 
    FROM `country-data`;
```
2. **Print out the content of the country, child_mort, and gdpp, only output 5 rows**:

```
    SELECT country, child_mort, gdpp
    FROM `country-data`
    LIMIT 5;
```
3. **Select all the columns of the dataset where infiation is less than 10**:

```
    SELECT *
    FROM `country-data`
    WHERE inflation < 10;
```
4. **Output the first 8 countries whose income is between 10000 and 25000**:

 ```
     SELECT country,income
     FROM `country-data`
     WHERE income BETWEEN 10000 AND 25000
     LIMIT 8;
 ```
 5. **Show 5 countries with the lowest child_mort**

```
    SELECT country, child_mort
    FROM `country-data`
    ORDER BY child_mort
    LIMIT 5;
```
6. **Select countries whose life-expentancy is greater than 70 or equal to 70**:

```
    SELECT *
    FROM `country-data`
    WHERE life_expec >= 70;
```
7. **Select countries whose inflation is less than or equal to 25**

```
    SELECT country, inflation
    FROM `country-data`
    WHERE inflation <= 25;
```
8. **Select countries whose inflation is greater than or equal to 8 but less than 20**:

```
    SELECT country, inflation
    FROM `country-data`
    WHERE inflation >= 8 AND inflation < 20;
```
9. **Print out all the data print for Albania**:

```
    SELECT *
    FROM `country-data`
    WHERE country = 'Albania';
```
10. **Print out all the data points excluding for Algeria, Albania, Angela, Australia, Austria, Armenia, Bahamas and Belgium**:

```
    SELECT *
    FROM `country-data`
    WHERE country != 'Algeria';
```
11. **Determine the total number of records in the dataset**:

```
    SELECT COUNT(*)
    FROM `country-data`;
```
