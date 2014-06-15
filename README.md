Reproducible-Research---PA-1
============================

Peer Assessments for Reproducible Research of Data Science Specialization
this Peer Assessment, we have datas of steps taken in interval of 5 minutes per day.

In the raw data we only have steps (and some have missing values, introduced as NA), interval, 
and date with the following format "YYYY-MM-DD"

First of all I read the data, the name of all data is "data_PA1"
Then I add information to the data as:
  - weekday_chr: Monday, tuesday, wednesday, thursday, friday, saturday and sunday
  - week_id: 1, 2, 3, 4, 5, 6, 7. This help me to identify faster which day is in the correspondent row, during the analysis.
  - type_day: weekday, weekend. This is for the last plot asked in the peer assessment
  
I classify the data according with week information in weekday_data (data.frame)
 -weekday_chr & week_id is the same idea as before,
 - mean_steps: is the mean of the steps for the correspondent day of the week
 - median_steps: is the median of the steps for the correspondent day of the week
 - mean_steps_interv5: is the mean of the steps for the correspondent day of the week; for a 5 minutes interval.
 
 I classify the data according with day information in day_data (data.frame)
  - day: day with the following format "YYYY-MM-DD"
  - steps: number of total steps for the correspondent day in the row.
  - mean: mean of total steps for the correspondent day in the row
  - median: median of total steps for the correspondent day in the row
  
Periodically i delete some variables which are created to help in the analysis. 
I delete them to avoid misunderstanding with the code

then I plot histogram of the total number of steps taken each day called: "histogram_totalnumber_steps_each_day.png"

I add mean and median of steps per day in weekday_data data.frame
and also I add mean of steps per day for 5 minutes interval

I plot 5-minute interval (x-axis) and the average number of steps taken, 
averaged across all days (y-axis) - named: "5_minute_interval_for_all_days.png"

Then I calculate which interval has the maximun mean of steps

I create variable clean_data to know how many rows have a missing data.

To fill all of the missing values in the dataset. I have used the following strategy: mean for that day
(one sugested strategy in the peer assessment)

I plot histogram of the total number of steps taken each day without missing values
with the name: "histogram_totalnumber_steps_each_day_without_missing_values.png"

The impact of the selected methodology (in case of missing value we estimate mean for that day)
In intervals that we don't have steps for sample sleeping, we have intruce a mean.
Intervals with more steps as 8:35 has less steps than reality.

For the new variable to difference among weekday and weekend i add a column in data_PA1 called "data_PA1$type_day"
type_data variable has these values.

For the latest plot I have use lattice
The name of the plot is: "5_minute_interval_weeday_weekend.png"





