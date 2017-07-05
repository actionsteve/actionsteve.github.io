---
layout: post
title: Project Benson
---

Learning data science at Metis is a project-driven experience. Over the twelve week program, we'll tackle five real world projects that build upon our experiences in the classroom. Follow along here, as a blog about this journey.

## What is the challenge?

True to "boot-camp" form, we hit the ground running in Week One with Project Benson. Our fictional client, WomenTechWomenYes (WTWY) needs help driving attendance at their annual gala. They plan on strategically deploying a street team of canvassers around New York City subway stations to collect email addresses from interested straphangers, offering free gala tickets while simultaneously spreading the organization's message. They've charged us with optimizing the placement of their team.

## What do we know? What do we assume?

The gala occurs at the beginning of Summer. For an early June event, we used MTA traffic from the preceeding Spring (February through April). This gives us the most recent ridership, while allowing sufficient time to deploy the streat team before the gala.

It is useful to revise our problem space, shifting our search from "greatest traffic volume" to "sufficent, yet *highly relevant* traffic volume." Relevance, here, refers to stations where our target audiences ride. WTWY focuses on reaching individuals passionate about increasing the participation of women in technology. Absent actual marketing research, "women" seem like an obvious first choice target demographic. "Tech company employees" seem like another.

We assume we have a modestly sized street team, divisible into three different groups that can simultaneously canvass distinct stations across the city.

## What was our approach?
Based on independent research data, we identified zip codes densely populated with our target demographics, and we strategized times of day to reach them.

1) **Women** - Census data provides gender percentage reports by zip code. Assuming men and women are equally likely to ride the subway, we blended these results with MTA entrance data to find the top stations where women start their daily commute. We used similar methods for women returning home after work.

2) **Tech Professionals** - We collected the addresses of technology companies in New York, from search engine giants to hustling startups. We also found addresses of top universities and research centers. We reason that riders who used associated stations during the work day are more likely to be tech professionals.

We (literally) mapped the top zip codes for each category to the stations present, focusing our analysis to the most relevant traffic.

## What did we find?

For the relevant zip codes associated with each target category, we ranked entrance traffic for our time period of interest. The top three ranked stations form the basis of our recommendations. (Note: Monday's top station might be different from Tuesday's. Whichever ranked highest was that day's recommendation.)

We reported the potential reach of the street teams among relevant populations as follows:

**Women on their way to work.**

![alt text][https://github.com/actionsteve/actionsteve.github.io/blob/master/images/time1_graph.png]
![alt text][time1_map.png]

From our subset of zip codes with highest female ridership, we identified the York St [F line], 125th St [2,3 line], and 125th St [1 line] as top three stations thirteen out of fifteen (three ranks a day, five weekdays a week). For a given day's top rankings, we would divide the team to those three stations in the morning, hopefully reaching more women on their way to work.

**Tech employees during work hours.**

![alt text][https://github.com/actionsteve/actionsteve.github.io/blob/master/images/time2_graph.png]
![alt text][https://github.com/actionsteve/actionsteve.github.io/blob/master/images/time2_map.png]

After the morning commute, throughout lunchtime, and just before the workday is finished, the street teams would move to the top locations to reach tech employees and academics. Fortunately, our data reveal some overlap with the morning posts. The top three stations are consistantly York St [F], 125th St [2,3], and Hoyt-Schermerhorn [A,C,G]. We would shift our teams to these locations as necessary.

**Women on their way home.**

![alt text][https://github.com/actionsteve/actionsteve.github.io/blob/master/images/time3_graph.png]
![alt text][https://github.com/actionsteve/actionsteve.github.io/blob/master/images/time3_map.png]

Finally, we identified top locations where women get on the train to head home from work. There was more distribution of top stations for this category. Canal St [J,N,Q,R,W,Z,6] rose to the top, with York St [F] and 125th St [2,3] remaining prevelant. Prince St [N,R,W], Jay St [A,C,F], High St [A,C], and Hoyt-Schermerhorn [A,C,G] also made the list.

## Final Report?
Taken together, we are able to create a final report, recommending when and where the teams should be distributed. Take Monday's report, for example:

![alt text][https://github.com/actionsteve/actionsteve.github.io/blob/master/images/monday_schedule.png]

On Monday morning, we would deploy Street Team 1 to York St [F], Street Team 2 to 125th St [2,3], and Street Team 3 to 125th St [1] in the morning, hoping to catch women on their way to work.

Around lunchtime, Street Team 1 would remain at York St [F], and Street Team 2 would stick to 125th St [2,3]. Street Team 3 would move to Hoyt-Schermerhorn [A,C,G] to a new, popular station relevant to the tech employee and student audience.

Finally, Street Teams 1 and 2 would move to Prince St [N,R,W] and Canal St [J,N,Q,R,W,Z,6], while Team 3 would remain at Hoyt-Schermerhorn [A,C,G]. Here, the teams would catch women on their way home from work.



#What are our next steps and future considerations?

* **Did we limit our scope too narrowly?**
We made limiting assumptions based on census data and tech/university addresses. Perhaps we are unwittingly ignoring key locations of interest. We should compare our results to those made using alternative strategies.

* **The right demographics?**
We used broad demographics to determine relevant targets. Owned research data might suggest more specific alternatives.

* **Women on their way home?**
Using census data of where women live to focus our search, our restricted scope does not tell us where women are getting on the train to go home. Our data don't tell us where women work. Using exit data would have been more appropriate for this last leg.

* **Do people want to be reached on their way to work? At lunch? On their way home?**
Reasonable arguements can be made as to why certain times of day are more effective times to canvass. Maybe people are in a rush to get to work (or home!). People may love talking to strangers on their lunch breaks. Station controlled sign-up counts could inform the value of canvassing throughout the day.

* **How to distribute the team?**
We broadly recommend dividing the team into three groups to work at the top stations at a given time. Depending on relative traffic of these stations, the teams could be distributed proportionately to expected traffic. Similarly, we should optimize time spent working by minimizing distance between a worker's shifts.


[time1_graph]: /time1_graph
[time1_map]: /time1_map
[time2_graph]: /time2_graph
[time2_map]: /time2_map
[time3_graph]: /time3_graph
[time3_map]: /time3_map
[monday_schedule]: /monday_schedule
