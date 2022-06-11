# 6-6 Lecture Notes

# Review

Write in two minutes:

- 3 concepts we covered in last class
- Will call on one of you to read your answer

### 3 topics

Data Viz

- how to add packages to rstudio to enhance features. We added ggplot2 to enhance data visualization
- within ggplot2 we focused on how to make scatterplots with geom_point
- how to modify the default geom_point graph with the labs() or scale_x/y_continuous()

# Topic: Exploratory Data Analysis

EDA within R

What is it?

- step one in building a model
- data-driven (model-free)
- Goal: get a general sense of the data
    - getting your hands dirty with the data
- interactive and visiual
    - good for pattern recognition

why use this step?

- gain intuition about the data
- sanity checking
    - is the data expected?
    - are the ranges of variables expected?
- detect outliers
- test assumptions
- identify useful raw data and transforms (via log(x))
- is there missing data?
- whats the scale of the data?
    - is it big data?

![we are on the storage part for EDA](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled.png)

we are on the storage part for EDA

EDA

- systematically going through the data
    - generating summary stats
    - evaling data quality
    - visualizing each variable
    - visualizing all pairwise relationships

Summary statistics

- not visual
- is a sample statistic of data X
    - mean
    - median
    - quartiles of sorted **x:** Q1 Q3
- variance
- mode

**R commands for this:** summary(dataset)

Data quality

- is there any missing data?
    - count the NAs
    - possible that missing values are not stored as NA
        - instead, 0 or -1 or something that cannot be a valid value
    - are there outliers?
    - check for each variable
- Ways to check for weird data
    - NA - not available
    - NULL - empty value
    - Inf - infinity
    - is.na(), is.null(), is.infinite()
        - identifies missing, empty, or infinite values in a dataset respectively
    - complete.cases() to identify the rows in a data frame that are complete.
    - many functions give NA if a single NA is present such as
        - mean(x)
            - use na.rm = TRUE to remove when calling
            - mean(x, na.rm=TRUE)

Numerical vs Categorical

- numeric
    - values that can be ordered
        - age, weight, etc
    - can be calculated
    - are **ordinal** values
- categorical
    - no natural ordering between the values
        - marital status, eye color, species
    - cannot average
    - called **nominal** values

Single Variable Visualization

- Numerical:
    - histogram
    - box plot
- Categorical
    - bar graph
- The Histogram
    - shows center, variability, skewness, modality, outliers, or strange patterns
    - bin width (granularity) and position matter
    - beware of real zeros

![Untitled](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled%201.png)

With R, generate a histogram with the airquality dataset

ggplot(data=airquality)+geom_histogram(mapping = aes(x=Ozone))

- will give a warning of bin size
- to fix, use: ggplot(data=airquality)+geom_histogram(mapping = aes(x=Ozone), binwidth = 20)

Issues with Histograms

- for small datasets, histograms could be misleading
    - small changes in data, bins, or anchor can deceive
- for large datasets, histograms can be quite effective at illustrating general properties of the distribution
- histograms only work with one variable at a time

## Classwork time

Consider the data iris

1. Create a histogram of Petal.Length

2. Try different values of binwidth

3. Save final plot as a PNG file and add it to your Google Doc

## Boxplots

- shows a lot of info about a variable in one plot
    - median
    - Inter-quartile range (IQR)
    - outliers
    - range
    - skewness
- negatives
    - overplotting
    - hard to tell shape of distribution
    - no standard implementation in software (many options fo outliers and whiskers)

![diagram of a boxplot and its labels](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled%202.png)

diagram of a boxplot and its labels

Making boxplots

- a **boxplot** is a graphical display of the five number summary
    - Median (50% val)
    - quartiles
        - 1st and 3rd or 25% and 75% values
    - Extremes: max and min of the expected valid points

![5 values shown](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled%203.png)

5 values shown

Identifying outliers

- in addition to serving a s measure of spread, the IQR is used as a part of a rule of thumb for IDing outliers
- 1.5xIQR Rule: call an observation an outlier if it falls more than 1.5 x IQR above the third quartile or below the first.
    - IQR = .75 quantile - .25 quantile
    - only a rule of thumb - not every ID data point is an outlier

![Untitled](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled%204.png)

![Untitled](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled%205.png)

![Untitled](6-6%20Lecture%20Notes%20619ce54e6f084833817c98a38e65f5c5/Untitled%206.png)

Construct a boxplot of 9 values

36,42,100,28,17,12,9,4,1

- sort and find middle value for median
    - 1 4 9 12 17 28 36 42 100 = 17
- find middle of lower half for 25%
    - 9
- find middle of upper half (including median for odd vector) for 75%
    - 36
- IQR = 75% val - 25% val → 36 - 9 = 27
- Lower and Upper Bounds
    - Upper bound: 75% val + 1.5*IQR = 76.5
        - 42 is ok
    - Lower bound: 25% val - 1.5*IQR = -31.5
        - 1 is ok

100 might be erroneous, but we can’t tell for certain. we can only call it an outlier

- data is erroneous by understanding the context of the data and if it makes sense to be this value

Pairs of Variables Visualization

- comparing groups is more interesting
- two variables = scatterplot
- one numerical and one categorical = box plot
- two categorical variables = bar graph