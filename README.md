# Kickstarting with Excel

## Overview of Project

### Purpose

Louise wants to start a Kickstarter campaign to fund her play, Fever. Louise is estimating a budget of $10,000-$12,000. Performing analysis on Kickstarter data will help uncover trends for plays in the US in order to help Louise understand what sets successful plays apart and what the best course of action is to replicate those successes.

## Analysis and Challenges

One of the initial ways that the analysis was conducted was through comparing the number of successful, failed, and cancelled theatre kickstarters to their corresponding launch date. This was done by creating a pivot table with filters, such as the parent category and year, and compared the month of the year to the count of theatre kickstarters. We are not concerned with which year was the best for successful theatre kickstarters, but rather what month/time of the year is the best time to initiate the campaign.

![Outcomes Based on Launch Date-Table](https://user-images.githubusercontent.com/111096246/187094409-51db5d65-857b-4ab1-821a-8f2e61cef7c4.PNG)

The graph and table above serve as an example for the type of tables and charts used that aid in visualizing a trend that could benefit the decision-making process. The table on the left is known as a pivot table, a helpful tool that assists in calculating, summarizing, and analysing data that allows for data comparison, and pattern and trend recognition. Given that we are attempting to identify what the patterns/trends are for successful theatre play fundraisers, this tool is extremely important and beneficial. The graph to the right helps visualize the block of numbers in the table and allows for the numbers to make more sense to whoever is attempting to extract a conclusion from the data. The pivot chart, essentially, is the illustrated version of the pivot table.

![Parent Category Outcomes-Table](https://user-images.githubusercontent.com/111096246/187531614-f7795ba6-8494-4342-a4e6-7ba0d3a1cb72.PNG)

When compared to other categories of fundraisers, the number of successful theatre fundraisers are higher than any other category. With a total of 912 theatre fundraisers, 525 were successful, 349 were cancelled, 26 failed, and 12 were live at the time data was gathered and analysed. With these numbers in mind, the success rate of a theatre fundraiser would be 58%. This number may be a bit discouraging, as it lands close to a 50/50 success or fail. However, other fundraisers did not rely on in-depth analysis to start off.

![Descriptive Statistics](https://user-images.githubusercontent.com/111096246/187531772-2f285d50-1238-4721-bd62-a69da7df1c61.PNG)

When attempting to figure out what sets successful fundraisers from failed ones, it is important to also recognize whether the fundraiser goal itself was what could have caused the project to succeed or fail. In this case, we can see that the average goal for a fundraiser was approximately $5,000 and $10,500 for failed fundraisers. This proves to be problematic for Louise, as the proposed goal for the production, Fever, is like past failures. Furthermore, the average amount of money received/pledged is about a tenth of what a successful fundraiser brings in.

![GB-Musicals Box-Plot](https://user-images.githubusercontent.com/111096246/187532681-bf2746f3-84b1-4abb-a663-c814b78e0560.PNG)

Louise has also expressed interest in the theatre market in Great Britain, especially musicals. Louise's proposed budget for her future project is around £4,000. Thankfully, there are British musicals ready for analysis that could help paint a picture for what to expect in Great Britain. With the box and whisker plot above, one can notice several things. The mean campaign goal is around £4,000, which is beyond the range of outliers for the amount pledged, so it would be recommended that the musical be produced for less than proposed. Moreover, half of the musicals had a goal of £2,000 or less, which just lies over the 3rd quartile for amounts pledged.

### Analysis of Outcomes Based on Launch Date

What is the best time of the year 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/111096246/187095012-6d7f7fa4-5cce-4ffa-b36c-6ec2b2a235cd.png)

There was a grand total of 900 theatre fundraisers from 2009 to 2017. Throughout the months of the calendar year there was one month which showed a larger number of theatre fundraisers becoming successful. This month is May, with 65 fundraisers becoming successful of a total of 96 proposed fundraisers (68% success rate). It is therefore recommended that the fundraising start in May. The fundraiser could allow for unexpected delays and start in June, as it is the month with the second most number of theatre fundraisers in the US.

### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/111096246/187532789-63ec50ee-9d54-4c57-93a7-a35f50b1ce26.png)



### Challenges and Difficulties Encountered

A challenge that was encountered was when the use of the COUNTIFS function came into play. The objective was the count how many successful, failed, or cancelled plays lied within a certain range for their proposed fundraiser goal. Initially, adding the second half of the range was difficult to implement, however through some research this was quickly resolved. The main problem arose when the count of plays was not matching the expected outcome. The incorrect code, for example, was asking for values greater than $25,000 and less than $29,999, as seen below:

```
COUNTIFS(Kickstarter!D:D,">25000",Kickstarter!D:D,"<29999",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays")
```

The issue was that the values should be including the goal ranges, not excluding them. Therefore, by adding two “=” signs in their respective places the code now looks like this:

```
=COUNTIFS(Kickstarter!D:D,">=25000",Kickstarter!D:D,"<=29999",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays")
```

Other than the problems mentioned previously, there were thankfully no major problems with the data analysis in general, and everything went accordingly well. Through comparing the obtained and expected outcomes, potential problems were suspected, analysed, clarified, and resolved. All that is left to do is to interpret the data, graphs and tables in order to present an in-depth conclusion that will answer questions for the client, Louise.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
