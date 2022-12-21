# Sales Segementation Analysis

## Abstract

Sales dataset found on Kaggle of what is presumed to be the sales data of a multinational corporation. The dataset contains sales data of 307 distinct orders, 287 of which have been shipped, 7 products, 73 cities, 19 countries, and 4 territories. The goal of this analysis is to explore the consumer segmentation trends within the dataset based on a variety of variables. 

***Access Dataset [HERE](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data)***

***Access Tableau Visual [HERE](https://public.tableau.com/views/SalesDataSegmentationViz/SalesDataSegmentation?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)***

## Objective

The objective of this analysis is to identify trends in consumer segmentation based on the consumer location of all orders that have a status of shipped. 

## Variables

There are several variables that will affect the outcome of this analysis:

- Country: Country the order is being shipped to
- City:  The city of the customer 
- Territory: Regions of the world the country is located in. 
  - EMEA: Europe, Middle East, and Africa
  - NA: North America
  - Japan 
  - APAC: Asia Pacific
- Deal Size: Grouping of the sale by range of money spent by customer 
  - Large: Sales greater than  $7,000 
  - Medium: Sales between $3,000 and $6,999.99
  - Small: Sales less than $3,000
- Status: Order status
  - Shipped: Order was shipped to customer 
  - Resolved: There was an issue with the order but it was resolved
  - On Hold: Order has been placed but payment not processed
  - Canceled:The order was canceled
  - In Process: The order is currently being processed
  - Disputed:There is a dispute regarding funds for the order
- MSRP: Manufacturer Suggested Retail Price

# Analysis 

## Segmentation Analysis: City


![City Heat Map Dashboard Total Sales ](https://user-images.githubusercontent.com/112409778/208795405-fb71e283-5a9f-4371-8fd8-7d772122015e.jpg)

Madrid, Spain generated the highest total sales revenue with 258 sales totaling $911,769.83 and an average sale of $3,533.99, categorized as a medium sized deal. San Rafael, USA generated the second highest revenue with  178 sales totaling $647,596.31 and an average sale of $3638.18, categorized as a medium sized deal. 50% of the cities in the top ten in total sales were from the USA and North America.


![City Heat Map Dashboard Avg Sales ](https://user-images.githubusercontent.com/112409778/208795270-d08b76be-0c4f-4991-833e-4887fbaf2a9b.jpg)

New Haven, USA had the highest average sale amount, $4,674.83, of all the cities in the data set. Liverpool, UK had the second highest average sale amount, $4,506.67, of all the cities in the dataset. Both average sale amounts are categorized as medium sized deals. Half of the cities in the top ten average sales are from the USA and North America.

### Segmentation Analysis: Country

![Heat Map Dashboard Country Total Sales](https://user-images.githubusercontent.com/112409778/208795620-6a9dd802-e5b3-4227-87c8-c877b751aa58.jpg)

The USA has the highest sales total, $3,372,204.28, and the most orders of any country in the database accounting for more than a third of orders and total revenue generated. France has the second highest sales total, $1,067,131.83, and the second most orders accounting for 301 orders. Additionally, there is a direct correlation between the number of orders of a country and the total revenue, the higher the number of orders the higher the more revenue generated. 

![Heat Map Dashboard Country Avg Sales ](https://user-images.githubusercontent.com/112409778/208949587-ac7ef9ab-de3c-4edd-9b77-a40c518b36eb.jpg)

Sweden had the highest average sale amount, each sale averaging $3858.37. Sweden had the second highest sales average, $3797.21. Countries in Europe, the Middle East, and Africa accounted for more than half of the top ten countries with the highest sales averages in the dataset. 


## Segmentation Analysis: Territory

![Territory Heat Map Dashboard ](https://user-images.githubusercontent.com/112409778/208951441-0d1307b0-1a3f-4126-ab50-bcf4e674431b.jpg)

Despite America accounting for more than a third of the total sales and revenue generated in the dataset, the EMEA territory had the highest total sales revenue totaling $4,552,272.71 more nearly half of the revenue generated in the dataset. North America had the second highest total in total sales totaling $3,596,282.84. Additionally, there was a positive correlation between the count of sales in each territory and the revenue generated, the higher the sale count, the higher the sale revenue. 

![Territory Heat Map Average Sales ](https://user-images.githubusercontent.com/112409778/208951498-3d238b27-0754-494e-8815-57f267d2061a.jpg)


Japan had the highest average sales out of all the territories, each sales was an average of $3761.76. North America had the second highest average sales, each sale was an average of $3,578.39

## Segmentation Analysis: Dealsize

![Total Sale MSRP Dealsize ](https://user-images.githubusercontent.com/112409778/208952158-f7940d6b-b612-4e67-ab8a-22296184cdae.jpg)

Medium sized deals had the highest total MSRP totaling $157,984.52 in additional revenue above the recommended price. There was also a positive correlation between the number of sales and total revenue.


![Average Sale MSRP Dealsize](https://user-images.githubusercontent.com/112409778/208952207-164d77c0-caa1-4856-9f6c-8d2a9e8c9b32.jpg)

Majority of the orders shipped were considered to be medium sized deals, between the sale range $3,000 and $6,999.99, and had an average sale price of $3,550.44. Additionally, medium sized orders also accounted for the majority of the shipped orders revenue totaling $5,633,596.52 with an average sale of $4,408.13. However, on average large sized deals, more than $7,000 had the highest MSRP, averaging an additional $966.50 per sale. 

![Sales Count Histogram](https://user-images.githubusercontent.com/112409778/208952360-0d20f539-4487-4f05-b6da-5a4b3ae0a9ff.jpg)

The Average sale amount irregardless of city, state, and territory of the dataset is $3553.89 which makes the deal size medium. This is reflected in the right-skewed histogram. Large deal sizes are outliers, majority of the sales made with a status order of shipped were medium deal sizes. So, medium sized deals were the most profitable in the dataset. 






