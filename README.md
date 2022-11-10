### Predicting the points scored and allowed for the 2022/23 NFL season

## Introduction

The goal of this repository was to try and predict how many points a team would score and allow in the 2022/23 season based on the 3 previous seasons statistics. All the data was collected from ProFootballReference.com. A random forest regression and multiple linear regressions were used to examine which statistics are more predictive of points on both sides of the ball. 
If this would like to be required, the following module and extensions would need to be installed: 
Pandas, Matplotlib, Numpy, Sklearn and ipywidgets.

## Scraping

Firstly, the data was scraped from Pro football reference. The datasets used for predicting points scored were advanced passing, advanced team rushing and scoring ofense. The data sets used for predicting points allowed were advanced team passing defence and advanced rushing defense.

## Analysis

Once imported the process for both allowed and for were the same. A random forest regression was used to see which statistics correlated best with the statistic that the regression was predicted for. Then those statistics were defined as x to be able to perform a multiple linear regression. The model created by this was then reused with the current seasons data which was modified by dividing by the games played and multiplied by the number of games in a season to emulate the full season statistics. After a prediction was created for each team, they were subtracted by the season projection for points scored or conceded using the same method above. 

## Results

The number retrieved from this was used to show if a team was over or underperforming. There are many factors that can impact this such as turnovers and defensive scores, field position and late game decisions. In the points allowed analysis no team had a differential a game of more than 6 points (1 Touchdown) and 24/32 had a differential below 3 (1 Field goal). This can be considered reasonably successful as the field goal is the minimum points allowed by a defence. On offense 1 team had a differential more than 7 and 20/32 were below 3. The mean of the differential for points scored was -2.8 and 2.1. The mean of the differential for points allowed was -1.9 and 1.8.

## Evaluation

This project could be improved by using more variables that differ from the data sets used such as penalties, time, previous game result (win/loss) and weather. Home and away splits should be used in future as well as predicting the number of points conceded and scored against specific teams based on their predictions.
