# Blinkit Grocery

### Dashboard Link : https://app.powerbi.com/groups/me/reports/a8a9a3b5-c03b-474b-a542-b198932c7322/fc404cc718a7d7b3aa9f/

## Problem Statement

This project focuses on analyzing fictional data from Blinkit, an online grocery delivery service, to extract valuable insights using Power BI. The dataset provides information on various parameters such as product demand, delivery trends, customer behavior, and operational efficiency. The goal is to transform raw data into meaningful visualizations that aid decision-making.

## Tool Used:
- Power BI Desktop
- Power Query
- Q&A Feature

## Files Included

### Blinkit .csv: 
Contains raw transactional data with details on orders, delivery times, customer preferences, etc.

### Blinkit .pbix: 
Power BI report file with interactive dashboards and visualizations on overview, outlet, sales, and visibility based on the dataset. 

## Blinkit Sheet:
- Item Fat Content: Categorization of the fat content of the grocery items (e.g., Low Fat, Regular).
- Item Identifier: Unique identifier for each grocery item in the dataset.
- Item Type: Category or type of the grocery item (e.g.- Dairy, Frozen Foods, Snacks).
- Outlet Establishment Year: Year when the outlet (store) was established.
- Outlet Identifier: Unique identifier for each outlet (store) in the dataset.
- Outlet Location Type: Type of location where the outlet is situated (e.g., Urban, Rural).
- Outlet Size: Size of the outlet (e.g., Small, Medium, High).
- Outlet Type: Type of outlet (e.g., Grocery Store, Supermarket).
- Item Visibility: Percentage of total display area of the item in the store.
- Item Weight: Weight of the item.
- Sales: Sales of the item in the given time period.
- Rating: Customer rating or feedback score for the item or the outlet.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Item Weight".
- Step 5 : At this point replace the value of "low fat" as "Low fat", "reg" as "Regular". Replace the _null_ value with "0" in the column "Item Weight".
