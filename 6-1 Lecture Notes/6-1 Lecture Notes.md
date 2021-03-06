# 6-1 Lecture Notes

# Continuing R

Working through the examples of R

Finished the R ppt with examples

# Visualization

### Whats being covered today?

- Data viz
- Grammar of graphics
    - hadley wickam’s layered grammar
    - ggplot2 in R

## Data Viz

- problem
    - big data sets. How do you understand them?
- solution
    - take better advantage of human perceptual system
    - convert info to a graphical representation
- issues
    - how to convert abstract to graphical?
    - does viz do a better job than other methods?

## Goals of info viz

- present large amounts of data
- present info from various viewpoints
- present info at several levels of detail
    - from overviews to fine structure
- support visual comparisons
- tell stories about data

![a good example of data viz](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled.png)

a good example of data viz

## Why viz?

- Use the eye for pattern recognition; people are good at

– scanning

– recognizing

– remembering images

- Graphical elements facilitate comparisons via

– length

– shape

– orientation

– texture

## Two goals of viz

- communicate
    - explain
    - make decisions
- explore/calculate
    - analyze
    - reason about info

## Types of Symbolic Displays

![Untitled](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled%201.png)

## Charts

![Untitled](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled%202.png)

## Maps

![Untitled](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled%203.png)

## Diagrams

![Untitled](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled%204.png)

## Graphs

![Untitled](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled%205.png)

## Common Graph Types

![Untitled](6-1%20Lecture%20Notes%209c602ed175c74dd18eb535b14a924f47/Untitled%206.png)

## ggplot2 philosophy

all graphs can be constructed by comboing specs with data

- a specification is a structured way to describe how to build the graph from *geometric objects (points, lines, etc)* projected on to *scales (x,y,color,size,etc)*
- Layer
    - Data
    - Mapping
    - Statistical transformation (stat)
    - Geometric object (geom)
    - Position adjustment (position)
- Scale
- Coordinate system (coord)
- Faceting (facet)
- Defaults
