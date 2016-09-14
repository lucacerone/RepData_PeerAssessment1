# Reproducible Research: Peer Assessment 1

## Loading required libraries and packages

```r
suppressPackageStartupMessages({
  library(dplyr)
  library(ggplot2)
})
```


## Loading and preprocessing the data

```r
if (!file.exists("activity.csv")) {
  if (!file.exists("activity.zip")) {
    download.file("https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip", "activity.zip", method = "libcurl")
  }
  unzip("activity.zip")
}
activity <- read.csv("activity.csv", header = TRUE)
head(activity)
```

```
##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```


## What is mean total number of steps taken per day?

First I calculate the number of steps taken each day:


```r
steps_per_day <- activity %>% group_by(date) %>% summarise(steps = sum(steps, na.rm = TRUE))
head(steps_per_day)
```

```
## # A tibble: 6 × 2
##         date steps
##       <fctr> <int>
## 1 2012-10-01     0
## 2 2012-10-02   126
## 3 2012-10-03 11352
## 4 2012-10-04 12116
## 5 2012-10-05 13294
## 6 2012-10-06 15420
```

The mean total number of steps taken each day is 9354.2295082 steps.

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
