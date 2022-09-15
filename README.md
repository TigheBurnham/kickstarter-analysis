# Kick Starting with Excel

## Overview of Project
Kickstarter is like other crowdfunding platforms allowing pledges to have specified incentives depending on the funding amount. This excel file is a technical analysis of various Kickstarter campaigns throughout multiple countries and their different funding goals.

## Purpose of Analysis
The goal of this project is to shed light and delve into the financial effectiveness of how different campaigns did in relation to their launch dates and fundraising goals.

## Analysis and Challenges
This analysis was primarily conducted through utilizing Pivot Tables to sort data, and then implementing Pivot Charts to visualize and explain the findings. 

### Analysis & Results of Outcomes Based on Launch Date
Crowdfunding launch dates that occurred in early summer months like May and June had the highest number of successful campaigns. September also appeared to be the hardest time of the year to kickstart a new project. This is seen in the graph below.

![Launch Date Outcomes](https://user-images.githubusercontent.com/112028534/189252264-532f4d64-98bc-4d89-b798-4f516cf1e925.png)

#### Analysis of Theater Outcomes Based on Launch Date
There were 166 total theater campaigns launched in May which made May the time of the year with the most theater campaigns started. This is also the time of the year when there was the most amount of successful campaigns. In addition, May was also the month with the highest success rate at 67%. December had the fewest number of new theater campaigns, and also had the lowest success rate at 49%. It appears the best time to start a new Theater campaign should be launched in the early summer months, and starting a campaign after June or around December should be avoided. 

![Theater_Outcomes_vs_ Luanch](https://user-images.githubusercontent.com/112028534/190502019-a6e7d436-134b-4d1c-97ce-8067cc75eb3f.png)

### Analysis & Results of Outcomes Based on Goals
In general, campaigns that had a pledge goal of around $5,000.00 had the highest success rate. The campaigns with the most successes were Theater with 839 completed projects, and the next most successful amount of projects was Music with 540. Music appears to be the easiest project to meet its funding goal with a 77% success rate.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/112028534/190503705-50792680-8133-4e28-92de-476268b892fc.PNG)

![Parent Outcomes](https://user-images.githubusercontent.com/112028534/189252278-f6de3c04-8ebf-4888-ad45-f7823dbedcb6.PNG)

Campaigns that targeted a pledge of $10,000.00 had the highest rate of failure. Journalism had the fewest number of Kickstarter campaigns. There were 200 food campaigns: 140 of them failed and only 30 were successful. Food projects appear to be the hardest category to kickstart and get off the ground as they had the highest rate of failure.

#### Analysis of Plays Outcomes Based on Goals
Play campaigns with a goal of $5,000 or less had a success rate of over 70%. As play campaign goals increased in value the success rate decreased until the campaign funding goal was between $35,000 to $45,000 where the success rate was over 60%. A limitation during this time is that there were few play campaigns started at this goal, so more data may be needed to normalize this rate. Nevertheless, there were over 700 play campaigns started with less than $5,000.00, and it appears that goal has the highest rate to be successful.   

![Subcategory Outcomes](https://user-images.githubusercontent.com/112028534/189252282-f61f0728-f8c8-432e-b3f3-f0d5a5717708.png)

### Challenges
The main challenge that was encountered in this project was properly referencing and absoluting  the correct columns when using the COUNTIFS() function. Referencing data between different worksheets without properly absoluting cells led to errors and miss-calculations that had to be debugged.  

For example: 

=COUNTIFS(Kickstarter!D:D,"<"&Goal!$C$2,Kickstarter!$F:$F,"Successful",Kickstarter!$R:$R,"plays")

The above formula was originally used to calculate the number of “Successful” campaigns depending on the funding goal. Notice the “Ds” in bold which is the first criteria that references the Goal column. When writing this formula I forgot to absolute this range therefore when I calculated the “Failed” campaigns my formula looked liked the one below:

=COUNTIFS(Kickstarter!E:E,"<"&Goal!$C$2,Kickstarter!$F:$F,"Successful",Kickstarter!$R:$R,"plays")

Without dollarazing the goal criteria my “failed” campaigns were counting the “pledge” data. This produced the following graph that was misleading.

![Misleading Graph of Goal Outcomes](https://user-images.githubusercontent.com/112028534/190503592-c746753f-16f3-49d8-a250-1192629fd2f2.png)

It’s clear that one error can have a cascading effect on other parts of the analysis.

## Conclusion and Final Comments
Based on the data it appears there is a correlation between the type of campaign, the time of month a campaign is started, and the level of its funding goal with regards to its success rate. Campaigns like Music and Theater that are launched in May or June with a funding goal of $5,000 or less will have the highest chances of success. Therefore, another graph and table that would be interesting to create would be the amount of “successful” and “failed”  campaigns that had a goal of less than $5,000.00 throughout the year. Again my hypothesis would be those campaigns launched in the early summer months with less than $5,000 as a funding goal would have the highest rates of success. Nevertheless, more research may be needed on why other campaigns launched during the early summer months with those times with smaller funding goals are less successful. For example, more campaign  data may be neeeded to be collected to increase the strength and results for kickstarters like journalism to shed light on why they underperformed. In addition, this analysis does not capture information regarding to the marketing or finance strategies used to kickstart these campaigns, which may also be crucial variables in each campaign's success. 


