# An Analysis of Kickstarter Campaigns.

### An Excel workbook showcasing statistical analysis of successful, failed, canceled, and live Kickstarter campaigns.

## Overview of Project

### In this project, an Excel file containing a large dataset of Kickstarter campaigns was analyzed. Kickstarter is a crowdfunding platform that has become very successful at manifesting projects from imagination, to reality, via backers that fund projects they believe in. Powerful Excel tools and techniques were learned and used to build a better picture of Kickstarter campaigns for a client named Louise. Filters, conditional formattting, pivot tables, formulas like ROUND, IFERROR, COUNTIFS, SUM, AVERAGE, MEDIAN, STDEV.P, QUARTILE.EXC, and VLOOKUP were used to help build a data story for Louise to launch a Kickstarter campaign with a higher probability of success.

## Analysis and Challenges
### To begin analyzing a large dataset such as this Kickstarter workbook it was essential to hone in on what the client Louise wanted to achieve. The client wanted to look in to campaign data specifically in the category of theatre and then deeper into the subcategory of plays. To do this, the workbook's Category and Subcategory column was separated into two individual columns called Parent Category and Subcategory, where the Parent Category could be filtered to show just "theatre" and the Subcategory could be filtered to show just "plays."

![image](https://user-images.githubusercontent.com/27036669/138611094-dab8cd49-93a9-4912-8360-e479470c376a.png)

### From here, the Kickstarter data was split into two worksheets where one held the data of all failed campaigns and the other held the data of all the successful campaigns. Descriptive statistics of mean, median, std. dev, upper quartile, lower quartile, and interquartile range were calculated for the successful campaigns and failed campaigns. From the statistical data given, we learned that Louise needs to lower her goal amount of $12,000 to something closer to the mean successful goal amount of $5,049. Failed campaigns had the tendency of having goals that were overextended and pledge deviations of large spread. 

![image](https://user-images.githubusercontent.com/27036669/138615048-bf155014-0d4a-4b1a-b81e-de80f6b3c2d2.png)

### By using a pivot table with time in months as the independent variable and the outcome value as the dependent variable we created a line graph titled, "Theatre Outcomes Based on Launch Date." Filtering the Parent Category to only "theatre," and types of outcomes to successful, failed, and canceled, we could see that launching a theatre Kickstarter between late April and the middle of June would be a statistical advantage. 

![image](https://user-images.githubusercontent.com/27036669/138615215-bdfaf379-1abc-4206-9396-fbd02de44d72.png)

### Creating a column of Kickstarter goal ranges, i.e, "Less than 1000," "20,000 to 24,999," and "Greater than 50,000," we calculated the number of successful, failed, canceled, and total projects within goal ranges. We then calculated the percentage of successful, failed, and canceled campaigns with respective goal ranges. The resulting data was represented in a line graph with the independent variable being goal ranges and the dependent variable being outcome percentages for successful, failed, and canceled campaigns seen below.

![image](https://user-images.githubusercontent.com/27036669/138615367-0a27af25-8114-4df5-8bc5-264171109eb2.png)

### The biggest hurdle I had during this data analysis was using the COUNTIFS formula, not for the Less than 1000 or the Greater than 50000 rows, but for the rows in between them. I wasn't putting the third <= criteria range in the right place, after the Kickstarter!$F:$F, "outcome", criteria, with the first criteria being the =COUNTIFS(Kickstarter!$D:$D, ">=1000", for example.

## Results

### - What are two conclusions you can draw about the Outcomes based on Launch Date?

#### From the Outcomes Based on Launch Date line chart we concluded that launching a theatre campaign between late April and the middle of June would be a statistical advantage. I also see that when overlayed, the failed outcome and successful outcome lines show a close correlation in the time domain, with a divergence in correlation in December. No theatre campaigns were canceled in October which is interesting in its own right.

### - What can you conclude about the Outcomes based on Goals?

#### The Outcomes Based on Goals line chart was from data of the "play" subcategory. We can see that none of the play campaigns were canceled and the data all lies on the 0% outcome percentage. The Percentage Failed line shows that campaigns became more likely to fail as their goals increased. There was less likelyhood of failure at the 35,000 - 39,999 and 40,000 - 44,999 goal ranges with a drastic increase in failure percentage from 45,000 and greater. The reason for less failures (a deviation from the trend) in the 35,000 to 44,999 range cannot be drawn from this data. For Louise, we conclude that it would be in her best interest to keep her campaign goal below 4,999, though there is success rates in the 35,000 - 44,999 goal ranges, those goals are far higher than her budget. The Outcomes Based on Goals chart truly shows the inverse relationship between successful and failed campaigns. We also let Louise know to not let any of her friends try to start a play campaign with goal ranges greater than or equal to 45,000 as they'll have a success rate less than or equal to 13%.

### - What are some limitations of this dataset?

#### The first thing I noticed about the dataset that was peculiar was that there was a currency column. The goal and pledge columns did not have any currency conversions. Kickstarter launched in 2009, the dataset contains campaigns from 2009 but the last campaign creation date has the year 2017. Louise needs campaign data up to today's date!

### - What are some other possible tables and/or graphs that we could create?

#### A graph that included percentage outcomes based on columns we did not use such as staff_pick and spotlight. We could see if length of campaign had an impact on campaigns, for example, campaigns that came very close to 100% funded but did not by the campaign end date.
