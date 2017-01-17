# API Design

What sort of data is useful for anyalizing a git project?

### Growth

Tracking the growth of a project, being able to accurately model growth and determine how fast/slow the project is expanding. 

_Commits_

* Breakdown commits by time span. User can determine what specific time span they want by selecting from and to date. Sample time spans would be month, week, day, and custom. Number of commits / time span = __Ac__ (average commits per time). This can be thought of as the 'speed' of growth. 
* The __Ac__ can be compared with other __Ac__ values to get a reading of how much faster or slower the growth of the project is occurring. This can be thought of as the acceleration of the projects growth. For example, week 1 has __Ac__ of 4, week 2 has __Ac__ of 7. The project is accelerating at 7-4/1 = 3 — each new week is producing 3 more commits than the last.  __Ac2__ - __Ac1__ / time span = __Ic__ (average increase of commits per time). User can determine what specific time spans for this formula as well. Can use percentage of increase instead, __Ac2__ - __Ac1__ / __Ac1__ = 3/4 = 0.75 = 75% more commits in week 2. 
* The __Ac__ and __Ic__ can be applied to the project, as well as individual users.

_Lines of code_

* __Al__ = number of new lines / number of commits (average lines of code per commit). User can specify the time span to determine the number of new lines that have been added during that time, and the number of commits that have been committed during that time. 
* The __Al__ can be applied to the project, as well as individual users.

### Time

Tracking how long certain processes in the project take. 

_Commits_

* Determine the average time between commits. First determine the time between each consecutive commits and sum them. Time between commits / number of commits - 1 = __Tc__ (average time between commits). User can specify the time span to determine the number of commits that have been committed during that time.
* The __Tc__ can be applied to the project, as well as individual users. 
* Determine how long it takes for # of lines to reach a particular limit. User can specify how many lines to reach. Example, it took 4 days to reach 100 lines, then 2 days, then 5. The average number of days to reach 100 would be: 11/3 = 3.67 days. 
* Can use percentage to express the increase/decrease in time per 100 lines. If it took 4 days to reach 100 lines, then 3, that would be 3-4/4 = -1/4 = -25%, which means it took 25% less time to reach 100 lines. 

### General Stats

General stats are just general metrics for the entire project/user. They don't track growth or time, but just indicate overall status. 

* Total commits = __C__
* Total number of lines = __L__
* Total number of days = __D__
* Graph of current git tree

### Leaderboard

Leaderboard sorts individual users based on all metrics (__Ac__, __Ic__, and __Tc__). Can also sort by total commits made, and total # of lines. 