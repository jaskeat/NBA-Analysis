# Do Offense or Defense Win NBA Championships? An Analytical Exploration of NBA Success

This project aims to analyze NBA Team stats from 2010 onwards to see if the quote "Defense wins championships" is really true or if offense prevails. We will be analyzing regular season and playoff success to test our hypothesis. In this project, I used Python for data analysis and visualization with the Matplotlib and Pandas libraries.

### Dataset

The data for this project was obtained from the [Official NBA website](https://www.nba.com/stats/teams/advanced). I combined the data from all the seasons. The dataset includes various metrics on the stats for each team in that season, including offensive and defensive ratings, which are crucial for understanding team performance.

#### Dataset Preview:

| Rank | Team                  | Win %    | Def Rtg | Off Rtg | Champion |
| ---- | --------------------- | -------- | ------- | ------- | -------- |
| 1    | Boston Celtics        | 0.780488 | 110.6   | 122.2   | 1        |
| 2    | Denver Nuggets        | 0.695122 | 112.3   | 117.8   | 0        |
| 3    | Oklahoma City Thunder | 0.695122 | 111     | 118.3   | 0        |

This is a snapshot of the data we will use, which shows the stats for each team over 14 seasons. In the NBA, various advanced stats exist, but we will focus on offensive and defensive ratings to assess team performance. Offensive rating measures how many points a team scores per 100 possessions, while defensive rating indicates how many points the team concedes in 100 possessions. Therefore, a lower defensive rating is better, while a higher offensive rating is preferable.

The Champion column is a binary variable where 1 represents whether that team won the championship. Our main indicator for success will be the win percentage for each team, as more wins theoretically indicate better performance. We will also consider championship status as the ultimate prize.

### Analyzing the Data

First, let's look at the correlation between the defensive and offensive ratings and the win percentage for each team in the regular season over the last 14 years.

##### Regular Season

|         Defensive Rating         |         Offensive Rating         |
| :------------------------------: | :------------------------------: |
| ![](Charts/Regular%20DefRtg.png) | ![](Charts/Regular%20OffRtg.png) |

From these two charts, we can see a negative correlation for defensive rating with win percentage and a positive correlation for offensive rating. This aligns with our understanding that a lower defensive rating is better, hence the negative correlation.

Both ratings are crucial for winning, with absolute correlations around 0.5 for both. However, the correlation for offensive rating is higher with win percentage, suggesting that offensive performance is more important. Does this hold true in the playoffs, however?

#### Playoffs

|    Playoffs Defensive Rating     |    Playoffs Offensive Rating     |
| :------------------------------: | :------------------------------: |
| ![](Charts/Playoff%20DefRtg.png) | ![](Charts/Playoff%20OffRtg.png) |

In the playoffs, we observe a similar trend where offensive rating has a higher absolute correlation with winning percentage. However, the difference between offensive and defensive ratings is smaller in the playoffs, indicating that offense may not be as critical compared to the regular season.

It’s also important to note that the sample size for the playoffs is smaller, as there are fewer games and more teams that exit without wins, leading to more outliers.

#### Offensive vs. Defensive Ranking

As a final test, let’s examine the rankings of championship teams over the years since championships are the ultimate prize. We will look at the average ranking of champions in defensive and offensive ratings.

| Average Defensive Rating Rank | Average Offensive Rating Rank |
| :---------------------------: | :---------------------------: |
|              6.1              |              5.1              |

We see that championship teams typically rank lower in defensive ratings compared to their offensive ratings.

### Considerations and possible improvements

Before we move onto the conclusions, I just want to highlight some possible improvements

1. I only used Offensive and defensive ratings to determine how good a team was on that side of the ball but that could be oversimplification so to make a more accurate analysis, other advanced stats could be used

2. I only considered seasons from 2010 which is the modern era of the NBA, the older eras were more defensive with slower pace so the results may be different for those eras. A separate analysis into the older eras could be done to prove this hypothesis.

### Conclusion

From our analysis, we can confidently conclude that while defense is a vital component of winning in the NBA, offense tends to be slightly more important. Championship teams generally exhibit better offensive stats than defensive stats, and the correlation between winning and offensive ratings is higher. This challenges the age-old saying, "Defense wins championships."
