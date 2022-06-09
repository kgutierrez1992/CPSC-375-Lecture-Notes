# 5-31 Lecture Notes

First Day

Possible Zoom option, but not encouraged

- lot of group work

Profs interests

- ML
- social media
- sensor networks

## Group Activity - Meet your Partners

Cesar

- fit the schedule
- SWE with a defense contract

Rhys

- fit the schedule
- likes autonomous vehicles

Konnor

- fit the schedule
- documentation and education

## Sample Application

I-710 Freeway in LA

![the 710 isn’t fully connected. why is that?](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled.png)

the 710 isn’t fully connected. why is that?

people around the area protested having a freeway in their neighborhood

- pasadena known as a very green city. ruins aesthetics

![Untitled](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%201.png)

with this plan, how do you get feedback?

- usually through a town hall type meeting

However, they used social media for the feedback, and determined Sentiment

- Sentiment - degree of subjective positivity/negativity in a message

![Negative sentiment, but could a computer pick up on this?](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%202.png)

Negative sentiment, but could a computer pick up on this?

You can represent a whole tweet as a vector, and the 5 options, and calculate the angle between the two vectors to determine similarity

![this is hard to read, a visual aid would be helpful](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%203.png)

this is hard to read, a visual aid would be helpful

![visualization is helpful in seeing the answer](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%204.png)

visualization is helpful in seeing the answer

**Data Science** is the science which uses computer science, statistics and machine learning, visualization and human-computer interactions to collect, clean, integrate, analyze, visualize, interact with data to create data products.

- **data product**: an insight or tool created out of raw data that can be used to improve decision making

![visualization of data science](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%205.png)

visualization of data science

![Examples of data → data products](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%206.png)

Examples of data → data products

- what does data science mean?
- is it only going on at big tech companies
- what is big data?
- how big is big? or is it relative
- whats the relationship between data science and big data?
- is data science the science of big data?
- who do many people refer to big data as crossing disciplines?

## Activity 2 - Example of Data Science → Data Product

Data science application - Record Server Utilization in a data center (auvik, labtech, nagios)

- CPU utilization
- Memory utilization
- write cycles on drives

Data product 

- operating efficiency
    - if hardware needs an upgrade
    - what could be upgraded
    - is the cluster overcompensated

### Goals of data science

- turn data into data products
- it is a process
- not a science???

![Untitled](5-31%20Lecture%20Notes%207185a23543154100b2f5c5263f235dad/Untitled%207.png)

### Context of the course at CSUF

- counts for upper div
- synergistic developments
    - big data discovery & diversity
    - courses on iot in CS and CSE

### Contents of the course

70% Data Science 

- Fundamental stat analysis
- R program

30% Big Data

- fundamentals
- most poplar platforms

# Introduction to R

## What we cover today?

- Why R?
- Basic R operations and data structures

### R, S and S-Plus

- S: an interactive environment for data analysis developed at Bell Laboratories since 1976
    - 1988 - S2
    - 1992 - S3
    - 1998 - S4
- Implementation languages C, Fortran.
- R: initially written at Dept. of Statistics of U. of Auckland, New Zealand during 1990s
- Since 1997: international “R-core” team of ~20 people
- R used for data manipulation
- its an interpreted language like python
    - vector based iterations instead of loops
        - like matlab
    - includes branches and loops
    - modular programming w/ functions
    - can call C, C++ or FORTRAN modules

### R and Stats

Statistics: most packages deal with statistics and data analysis• linear and generalized linear models

- nonlinear regression models
- time series analysis
- classical parametric and nonparametric tests
- clustering
- smoothing

Implementation of high-end statistical methods

Packaging: a crucial infrastructure to efficiently produce, load and keep consistent software libraries from (many) different sources / authors

State of the art: many statistical researchers provide their methods as R packages

### Pros of R

- Free and Open Source
- Strong User Community
- Highly extensible, flexible
- Maintained by experts
- continuous improvement
- Flexible graphics and intelligent defaults
- language almost the same as S
- available on all platforms

### Cons for R

- Slow for large datasets
- All data has to fit in memory (RAM)
    - Data limited to RAM size (e.g., 8GB)
    - There are ways around it now
- Steep learning curve

Think of dataset[all rows where condition, all columns where condition]
