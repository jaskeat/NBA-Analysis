# Does Defense Win Championships? An Analytical Exploration of NBA Success

This project aims to analyse NBA Team stats from 2010 onwards to see if the 'Defense wins championships' is really true or if offense prevails. We will be analysing the regular season and playoff success to test our hypothesis.

### Dataset

The data for this project was obtained from the [Official NBA website](https://www.nba.com/stats/teams/advanced). I combined the data from all the seasons. The dataset includes various metrics on the stats for each team in that season.

##### Dataset preview:

| Rank | Team                  | Win %    | Def Rtg | Off Rtg | Champion |
| ---- | --------------------- | -------- | ------- | ------- | -------- |
| 1    | Boston Celtics        | 0.780488 | 110.6   | 122.2   | 1        |
| 2    | Denver Nuggets        | 0.695122 | 112.3   | 117.8   | 0        |
| 3    | Oklahoma City Thunder | 0.695122 | 111     | 118.3   | 0        |

This is the main jist of the data that we will be using which shows the stats for each team. We will mainly be focusing on the offensive and defensive rating from each season which show how good or bad a team is in that category. Higher the Offensive rating the better a team was on offensive and the lower the defensive rating the better that team was at defending others.

The Champion column is a binary variable where 1 represents whether that team went on to win the championship. Our main indicator for success will be the win percentage for each team as the more games a team wins the better they theoretically are.

### Analysing the data

First let's look at the correlation between the defensive/offensive rating at the win percentage for each team in the regular season over the last 14 years.

From these 2 charts we can see that there is a negative correlation for Def Rtg with win % and a positive correlation for Off Rtg. This checks out as the lower he defensive rating the better thus the negative correlation.

We can see from both the correlation that both are extremely important to winning as the absolute correlation is around 0.5 for both. However, the correlation for offensive rating is higher with Win % which does suggest that Offensive Rating is more important. Does this hold up in the playoffs though?
