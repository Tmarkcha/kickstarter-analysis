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

There are many questions that need answering when planning a significant fundraiser such as this one. First one that comes to mind is: Does the time of year when the fundraising start affect the potential success? Please refer to the visual aid below to find out.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/111096246/187095012-6d7f7fa4-5cce-4ffa-b36c-6ec2b2a235cd.png)

There was a grand total of 900 theatre fundraisers from 2009 to 2017. Throughout the months of the calendar year there was one month which showed a larger number of theatre fundraisers becoming successful. This month is May, with 65 fundraisers becoming successful of a total of 96 proposed fundraisers (68% success rate). It is therefore recommended that the fundraising start in May. The fundraiser could allow for unexpected delays and start in June, as it is the month with the second most number of theatre fundraisers in the US.

![Theatre Outcomes Vs Launch Date Table](https://user-images.githubusercontent.com/111096246/187534215-3e72aa41-a0af-4e4f-9e7b-5026fb191766.PNG)

In conclusion, the month of May, as stated previously, is the optimal month to begin the fundraiser campaign, but that's not to say it is the only month wher Louise can look to start her campaign. The months of June and July also offer a glimmer of opportunity for further campaigning, but it must be noted that the odds of a successful campaign dwindle as time passes on. Anytime before May is out of the question, and anytime after July should also be ruled out.

### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/111096246/187532789-63ec50ee-9d54-4c57-93a7-a35f50b1ce26.png)

As observed in the graph above visualizing the relationship of the percentage of a fundraiser’s success, failure, or cancellation to the dollar amount of the fundraiser’s goal, the less the fundraiser requested in terms of its goal, the better the odds of obtaining a successful status. At a goal of less than $1,000 the percentage of successful campaigns is at its highest at 76%, and the percentage of failed campaigns is aits lowest at 24%. This percentage dips a little to 73% with a goal from $1,000 to $4,999. The only other “acceptable” goal range would be from $35,000 to $39,999 and $40,000 to $44,999 where the percentage of success is 67% for both ranges. This is not ideal, as the odds of having a failed campaign are higher than before at 33%.

![Outcomes Based on Goal Table](https://user-images.githubusercontent.com/111096246/187541364-9d370c99-065b-400f-86b5-8f688a29dc4e.PNG)

Louise’s proposed goal of $10,000-$12,000 puts her percentage of a successful campaign at 54%, and that is eerily close to failing her fundraiser with the percentage of failed campaigns being calculated at 45% - Almost double than the ideal goal of less than $1,000. It would be up to Louise’s discretion if by asking for ten times the recommended amount, she would be comfortable with doubling her potential odds of failing.


### Challenges and Difficulties Encountered

A challenge that was encountered was when the use of the COUNTIFS function came into play. The objective was the count how many successful, failed, or cancelled plays lied within a certain range for their proposed fundraiser goal. Initially, adding the second half of the range was difficult to implement, however through some research this was quickly resolved. The main problem arose when the count of plays was not matching the expected outcome. The incorrect code, for example, was asking for values greater than $25,000 and less than $29,999, as seen below:

```
=COUNTIFS(Kickstarter!D:D,">25000",Kickstarter!D:D,"<29999",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays")
```

The issue was that the values should be including the goal ranges, not excluding them. Therefore, by adding two “=” signs in their respective places the code now looks like this:

```
=COUNTIFS(Kickstarter!D:D,">=25000",Kickstarter!D:D,"<=29999",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays")
```

Another problem that was resolved was the fact that the dates in which the fundraisers were created and ended were provided as Unix timestamps. Unfortunately, these numbers do not provide a clear date, and thus require further calculations to translate from Unix to a recognizable date format. First, what is a Unix timestamp? It is a way to track time in seconds from the start of the Unix epoch on the 1st of January 1970. In other words, a Unix timestamp is the number of seconds that have passed since a particular date and the Unix epoch. The following sample code is the function used to translate from Unix to a standard date format.
```
=(((J522/60)/60)/24)+DATE(1970,1,1)
```

Where the first division of 60 converts the seconds to minutes. The second division of 60 converts the minutes to hours. Additionally, the division of 24 converts the hours to days. Lastly, the addition of “DATE(1970,1,1)” refers to the Unix epoch mentioned previously. 

Other than the problems mentioned previously, there were thankfully no major problems with the data analysis in general, and everything went accordingly well. Through comparing the obtained and expected outcomes, potential problems were suspected, analysed, clarified, and resolved. All that is left to do is to interpret the data, graphs and tables in order to present an in-depth conclusion that will answer questions for the client, Louise.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The first conclusion, as mentioned previously, is that May is the optimal month for the fundraiser to begin. This is affirmed by the 65 successful campaigns out of a grand total of 96 campaigns initiated in the month of May. These numbers show that there is a 67.7% chance of a successful campaign, a 30.2% chance of failure, and a 2.1% chance of being cancelled.

One might wonder why May produces more successful campaigns and there can be a variety of reasons. One of those potential reasons is the fact that spring has just started, and with winter out of the way, people are looking to go out and enjoy themselves. Additionally, with the following months, namely June through to August, people start heading out on holidays and attending other summer events which might be higher on the list for potential patrons.

The second conclusion would be which month is the least favourable for a fundraiser to start. This month would be December, where the odds of generating a successful campaign is just as likely as the campaign failing. This can be noted by noting that there are just as many successful campaigns as there are failed, with there being 27 campaigns each.

This can be due to seasonal factors as well, with December being in winter, and people not wanting to go out and stay in the comfort of their home. In addition, December is a time for family and friends where people are getting presents, going on vacation, or supporting charitable organizations, and are not thinking of the theatre.  

- What can you conclude about the Outcomes based on Goals?

Based on previous fundraisers, their final status, and their financial goals, it is safe to say that the ideal fundraiser goal is less than $1,000, as this puts the success percentage to be 76%. With Louise’s proposed fundraiser goal of $10,000-$20,000 this would leave her fundraiser a 54% chance of succeeding, or a 46% chance of failing. These percentages are too close for comfort, and it would be advised that the proposed budget should be reduced to better the odds of succeeding.

- What are some limitations of this dataset?

The inclusion of outliers heavily hinders the ability to do further analysis, as any attempt to perform descriptive analysis is skewed and does not truly reflect the average, for example, goal or amount pledged.

Furthermore, it would be beneficial for the dataset to include in what way were the campaigns advertised. With this information, one could easily compare how different forms of media stack up to one another. Could newspaper ads be more successful than radio ads? Or how would different social medias stack up to one another?

With social media in mind, the dataset is limited by the lack of demographic information. Knowing which age groups pledge more money than others would allow for a more focused, and targeted campaign. There’s no point to advertise to teenagers if the average donor is in their 30s.

Another limitation would be the lack of a genre column. Having a genre dataset would allow for further, and more specified analysis. This could also pave the way to figuring out what people want to see in the theatre. Would the donors rather see a comedy, or a sci-fi rom com? Having that information could help answer that question.

Lastly, having zip/postal codes would allow one to geographically visualize how donations compare to distance away from the proposed venue. If we know that the average donation is approximately $100 within a 20Km radius of the venue, and with the average amount dwindling as the radius increases, then one can focus on prospective patrons within that 20Km radius.

To sum it all together, by knowing what platform is the most successful at receiving pledges, to also knowing what age group is more likely to donate, and what genre increases popularity one can engineer an incredibly specific ad campaign that checks all the boxes. 

- What are some other possible tables and/or graphs that we could create?
