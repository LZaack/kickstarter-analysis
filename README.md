# Kickstarting with Excel

## Overview of Project

We worked with the data of 1,393 theater projects including musicals and plays, around 19 countries, but principally in the United States and Great Britain. We analyzed certain characteristics of the successful, failed, and canceled projects, like the goal, pledged, date of launch, and year.

The outcomes are described in a visual presentation in order Louise could check them at a glance. With this information, we anticipate she would be able to take accurate finance and date decisions to launch her project.

### Purpose

`The purpose of this analysis` is to generate insights that will help Louise to make decisions about her theater project. We get a database named Kickstarter Sheet (“***KS***”) that contains the information of many projects around the world like film & video, technology, food, publishing, music, and certainly theater.

## Analysis and Challenges

The first step was to identify how the information was classified in the KS and after that, based on the information already given we create new categories, for example, we separate the data in the column named “Category and Subcategory” and create the columns “Parent Category” and “Subcategory”. As a result of this, was easy to identify and measure the musicals and plays.

![Parent Category_Result](https://user-images.githubusercontent.com/95454286/147423184-c497a232-cb72-459c-86ce-e5240c9412e2.png)

To get the finding outcomes, we changed the format of the information in the column named “launched_at” that contain timestamps, which measure time as the number of seconds since midnight of January 1, 1970, to a specific date, so we apply a formula to figure out how many days, minutes and seconds the timestamp translates to.

![Timestamps_Formula](https://user-images.githubusercontent.com/95454286/147423200-89ecb74a-941a-42e6-81b7-eb99a0e0fac3.png)

Then, from the new column named “Date Created Conversion” we extract just the year to filter the success of the plays, by using the excel formula ![Year_Formula](https://user-images.githubusercontent.com/95454286/147423269-9aa7965f-671f-4338-8711-5d07772b39b1.png) to finally get it as it looks in the next image:

![Year_Formula_Result](https://user-images.githubusercontent.com/95454286/147423210-7c5991c0-db89-4dd2-90cd-b8f60716b407.png)

### Analysis of Outcomes Based on Launch Date

After that, we created a pivot chart from the KS, labeled “Theater Outcomes by Launch Date”, filtered based on the Parent Category and Years and we filtered the columns labels to show only successful, failed, and canceled projects.

Then we sorted the Parent Category to show only the data for Theater, to get the following result:

![Pivot Table_Parent Category_Results](https://user-images.githubusercontent.com/95454286/147423223-983546e8-72b0-49dc-afff-0ef8288bcf10.png)

From this pivot table, we get the next line chart to visualize the relationship between outcomes and launch month:

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/95454286/147423233-6b491892-7b02-4732-8ef1-79ae9c964c99.png)

From a glance at the chart, Louise can observe that May is the month where most of the successful theater projects start, followed by June, and July. February, April, and August are slightly closed. January, March, September, and November are related in number with a decrease in comparison with the previous group, and December is the worst month to start a Theater Project.

#### First Recommendation

Based on this information, we recommend Louise start her project in May, which means starting pre-production earlier, but if she decides to start after May, she can do it in June and July with great certainty of success.

### Analysis of Outcomes Based on Goals

We understand that Louise was more interested in plays than in musicals, so to reach precise data about it, we also made a graph to understand the number of successful, failed, and canceled plays based on the goal.

It is convenient to precise that the population analyzed here was just the plays, without the musicals, reason why the number of the total is slightly lesser. 

![Outcomes_Based_on_Goals](https://user-images.githubusercontent.com/95454286/147423253-cf0e8f05-94c5-49be-8353-f2a4e4793cd4.png)

From the table below 388 successful plays have a goal from $1,000 to $4,999 followed by those with a goal of 41,000 or less. It is important to realize that from the 534 plays in this range, just 72.66% were successful and the other 27.34% were failed.

The second place was for the plays with a goal of $1,000 or less. In addition, the percentage of success was slightly higher than those in the range of $1,000 to $4,999, which reduces the possibility of failure.

In third place were the plays in the range of $5,000 to $9,999, with a close difference between the successful and the failed plays, 55.03%, and 44.97% respectively.

In the following table, appears the behavior of the success and canceled plays about the range of goal, analyzed herein before.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/95454286/147423387-f55347bf-8448-4992-98a1-98f6a092faf7.png)

#### Second Recommendation

Our second recommendation to Louise is, according to the data, the plays with more success are those in the range of $1,000 to $4,999, so try to find a play whose budget could be fittable into the range to increase the percentage of success. 

### Challenges and Difficulties Encountered

The biggest challenge was to interpret the data without knowing its source. After many days of working with the data, I understood that most of it is about crowdfunding, not about the projects per se.
Additionally, I found some difficulties like comparing different units, for example, goals currency and pledged currency, without a clear date and exchange rate.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. The Theatre projects launched in May, Jun, and July are more successful than those launched in other months.
2. It is not recommendable to launch a project of this nature in December, the numbers reflect the low success in that month.

- What can you conclude about the Outcomes based on Goals?

Most of the successful plays are in the goal range of $1,000 to $4,999, but the fewer plays that failed are those in the range of $1,000 or less. So, it is important to fit the budget´s play closely to de number of $1,000.

- What are some limitations of this dataset?

The goals given in the KS are skewed because the goals compared are in a different currency, which means that the ranges calculated in the table “Outcomes Based on Goals” are a parameter, but it is not reliable. To give Louise accurate information, I probably would compare the data from the same country.

- What are some other possible tables and/or graphs that we could create?

A bar table probably shows in detail, in the case of “Theater Outcomes by Launch Date” the exact percentage of the outcomes filtered by month, and in the case of the “Outcomes Based on Goal”, the difference between the percentages of success and failed plays.
