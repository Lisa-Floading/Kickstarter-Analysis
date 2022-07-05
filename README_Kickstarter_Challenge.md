# Kickstarting with Excel

## Overview of Project


### Purpose
The purpose of this analysis is to consider how crowdfunding data can be used to understand what makes a successful campaign. The client is Louise, a playwright who was able to come close to her fundraising goal for her play, Fever, in a relatively short time. She estimated a budget of over $10,000 for the project. Now that her Kickstarter campaign has ended, she wants to know how different crowdfunding campaigns did in relation to their launch dates and fundraising goals. For this analysis, campaign outcomes based on launch dates and funding goals were visualized.  

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

In order to visualize campaign outcomes based on their launch date for this section, I created a pivot table (Insert->PivotTable) from the original Kickstarter data in a new worksheet with the following parameters.
![](PivotTable_Fields_Launch_Date.png)
Next, the "Parent Category" on the table was filtered on "theater" and the row labels were grouped to display the months of the year. To do this, I right-clicked on the row labels (which were the date created) and selected "Group" and then changed the labels to be only months. Next, the campaign outcomes were sorted by month, starting with January. Finally, I clicked on "Recommended Charts" and selected Line to insert the chart. 


### Analysis of Outcomes Based on Goals

For this deliverable, I created a new sheet in the original Kickstarter workbook that would show goals and the number of successful, failed and canceled projects as well as the total for each category and the percentage of successful, failed and canceled projects. Based on the given dollar amount ranges in the module, the first column was created to look like this: 
[![](https://courses.bootcampspot.com/courses/1601/files/1856825/preview)](https://courses.bootcampspot.com/courses/1601/files/1856825/preview)

Next,the COUNTIFS() function was used to create a formula to place the number of each type of projects in the appropriate category. The formula below shows that I am using the goal column (D) and only those campaigns that were successful for plays seeking under $1,000. 
=COUNTIFS(' Kickstarter Challenge'!$D:$D,"<1000",' Kickstarter Challenge'!$F:$F,"Successful",' Kickstarter Challenge'!$R:$R,"plays")

### Challenges and Difficulties Encountered

When I was creating the Analysis of Outcomes Based on Goals line chart, at first it did not look like the finished product on the module. I realized that I was using the wrong column in the formula. Instead of using the goal column (D) I was using the pledged column (E). I carefully read over the instructions and realized my mistake. Correcting the formula resulted in a chart that matched the one shown in the Challenge.  

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

Two conclusions I can draw from the Outcomes Based on Launch Date information are based on when donors might be willing to support a theater project. The most successful campaigns launch in early summer (May and June) and the least successful campaigns are in December. Perhaps seeking donations around the end the of year is a challenge because of the various holidays. 

- What can you conclude about the Outcomes based on Goals?

From the Outcomes based on Goals I can conclude that some of the most successful campaigns seek between $1,000 and $5,000. 

- What are some limitations of this dataset?
 
One limitation of this dataset is that it only looks at Kickstarter campaigns. Might there be other ways to raise money for this project? Another limitation of this data is that it does not take into account the audience for each play's campaign. Perhaps some types of stories are a better investment for donors. 

- What are some other possible tables and/or graphs that we could create?

We could consider theater in the US as compared to other countries. We could also consider which goals tend to have the most backers for plays and what the average donation tends to be. This would be helpful in requesting donation amounts. We could also look at the average length of time for a Kickstarter campaign for similar projects to determine the optimal length of time for the campaign. 
<!--more-->

<!--more-->

