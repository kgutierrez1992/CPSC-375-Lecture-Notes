# 6-7 Lecture Notes

# TOPIC: Data Wrangling

80% is cleaning the data, and 20% is complaining about it

## Data Wrangling in Tidyverse

- Data wrangling:

– transforming data from one form into another

form with the intent of making it more suitable

for later analysis

- Also called data munging
- Base R functions can be used to wrangle data

– Bracket-based subsetting

- A more complete set of functions in tidyverse

– tidyr and dplyr packages developed by Hadley

Wickham

- Called “verbs” – the language of data cleaning

– A grammar of data manipulation

- Install the tidyverse package

## Core data wrangling verbs

- filter - remove rows
    - subset observations based on their values
    - first argument:
    
    – name of the data frame
    
    - second (and subsequent arguments):
    
    – expressions that filter the data frame
    
- select - remove columns
- Get column subset using operations based on the names of the variables
    - Parameters:
    
    – the data frame
    
    – a set of column names to select
    
- arrange - add of modify variables
    - change the order of rows (sorting
    - parameters
        - names of columns
        - additional colums used to break ties in the values of the preceding columns
    - ascending order by default
        - descending order: desc(value) or -value
- mutate -
    - add new columns that are functions of existing columns
    - always adds new columns at the end of the dataset
- summarize - collapse multiple values into a single value
    
    
    - Collapses a data frame to a single row
    - E.g.:
    
    – By summing or taking the mean of a column
    
    - airquality %>% summarise(mean(Wind))
    - airquality %>% summarise(n())
    
    – Note: n() is a function that just counts the rows
    
- group_by - divide dataset into subgroups
    - Divides data into non-overlapping groups
    - Divide dataset according to one or more categorical variables
    
    cars_by_manuf <- group_by(manufacturer)
    
    – Original dataset had one group (the whole data)
    
    – Transformed dataset has one group for every unique manufacturer
    

## Pipe commands

An alternative syntax emerged long ago from Unix terminal programming:• find . –iname '*.pdf' | grep –v 'figure' | sort –n

- The idea of "pipes" and "redirection" in shell

scripting is that the commands can be read from left to right where the pipe | indicates:

– output of left command is the input to the right command

- This syntax makes multi-step chains easier to see
- Pipe operator %>%
- All dplyr functions can be piped

> mpg %>% filter(cty > 25) %>% select(manufacturer)

– An example of one pipeline

- Compare with:

> select(filter(mpg, cty > 25), manufacturer, mpg)