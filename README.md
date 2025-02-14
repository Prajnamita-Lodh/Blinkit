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

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Item Weight".
- Step 5 : At this point replace the value of "low fat" as "Low Fat", "reg" as "Regular". Replace the _null_ value with "0" in the column "Item Weight".
- Step 6 :To redirect to the Power BI Desktop, click on "Close & Apply" from the File menu of the Power query 
- Step 7 : In the report view, under the Format pane, select the Yellow colour (#F9E061) for _Canvas Background_.
- Step 8 : Visual filters (Slicers) were added for one field named "Outlet Establishment Year".
![Image](https://github.com/user-attachments/assets/23fdb3ed-1e49-43f8-a8cf-a6db265cd986)
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
