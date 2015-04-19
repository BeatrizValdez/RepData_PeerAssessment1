## Introduction

For this  assignment I have made use of dataset from a personal activity monitoring device provided by the instructor and downloaded from github to my computermber of steps taken in 5 minute intervals each day.

## Data

The data for this assignment has been downloaded from the course web
site:

* Dataset: [Activity monitoring data](https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip) [52K], which was stored in a comma-separated-value and had 17,568 observations and three variables:

* **steps**: Number of steps taking in a 5-minute interval (missing
    values are coded as `NA`)

* **date**: The date on which the measurement was taken in YYYY-MM-DD
    format

* **interval**: Identifier for the 5-minute interval in which
    measurement was taken

The dataset had a total of **2,304 missing values**. I have imputed those values using the mean of total steps taken by interval. To do so, I have followed these steps:


* group the data by 5-minutes interval
* compute the mean on those intervals
* use the computed mean where  there is a NA, or use the real mean otherwise, storing all these values in a vector
* create a new data frame where the  vector created above is the new 'steps' variable, and adding the existing variables 'date' and 'interval'


## Findings

* The mean of the total number of steps taken per day is **10,766.19** and the median is **10,765.00**. The maximum number of steps that have been taken, in average, in the 5-minutes interval is in the **interval number 2083,  on November 23, 2012**.

* After imputing missing data, I have obtained a mean of **10,765.64** and a median of **10,762.00**. These results are very closed to the values previously estimated. In the present activity, imputing data seems to have had  none impact on the estimates of the averages of total daily number of steps, despite the fact that the total daily number of steps have increased. 

*  Finally, the total number of steps taken increased on average during the weekend w.r.t the weekdays. On weekends the mean is 41.9, while during the week is 36.6. More free time, more steps taken.