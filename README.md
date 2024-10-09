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

```sql
    SELECT * 
    FROM `country-data`;
```
2. **Print out the content of the country, child_mort, and gdpp, only output 5 rows**:

```sql
    SELECT country, child_mort, gdpp
    FROM `country-data`
    LIMIT 5;
```
3. **Select all the columns of the dataset where infiation is less than 10**:

```sql
    SELECT *
    FROM `country-data`
    WHERE inflation < 10;
```
4. **Output the first 8 countries whose income is between 10000 and 25000**:

 ```sql
     SELECT country,income
     FROM `country-data`
     WHERE income BETWEEN 10000 AND 25000
     LIMIT 8;
 ```
 5. **Show 5 countries with the lowest child_mort**

```sql
    SELECT country, child_mort
    FROM `country-data`
    ORDER BY child_mort
    LIMIT 5;
```
6. **Select countries whose life-expentancy is greater than 70 or equal to 70**:

```sql
    SELECT *
    FROM `country-data`
    WHERE life_expec >= 70;
```
7. **Select countries whose inflation is less than or equal to 25**

```sql
    SELECT country, inflation
    FROM `country-data`
    WHERE inflation <= 25;
```
8. **Select countries whose inflation is greater than or equal to 8 but less than 20**:

```sql
    SELECT country, inflation
    FROM `country-data`
    WHERE inflation >= 8 AND inflation < 20;
```
9. **Print out all the data print for Albania**:

```sql
    SELECT *
    FROM `country-data`
    WHERE country = 'Albania';
```
10. **Print out all the data points excluding for Algeria, Albania, Angela, Australia, Austria, Armenia, Bahamas and Belgium**:

```sql
    SELECT *
    FROM `country-data`
    WHERE country != 'Algeria';
```
11. **Determine the total number of records in the dataset**:

```sql
    SELECT COUNT(*)
    FROM `country-data`;
```
12. **Select 6 countries, exports, health, income that end with the letter y**:

```sql
    SELECT country, exports, health, income
    FROM `country-data`
    WHERE country LIKE '%y'
    LIMIT 6;
```

13. **Select the data points for the following countries only, Austria, Armenia, Bahamas, Belgium**:

```sql
    SELECT *
    FROM `country-data`
    WHERE country IN ('Austria','Armenia','Bahamas','Belgium');
```
14. **Select only countries that have an inflation in the range of 5 to 15**:

```sql
    SELECT country, inflation
    FROM `country-data`
    WHERE inflation BETWEEN 5 AND 15;
```
15. **Select all the data points for the following countries only Austria and Armenia**:

```sql
    SELECT *
    FROM `country-data`
    WHERE country IN ('Austria','Armenia');
``` 
16. **Select countries whose child_mort is less than 10 and inflation is above 15**:

```sql
    SELECT country, child_mort, inflation
    FROM `country-data`
    WHERE child_mort < 10 AND inflation > 15;
```
17. **Print out all the data point excluding for Angola (CTE) Australia, Austria, Bahamas, Belgium**:

```sql
    With data_CTE as (
    SELECT *
    FROM `country-data`
    WHERE country IN ('Austria','Angola','Bahamas','Belgium', 'Australia')
    )
    
    SELECT *
    FROM data_CTE
    WHERE country NOT IN ('Angola');
```
