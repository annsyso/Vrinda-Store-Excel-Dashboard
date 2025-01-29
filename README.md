# Vrinda-Store-Excel-Dashboard

Objective - the Vrinda store wants to create an annual sales report to understand their customers and grow their sales for the next year. Looking at data from 2022 for predictions for 2023.

Sample questions for the analysis and dashboard in clude: which month got the highest sales and orders? who purchased more based on gender? what are the top states contributing to orders? which channel has the greatest ROI for sales? What is the highest selling category? etc.

1. Data Cleaning    - first we want to duplicate the raw data so we always have something to look back on in case anything goes wrong. Next, to look at duplicates and remove any before we get started on cleaning.
   - next, filter on all of the column categories to see what we are working with for the data and estimate that columns we will need to clean. Some things of note is different strings denoting gender. Case of some strings in the item column. Qty is both integer and string. and case cleaning for the ship city.
   - For the gender changing, can either do a simple find and replace or write an IF formula and create a new, cleaned column. '=IF(E2="W", "Women", E2)'. This is the same process for the quantity column where there is a mix for strings and integers.

2. Data Processing
   - first, we are going to look at the correlation between gender and age. We want to make a new column to create age groups to more easily divide everything up. This involves creating a new column and using nested conditional IF statements to bucket out the different groups.
   -   `=IF(E2>=50, "Senior",IF(E2>=30,"Adult","Teenager")`
  
   -   Next it is helpful to isolate the months to eventually be able to analyze which months have higher vs. lower sales. I do this by creating a new column and then using a formula to isolate the month. `=IF(H2=1,"Jan",IF(H2=2,"Feb",IF(H2=3,"Mar",IF(H2=4,"Apr",IF(H2=5,"May",IF(H2=6,"Jun",IF(H2=7,"Jul",IF(H2=8,"Aug",IF(H2=9,"Sep",IF(H2=10,"Oct",IF(H2=11,"Nov",IF(H2=12,"Dec",""))))))))))))'

3. Data Analysis
- first I make a pivot table on a seperate sheet that has the months as rows and then the sum total of orders and the count total of orders for each month. From there, I create a pivot combo chart with 2 axis that show the total sales using a bar chart and the total count of orders using a line chart.
- 
