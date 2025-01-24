# June 2024 Citi Bike Analysis

## Overview
This Tableau Story presents a set of visualizations based on data provided by the Citi Bike program. The analysis aims to uncover phenomena in bike usage patterns, customer behavior, and station performance throughout June 2024. Each phenomenon is explored through a series of data visualizations that highlight key trends, with the goal of providing actionable insights to city officials and stakeholders.
View the Tableau Story at: [https://public.tableau.com/app/profile/jean.ryan.lozon/viz/CitiBikeAnalysis-June2024/June2024CitiBikeAnalysis] (https://public.tableau.com/app/profile/jean.ryan.lozon/viz/CitiBikeAnalysis-June2024/June2024CitiBikeAnalysis)

## Data Source
**CitiBike Data:** https://s3.amazonaws.com/tripdata/index.html
202406-citibike-tripdata.csv.zip

CitiBike Data was downloaded as 5 csv files and then combined into a single dataframe in the Jupyter Notebook "CitiBike_Data_Cleaning.ipynb". This was done using guidance from the class TA, Mo Abouelkhier.

## How to Navigate the Story
Findings are structured as a Tableau Story to guide the user through each phenomenon step-by-step. It includes:

 - Interactive visualizations that allow you to explore the data in depth.
 - Maps showing station usage over time, with dynamic filters to track trends.
 - Dashboards that combine multiple visualizations to provide comprehensive insights into each phenomenon.
 - Each section is accompanied by a written analysis that explains the findings and provides context for the observed trends.

## Key Findings
The written analysis of each section of the Tableau Story is included below for easy reference.

### Station Popularity
Ridership in the month of June was concentrated in the Manhattan area. By isolating the "Top Ten Ending Stations, we can see that 150,619 rides ended at these stations in June. 

The graph "Top Ten Ending Stations (Colored by Starting Station)" demonstrates how bike traffic from all over NYC fed into these ten stations. Each color represents a different starting station. The sheer number of different starting stations whose riders came to these ending stations results in the gradient effect on the graph. Hover over individual colors to how many rides each starting station contributed to the corresponding ending station.

Manhattan isn't only the most popular destination, but also the most popular origin. The graph "Top Ten Starting Stations (Colored by Top Ten Ending Stations)" shows which stations were the most popular starting spots in June. In this graph stations are colored with only the top ten ending stations. This illuminates how these high traffic areas interacted with one another. Central Park S and 6 Ave is a particularly interesting case: over 2,000 rides that started at Central Park S and 6 Ave also ended there! This might be due to riders using Citibikes for leisure rides in Central Park or more tourists using the bikes to explore before returning to a meetup spot.

### Membership Insights
Seeing that ridership was concentrated in Manhattan might make it tempting to conlcude that most riders are tourists or non-locals. However, membership data shows otherwise.

The breakdowns of Member and Non-Member rides seen here shows that Members consistently ride more frequently and make up the majority of riders, regardless of the day. "Member and Bike Type Categorized by Weekday" shows that the day with the most rides is Saturday, and Members are taking the majority of rides. Predictably, Members are also making up the majority of rides during the week. Interestingly, the preference for Electric Bikes over Classic (non-electric) Bikes is consistent across both Members and Non-Members. But Member rides outnumber Non-Member rides so significantly that Member usage of the less popular Classic Bikes still outpaces the number of Non-Member rides on the more popular Electric Bikes.

For a more detailed look at how rides were distributed between Members and Non-Members in June, scroll through "Member Type by Date" to compare ridership day-by-day.

One factor that could contribute to Member rides being such a consistent majority is commuters using citibikes consistently to get to work. Additionally, the pricing of memberships is most likely a major factor in the popularity of Membership rides. See the Citi Bike webpage for a breakdown of current pricing. With reduced rate Electric Bike rides and unlimited 45-minute Classic bike rides for under $20/month, most riders looking to use a Citi Bike would benefit from choosing a membership over a Non-Member ride.

### Time Data by Ride Type
The Analysis of popular ride times is consistent with out previous conclusions. Ridership is highest during the post-work rush hour, from 5-6pm, and there are consistent ride numbers across the work week, although Saturday remains the most popular dy to ride. 

In the Breakdown of rides day-by-day, "Rides per Day by Bike Type" there are consistent spikes in ridership each Saturday, although the most rides occurred on Friday June 28th.

As was noted in the Membership analysis, Electronic Bikes are consistently more popular than Classical Bikes, regardless of the time, weekday, or date. The popularity of Electronic Bikes is most likely a reflection of convenience, as Citi Bike's marketing notes, these bikes "give you the power to go farther and faster - without breaking a sweat".

### Map of All Starting Stations
The "Map of All Starting Stations in June 2024" provides a static map that plots all bike stations. Stations are represented by a circle, which is sizesd and colored to indicate which locations are more popular. The more frequently a starting station was used, the larger its circle will be. The least-used stations are green, whereas those in the mid-range of use become yellow or orange, and the most-used stations are red.

The number of rides that occurred in June is massive. While mapping this data can help visualize where all of the CitiBike stations are and get an idea of popularity, the sheer volume of data can be cumbersome. See the next Dashboard for a more useful map of CitiBike usage in June.

### Map of Starting Stations with Over 2500 Rides
The "Map of Starting Stations with Over 2500 Rides in June 2024" provides a static map that plots the most popular bike stations (those that saw over 2500 rides in June). Stations are represented by a circle, which is sizesd and colored to indicate which locations are more popular. The more frequently a starting station was used, the larger its circle will be. The least-used stations are green, whereas those in the mid-range of use become yellow or orange, and the most-used stations are red.

The conclusions we can draw from this mapping are once again consistent with the rest of this analysis. Manhattan shows a concentration of popular stations. Hovering over the stations provides a detail tag of each station location and name, as well as the number of rides that started there in June.

## Conclusion
This analysis of Citi Bike data for June 2024 provides valuable insights into bike usage patterns, membership behavior, and station performance throughout New York City. Key findings reveal that Manhattan remains the dominant area for both bike trips and station usage, while membership-based riders consistently account for the majority of trips. Additionally, electric bikes continue to outpace classic bikes in popularity, likely driven by their convenience. The visualizations presented in this story offer a comprehensive view of Citi Bike’s operations, which can help city officials make data-driven decisions to optimize station locations, bike availability, and overall program growth moving forward.
