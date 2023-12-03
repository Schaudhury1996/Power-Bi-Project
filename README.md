# Pizza Sales Report

### Dashboard Link :https://app.powerbi.com/groups/me/reports/f2410fa6-3066-4543-8033-c67f31aebae1/ReportSection?experience=power-bi

## Problem Statement

This dashboard helps the Pizza sellers understand their customers better. It helps the Pizza sellers know if their customers are satisfied with their services. With the help of different visualizations based on their data, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the best and worst selling pizzas, so by using this dashboard they can identified this problem and can work on it.

Since,the Brie Carre pizza is the lowest selling pizza and generates lowest revenue among all other pizzas so they can work on this pizza to improve it or can replace it with a different kind of pizza.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is taken from SQL server.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 : Although in the pizza size column the initials were there so we changed initial 'L' to 'Large', 'M' to 'Medium', 'S' to 'Regular'.
- Step 6 : In the report view, under the view tab, card visuals are added to show all the KPIs.
- Step 7 : Column viewt was added to show the daily trends for total orders.
- Step 8 : Area view added to show the monthly trends for total orders.
- Step 9 : Two donut view was added to show the percentage of sales by pizza category and size.
- Step 10 : Finally a funnel view was added to show the total pizzas sold by pizza category. 
- Step 11 : In the report view, under the insert tab, two text boxes were added to the canvas where the insights of the 'Busiest days & times' and sales performance were analysed.
- Step 12 : Two buttons were added from elements group with the help of which you can go to the next page and check the best and worst pizzas analysis.
- Step 13 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & a slicer was added consisting of all the pizza categories and in another slicer the dates were added.
- Step 14 : Two Calculated column was created with the help of which we have fetched only the first 3 initials of days and months. 
- Step 15 : For creating new column following DAX expression was written;
       
        Order day = UPPER(LEFT(abcd[Day Name],3)) 
        Order Month = Upper(LEFT(abcd[Month Name],3))
        
Snap of new calculated column ,

![Snap 01](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/9232ef9a-cc0f-4254-874e-072478908524)
        
- Step 16 : New measure was created to find total revenue.

Following DAX expression was written for the same,
        
        Total Revenue = SUM(abcd[total_price])
        
A card visual was used to represent total revenue.

![Snap 2](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/7684f978-710a-41ff-89d8-049682d35b62)

        
 - Step 17 : New measure was created to find total orders.
 
 Following DAX expression was written to find total orders.
 
         Total Orders = DISTINCTCOUNT(abcd[order_id])
 
 A card visual was used to represent this.
 
 ![Snap 3](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/455fae9d-245f-4e59-9008-1b9b08e5acbe)

 
 - Step 18 : New measure was created to calculate the average order value.
 
 Following DAX expression was written to average order value,
 
         Avg order value = [Total Revenue]/[Total Orders]
    
 A card visual was used to represent this.
 
 
![Snap 4](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/313d6427-73ce-4210-bae6-860533b36c83)
 
  - Step 19 : New measure was created to calculate the average pizzas per order.
 
 Following DAX expression was written to average pizzas per order,
 
         Avg pizzas per order = [Total Pizzas Sold]/[Total Orders]
    
 A card visual was used to represent this.
 
 
![Snap 5](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/5c0647ba-a75d-4ffc-b676-ae057940bd0f)

 - Step 20 : The report was then published to Power BI Service.
 
 
![Snap 6](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/7e928b84-a214-4f7b-897b-f592de667286)


# Snapshot of Dashboard (Power BI Service)

![snap 7](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/64174054-455f-42b0-884f-61fe2663dfe1)

 
 # Report Snapshot (Power BI DESKTOP)

 
![snap 8](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/d47a660e-7b87-4541-b221-881fe04cde93)

![snap 9](https://github.com/Schaudhury1996/Power-Bi-Project/assets/152690681/c261077d-a53a-4756-9d29-4d47b0bd2723)



# Insights

Two page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Revenue = 817860.05

           
### [2] Average order value= 38.31

  
  ### [3] Average Pizza per order= 2.32


 ### [4] Some other insights
 
         Orders are highest on Thursdays, Fridays and Saturdays.
         
       
         Classic category(26.91%) and large size(45.89%) pizza contributes to maximum sales.

 ####     Best and worst selling pizzas

        The Thai chicken pizza generates the maximum revenue(43434.25).
        The Brie Carre pizza generates lowest revenue(11588.50).
