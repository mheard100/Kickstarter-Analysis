# Kickstarter-Analysis
Performing analysis on Kickstarter data to uncover trends

# Kickstarting with Excel

## Overview of Project
	Louise had a play *Fever* that came close to its fundraising goals. She wanted to know how other fundraising goals
	faired based on launch dates and fundraising goals. The dataset Kickstarter was used to visualize campaign outcomes 
	based on the launch dates and fundraising goals. Pivot tables and Excel formulas were used in tandem to extract information
	from the provided dataset to create visuals that are used to provide details on what helps makes successful fundraisers and 
	to make other conclusions based on what the results are. Louise can use the results to start a fundraiser that have increased 
	odds of succeeding 
### Purpose
	The purpose of this analysis is to use the power of Excel to extract data and use it to make visuals that can be used to draw conclusions. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

	# Pivot Table
	A pivote table was used to analyze "successful," "failed," and "canceled" campaigns based on launch date. In addition 
	to the already provided dataset, a new column was added titled "Years." In the top cell, the year() function was used
	to extract the year from the Date Created Conversion column. The Date Created Version column converted the date a 
	fundraiser started from unix timestamp to a calendar date. From there, a pivot table was inserted on a new excel sheet
	named "Theater Outcomes By Launch Date." Count of outcomes was used for values because that is what
	Louise wants to quantify. The legend field also contains outcomes while the axis field has the Date
	Created Conversion. The pivot table was filtered by year and Parent category where "Theater" was 
	selected. 

	##Visual
	While the pivot table created shows the story we are looking for, it is easier for the human brain
	to see and assess a visual chart. A line chart was inserted showing "successful," "failed," and "canceled."
	The x axis is the month and the y axis is the amount of Theater Outcomes. 
	

### Analysis of Outcomes Based on Goals

	#Selecting Wanted Data

	In a new excel sheet, columns for Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage
	Successful, Percentage Failed, and Percentage Canceled were created with rows for <1000, 1000 to 4999, 5000 to 9999, 
	1000 to 14999, 15000 to 19999, 20000 to 24999, 25000, to 29999, 30000 to 34999, 4000 to 44999, 45000 to 49999, and
	Greater than 50000 that represent goal money. The CountIFS() function was used to bring over and sort the data for all 
	the row values for Number Successful, Number Failed, and Number Canceled from the data set for plays. Total Projects was 
	calculated using the sum() function by row. Percentages were then calculated for by taking the number of outcomes by total projects
 	multipled by 100 for each respective outcome. 

	##Visual 
	
	A line graph was inserted to show the % of successful, failed, and canceled for all goal money ranges. 
	
### Challenges and Difficulties Encountered

	#Outcomes Based on Launch Date

	For the this section of the analysis, success, failed, and canceled where looked at as outcomes. There
	is another category for live fundraisers. This category needed to be excluded to get the correct numbers
	for total the Grand Total and to correcting populate the graph. This is something I failed to notice immediately.
	

	##Outcomes Based on Goals

	For the CountIFS() function when sorting by the intervals of goal money, I had incorrect < > usage originally.
	This caused my totals to be off. It is important to correctly go through and double check the formulas for 
	correctness. 
	
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

	May and June are the best months to start a fundraiser for Theater while November, December are the worst month to start one.
	
- What can you conclude about the Outcomes based on Goals?

	Lower goals have the most success. Less than $4999 is the best range with over 70% successful. Furthermore, plays had no cancelations
	in our dataset. 

- What are some limitations of this dataset?

	One major limitation of this dataset is how the fundraising was done. Could fundrasing methods drive the success of fundraisers?
	Also, we have the country where these fundraisers happened. Could city or area be an influential factor in the success of a 
	fundraiser? In all, the dataset could have more comprehensive information. 

- What are some other possible tables and/or graphs that we could create?

	A clustered Column Chart would be useful for Theater Outcomes by Date showing total outcomes by type by month. A 100$ stacked column chart 
	would be useful instead of the line chart for Outcomes Based on Goals. This type of chart can easily show
	outcomes as a percentage of a whole. Also, we could have looked at Theater Outcomes by Country and Outcomes based on amount of backers
	as interesting ways to analyze success on fundraising. 
