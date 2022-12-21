## SQL Syntax for variable calculations

~~~SQL
/* List and count of distinct countries in the data set */

SELECT DISTINCT country
 FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` 
 ORDER BY country DESC;
 


SELECT COUNT(DISTINCT country) AS CountryCount
 FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`;


 /* List and count of distinct cities and distinct countries in the data set*/

 SELECT DISTINCT city , country, count(city) OVER (PARTITION BY country) AS CityCount
 FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` 
 GROUP BY country, city
 ORDER BY country DESC;

 SELECT COUNT(DISTINCT city) AS TotalCityCount
 FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`;



/* List of distinct territories of customers in the data set */

 SELECT DISTINCT territory
 FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`;



/* List of deal size and sales range*/

SELECT DISTINCT DEALSIZE, MIN(sales) AS low_amount,MAX(sales) AS high_amount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` 
GROUP BY DEALSIZE;
 
/* List of order statuses in the data set */

SELECT DISTINCT status
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`;

/* Count of Distinct Customers in the dataset */

SELECT COUNT (DISTINCT ORDERNUMBER) AS customer_count
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` ;



/* Count of Distinct Customers in the dataset with an order status of shipped */

SELECT COUNT (DISTINCT ORDERNUMBER) AS customer_count
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` 
WHERE Status = 'Shipped' ;

~~~
