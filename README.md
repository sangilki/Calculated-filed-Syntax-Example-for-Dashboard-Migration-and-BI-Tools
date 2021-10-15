# Dashboard-Migration
Code Syntax Reference for Cross Visualization tools Migration

**BI Tools - Calculated filed Syntax/Example 	**

**Tableau:**

IF [Profit per Day] > 000 THEN "Highly Profitable"
ELSEIF [Profit per Day] <= 0 THEN "Unprofitable"
ELSE "Profitable"
END
	
  
**Power BI	**
Price Group =
IF(
    'Product'[List Price] < 500,
    "Low",
    "High"
)

Data Analysis Expression (DAX) language: 	

**Amazon Quicksight**
ifelse(salesTotal >= 0 AND salesTotal < 500, 'Group 1', salesTotal >= 500 AND salesTotal < 1000, 'Group 2', 'Group 3')	

**GCP Studio	**
IF(DATETIME_DIFF(TODAY(),Date,DAY) > 60, "old","new")	

**IBM Cognos Analytics**
if ("Net Income" <100000) then 
("Gross Profit"*1.25) else
NULL


![Code Syntax - BI Tools](https://user-images.githubusercontent.com/87334029/137420817-9b1dd83e-c68b-46a2-9e9c-9666eeb336c7.png)
