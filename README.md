# Sales Segementation Analysis

## Abstract

Sales dataset found on Kaggle of what is presumed to be the sales data of a multinational corporation. The dataset contains sales data of 307 distinct orders, 287 of which have been shipped, 7 products, 73 cities, 19 countries, and 4 territories. The goal of this analysis is to explore the consumer segmentation trends within the dataset based on a variety of variables. 

***Access Dataset [HERE](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data)***

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

