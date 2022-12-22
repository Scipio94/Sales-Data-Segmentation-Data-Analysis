## SQL Syntax for segmentation analysis

~~~SQL
/*Dataset Calculations*/

SELECT 
  COUNT (DISTINCT ORDERNUMBER) AS CustomersCount, COUNT(DISTINCT PRODUCTLINE) AS Products, COUNT (DISTINCT COUNTRY) AS CountryCount, COUNT (DISTINCT TERRITORY) AS TerritoryCount , COUNT (DISTINCT CITY) AS CityCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE status = 'Shipped';

/* Total and Average amount of sale grouped by country - filtering for all orders shipped*/

SELECT  COUNTRY, ROUND(SUM(SALES),2) AS TotalCountrySales, ROUND(AVG(SALES),2) AS AvgCountrySales,ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSaleMSRPComp, 
ROUND(SUM(sales) - SUM (msrp * QUANTITYORDERED),2) TotalSaleMSRPComp
,COUNT (SALES) AS SaleCountCountry
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` 
WHERE status = 'Shipped'
GROUP BY country
ORDER BY TotalCountrySales DESC;
--USA accounted for the most sales


/* Total and Average amount of sales grouped by territory for all orders shipped */

SELECT territory, ROUND(SUM(SALES),2) TotalTerritorySales ,ROUND(AVG(SALES),2) AS AvgTerritorySales, ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSaleMSRPComp, ROUND(SUM(sales) - SUM (msrp * QUANTITYORDERED),2) TotalSaleMSRPComp,COUNT (sales) AS SaleCountTerritory
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data` 
WHERE status = 'Shipped'
GROUP BY TERRITORY
ORDER BY AvgTerritorySales DESC;


/* Total and Average amount of sales by grouped by city data set filtered for all orders shipped*/

SELECT city, country, ROUND(SUM(SALES),2) TotalCitySales,ROUND(AVG(sales),2) AvgCitySales,ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSaleMSRPComp, ROUND(SUM(sales) - SUM (msrp * QUANTITYORDERED),2) TotalSaleMSRPComp,
COUNT (sales) CitySaleCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE status = 'Shipped'
GROUP BY city, country
ORDER BY AvgCitySales DESC
LIMIT 10 ;

/* Total and average price grouped by prodcut and calculation of the difference between Sale price and MSRP of all orders shipped*/

SELECT PRODUCTLINE, ROUND(SUM(sales),2) AS TotalProductSale, ROUND(AVG(sales),2) AS AvgProductSale,
ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSaleMSRPComp, ROUND(SUM(sales) - SUM (msrp * QUANTITYORDERED),2) TotalSaleMSRPComp,
COUNT(sales) AS ProductSaleCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE status = 'Shipped'
GROUP BY PRODUCTLINE
ORDER BY TotalProductSale DESC;
--Classic cars the most profitable product


/* Total and average price of products group by product and country and difference between sale price and MSRP of all orders shipped*/

SELECT country, TERRITORY,PRODUCTLINE, ROUND(SUM(sales),2) AS TotalProductSaleCountry, ROUND(AVG(sales),2) AS AvgProductSaleCountry,
ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSalesCountryMSRPComp, ROUND(SUM(sales) - SUM(msrp * QUANTITYORDERED),2) AS TotalSalesCountryMSRP, COUNT(sales) AS SaleCoutryCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE status = 'Shipped'
GROUP BY country, TERRITORY,productline
ORDER BY TotalProductSaleCountry DESC;
-- Classic cars sold in the US most profitable product

/* Total and average price of products grouped by city and country filtered by order status shipped with MSRP calculation*/

SELECT city,country, PRODUCTLINE, ROUND(SUM(sales),2) AS TotalProductSaleCity, ROUND(AVG(sales),2) AS AvgProductSaleCity,
ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSalesCityMSRPComp, ROUND(SUM(sales) - SUM(msrp * QUANTITYORDERED),2) AS TotalSalesCityMSRP, COUNT(sales) AS SaleCityCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE status = 'Shipped'
GROUP BY city,country, productline
ORDER BY TotalProductSaleCity DESC
LIMIT 50;


/* Total and average price of products grouped by territory filtered by order status shipped with MSRP calculation*/

SELECT TERRITORY, PRODUCTLINE, ROUND(SUM(sales),2) AS TotalProductSaleTerritory, ROUND(AVG(sales),2) AS AvgProductSaleTerritory,
ROUND(AVG(sales) - AVG(msrp * QUANTITYORDERED),2) AS AvgSalesTerritoryMSRPComp, ROUND(SUM(sales) - SUM(msrp * QUANTITYORDERED),2) AS TotalSalesTerritoryMSRP, COUNT(sales) AS SaleTerritoryCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE status = 'Shipped'
GROUP BY TERRITORY, productline
ORDER BY TotalProductSaleTerritory DESC;
-- EMEA the largest territory market for classic cars

/* Average Sale Amount */
SELECT ROUND(AVG(SALES),2) AS AvgSale
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`;


/*Dealsize and MSRP Calculations*/
SELECT DEALSIZE, ROUND(SUM(sales),2) AS TotalSales,ROUND(AVG(sales),2) AS AvgSales,ROUND(SUM(sales),2) - ROUND(SUM(MSRP * QUANTITYORDERED),2) AS TotalSalesMSRP,
  ROUND(AVG(sales),2) - ROUND(AVG(MSRP * QUANTITYORDERED),2) AS AverageSalesMSRP,
  COUNT(SALES) AS DealsizeCount
FROM `my-data-project-36654.Kaggle_sales_dataset.Sales_Data`
WHERE STATUS = 'Shipped'
GROUP BY DEALSIZE;


~~~
