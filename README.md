# Blinkit Grocery

### Dashboard Link : https://app.powerbi.com/groups/me/reports/a8a9a3b5-c03b-474b-a542-b198932c7322/fc404cc718a7d7b3aa9f/

![Image](https://github.com/user-attachments/assets/6b735b13-1fa7-4642-91bc-9772dcbc88de)

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

## Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Item Weight".
- Step 5 : At this point replace the value of "low fat" as "Low Fat", "reg" as "Regular". Replace the _null_ value with "0" in the column "Item Weight".
- Step 6 :To redirect to the Power BI Desktop, click on "Close & Apply" from the File menu of the Power query 
- Step 7 : In the report view, under the Format pane, select the Yellow colour (#F9E061) for _Canvas Background_.
- Step 8 : Visual filters (Slicers) were added for one field named "Outlet Establishment Year".

  
![Image](https://github.com/user-attachments/assets/23fdb3ed-1e49-43f8-a8cf-a6db265cd986)
- Step 9 : In the report view, under the insert tab, using image option company's logo was added to the report design area at the left corner.
Here is the Logo:

![Image](https://github.com/user-attachments/assets/797d55de-4d4f-467c-abd2-018aa95e163e)
- Step 10 : Text box is inseted in the report to write the **TITLE** of the page. Make the duplicate of the page for four times and named thise as "Overview", "Outlet", "Sales" and "Visibility" consecutatively.
### Overview Page:
- Step 9 : Two card visuals were added to the canvas, one representing total sale and sales to visibility ratio in "Overview" page.
![Image](https://github.com/user-attachments/assets/8cb275e2-0fcf-4161-903c-cedf95389371)
- Step 10 : New measure is crated for **"Total Sale"**. DAX expression for "Sales" is mentioned here:
       
         Total Sale = SUM(Blinkit[Sales])
![Image](https://github.com/user-attachments/assets/57c33bf4-f4e2-4fb0-abdc-aa8282b4e2ca)
- Step 11 : **Sales to visibility ratio** is calculated through the following DAX expression. To display it in ratio format, set the custom format as **_"0:0"_** under _Format Options_. Insert the card visual to represt the ration on the report.

        Sales-to-Visibility Ratio = SUM(Blinkit[Sales]) / SUM(Blinkit[Item Visibility])
![Image](https://github.com/user-attachments/assets/9ee4d58d-bc21-44a1-9200-675409c0fa5f)
- Step 12 : Added Gauge visual to represent **Customer Satisfection.** To format the visual, set the gauge minimun axis as "1" and maximum axis as "5" as "4" was target value. 
Please see the snippet of the gauge meter.
![Image](https://github.com/user-attachments/assets/f4e84f4c-9814-4bca-a33c-cd3cc8fbdb87) 
- Step 13 : A pie chart was also added to the report design area representing the fat content of the items. While creating this visual, field named "Item fat Content" was also added to the Legends bucket. In time of formating the visual, yellow colour (#F9E061) is selected to refer "Regular" and green color (#008000) is chose for "Low Fat". Additional image is added to enhance the report view.

![Image](https://github.com/user-attachments/assets/f451b1e0-0e81-48e9-b708-ac94d4ac3ab9)
- Step 14 : The scattered chart is inserted to represent item visibility by sales. Sum of Item Visibility is plotted in X-axis and Sum of Sales is plotted in Y-Axis where the "Sales" is added in value field.

![Image](https://github.com/user-attachments/assets/bf55f69f-79f4-48dd-b5fc-446b86616bee)

### Outlet Page:
- Step 15 : A stacked column chart is used to represent the count of outlet identifiers by item type. The X-axis displays the item types, while the Y-axis represents the count of outlet identifiers. Conditional formatting is applied in the "Column" section for the fill color, where yellow indicates the minimum value and green represents the maximum value.

![Image](https://github.com/user-attachments/assets/94a4e474-4ef6-4b4c-95d7-ed4be948a6d0)
- Step 16 : A donut chart is inserted to display the outlet sizes. In this chart, green represents _small outlets_, yellow represents _high outlets_, and yellow-green represents _medium outlets_.

![Image](https://github.com/user-attachments/assets/8c579c3f-649b-4fdc-879e-4d2aa766caef)
- Step 17 : A stacked bar chart is used to represent the total sales based on outlet size. In this chart, green represents _small outlets_, yellow represents _high outlets_, and yellow-green represents _medium outlets_.

![Image](https://github.com/user-attachments/assets/5c892dc7-9ec7-4300-aa45-8fc0c6ab9f36) 


 ### Sales Page:
- Step 18 : A line chart has been implemented to represent sales based on the establishment year of the outlet. According to the analysis, total sales peaked in 2018.

![Image](https://github.com/user-attachments/assets/c7cf175d-c5c9-4c0e-910e-5dde4b4c3b5e)
- Step 19 : A donut chart is used to represent the total sales by outlet location. In this chart, green represents _Tire 3_, yellow represents _Tire 1_, and yellow-green represents _Tire 2_.

![Image](https://github.com/user-attachments/assets/4b041db1-785a-4073-b8ac-7fbe8955df70)
- Step 20 : Stacked bar chart is used to display the top 10 items by sales where sum of sales is plotted in the X-axis and item type is plotted in the Y-axis. To filter the top 10 item, click on "TOP N" for **"Filter Type"**. Now select "Top" to **"Show items"**.

![Image](https://github.com/user-attachments/assets/128723d0-7af5-4977-b295-317852e2eb1f)

- Step 21 : Stacked bar chart is used to display the bottom 10 items by sales where sum of sales is plotted in the X-axis and item type is plotted in the Y-axis. To filter the bottom 10 item, click on "BOTTOM N" for **"Filter Type"**. Now select "Bottom" to **"Show items"**. 

![Image](https://github.com/user-attachments/assets/000fbba8-9b4f-48e8-a9b0-4ea305c86308)

 ### Visibility Page:
- Step 22 : The Power BI Q&A feature is used to create a matrix table that displays the visibility of item identifiers based on the outlet. The Item Identifier is placed in the Rows field, the Outlet Identifier is placed in the Columns field, and the Sum of Item Visibility is assigned to the Values field.

![Image](https://github.com/user-attachments/assets/cc9c8203-048c-4c65-84f2-eb3d1a1dca96)

 - Step 23 : The report was then published to Power BI Service.
   
![Image](https://github.com/user-attachments/assets/35503332-354c-4062-81ce-f03197ad3c9c)

# Used DAX expression in Blinkit Report:
- Average Sales per Item:

        Average Sales per Item = SUM(Blinkit[Sales])/COUNT(Blinkit[Item Identifier])
- Sales Contribution Percentage by Outlet = 

        Sales Contribution Percentage by Outlet = SUM(Blinkit[Sales])/CALCULATE(SUM(Blinkit[Sales]), ALL(Blinkit[Outlet Identifier]))*100
- Sales-to-Visibility Ratio 

        Sales-to-Visibility Ratio = SUM(Blinkit[Sales]) / SUM(Blinkit[Item Visibility])
- Total Sale 

      Total Sale   = SUM(Blinkit[Sales])

 # Snapshot of Dashboard (Power BI Service)

## Overview
![Image](https://github.com/user-attachments/assets/28494b99-ea03-4992-b7ee-764cdbd62cf4)
## Outlet
![Image](https://github.com/user-attachments/assets/f9206eb6-9e63-4cef-828e-04980e6d012d)
## Sales
![Image](https://github.com/user-attachments/assets/f38c197e-f792-48f2-b8f6-8a72f6be9b9b)
## Visibility
![Image](https://github.com/user-attachments/assets/38576639-7ca2-4aa3-bfc8-fd8a5b03269a)

 
 # Report Snapshot (Power BI DESKTOP)

 ## Overview
![Image](https://github.com/user-attachments/assets/6ef39721-2947-416a-9857-06b0636e05d5)
## Outlet
![Image](https://github.com/user-attachments/assets/93e3382c-002e-4dc3-980d-b475a510ccfa)
## Sales
![Image](https://github.com/user-attachments/assets/458e1587-bdf1-47e3-a26f-4d6c43e75076)
## Visibility
![Image](https://github.com/user-attachments/assets/88ad06cd-0eae-4c01-a544-8b3f9fe339e0)

## Insights and Conclusion:
The analysis of Blinkit's fictional grocery data reveals key trends in customer satisfaction, product composition, outlet distribution, and sales performance. The average customer satisfaction stands at 3.92, slightly below the target of 4.0, indicating a need for improvements in service or product offerings. Low-fat items dominate the grocery segment, accounting for approximately 64% of total products. Additionally, medium-sized outlets are the most common and have contributed the most to total sales, likely due to their balanced capacity and accessibility. A significant concentration of grocery outlets is observed in Tier-3 cities, suggesting a focus on expanding market reach in smaller urban areas. The highest total sales were recorded in 2018, marking a peak performance year. Among product categories, fruits and vegetables are the best-selling items, while seafood ranks the lowest in sales. These insights provide a strategic foundation for optimizing product offerings, improving customer satisfaction, and enhancing sales performance in targeted regions.
## Improvement Areas:
- **Enhancing Customer Satisfaction** – With the rating of 3.92 against the target of 4.0, there is room for improvement in service quality, product availability, and customer engagement. Collecting feedback and implementing loyalty programs or personalized promotions can help bridge this gap.

- **Optimizing Outlet Size and Distribution** – While medium-sized outlets contribute the most to sales, assessing the potential of small and large-sized stores in different regions may help improve overall performance. Additionally, expanding into Tier-1 and Tier-2 cities can create new revenue streams.

- **Boosting Sales in Underperforming Categories** – Seafood ranks lowest in sales, suggesting the need for better marketing, improved supply chain management, and promotional offers to increase demand.

- **Sustaining Sales Growth Beyond 2018** – Since 2018 was the peak year for total sales, analyzing the factors behind its success (such as pricing strategies, promotions, or seasonal demand) can help replicate this growth in the future.
