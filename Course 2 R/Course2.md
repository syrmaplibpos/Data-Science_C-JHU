# [Coursera 2: R Programming](https://www.coursera.org/learn/r-programming/home/welcome)

- [Coursera 2: R Programming](#coursera-2-r-programming)
  - [Week 1 Background, Getting Started, and Nuts & Bolts](#week-1-background-getting-started-and-nuts--bolts)
    - [Background Material](#background-material)
    - [Getting Started, and Nuts & Bolts](#getting-started-and-nuts--bolts)
    - [Introduction](#introduction)
    - [Overview and History](#overview-and-history)
    - [Getting help](#getting-help)
    - [R Console Input and Evaluation](#r-console-input-and-evaluation)
    - [R Data Types: Objects and Attributes](#r-data-types-objects-and-attributes)
      - [Objects](#objects)
      - [Attributes](#attributes)
    - [R Data Types: Vectors and Lists](#r-data-types-vectors-and-lists)
    - [R Data Types: Matrices](#r-data-types-matrices)
    - [R Data Types: Factors](#r-data-types-factors)
    - [R Data Types: Missing Values](#r-data-types-missing-values)
    - [R Data Types: Data Frames](#r-data-types-data-frames)
    - [R Data Types: Names Attribute](#r-data-types-names-attribute)
    - [R Data Types: Summary](#r-data-types-summary)
    - [Reading Tabular Data](#reading-tabular-data)
    - [Reading Large Tables](#reading-large-tables)
    - [Textual Data Formats](#textual-data-formats)



## Week 1 Background, Getting Started, and Nuts & Bolts

### Background Material

Week 1: Overview of R, R data types and objects, reading and writing data

Week 2: Control structures, functions, scoping rules, dates and times

Week 3: Loop functions, debugging tools

Week 4: Simulation, code profiling

* Course Textbook

[R Programming for Data Science (read on leanpub)](https://leanpub.com/rprogramming/read_full)

[R Programming for Data Science (purchase link)](http://bit.ly/rprogrammingcoursera)

[leanpub categories](https://leanpub.com)

[R Programming Course Companion](http://apple.co/1AAfjiY)

* Quizzes

four weekly quizzes. 

up to 3 times in 8 hours.


* Programming Assignments

three required

1 and 3 graded via script that compares, 2 graded via a peer review.

* swirl Programming Assignment (practice)

[swirl R package](http://swirlstats.com/)

completely optional

* Grading Policy

score at least 80% on all required assignments

Week 1 Quiz - 20%

Week 2 Quiz - 10%

Week 3 Quiz - 5%

Week 4 Quiz - 10%

Programming Assignment 1 (Air Pollution) - 20%

Programming Assignment 2 (Lexical Scoping) - 10%

Programming Assignment 3 (Hospital Quality) - 25%

swirl Programming Assignment (practice) - 0% 

* Anonymity

set up an anonymous Github account 

[Course Supplement: The Art of Data Science](https://leanpub.com/artofdatascience/)

[Data Science Podcast: Not So Standard Deviations](https://soundcloud.com/nssd-podcast)


### Getting Started, and Nuts & Bolts

Learning Objectives

Install the R and RStudio software packages

Download and install the swirl package for R

Describe the history of the S and R programming lectures

Describe the differences between atomic data types

Execute basic arithmetic operations

Subset R objects using the "[", "[[", and "$" operators and logical vectors

Describe the explicit coercion feature of R

Remove missing (NA) values from a vector

### Introduction
### Overview and History
### Getting help

* Asking questions

What steps will produce the problem

what is the expected output

what do you see instead

what version of the product (e.g. R, packages, etc.) are you using

what operating system

additonal information


* Smarter subject header

R.3.0.2 Im() function on Mac OS X 10.9.1 --seg fault on large data frame

* Wrong email example

Questions sent to wrong email list

email subject was very vague 

question was very vague

problem was not producible

no evidence of any effort made to solve the problem

result: recipe for diaster

* Place to turn

class dicussion forum, fellow students

r-help@r-project.org

other project specific mailing lists (eric raymond: how to ask questions in a smart way)

[Base R Cheatsheet](http://github.com/rstudio/cheatsheets/blob/main/base-r.pdf)

[RStudio Cheatsheet](https://www.rstudio.com/resources/cheatsheets/)

### R Console Input and Evaluation

* Entering input

`>` to assign

`> x<-5 ## comment`

`#`to comment

* Evaluation

```
> x
[1] 5
```
when enter at the prompt, it is evaluated and result of the evaluated expression is returned

The [1] indicates that x is a vector and 5 is the first element

* Printing

```
> x <- 1:20
> x
[1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15
[16] 16 17 18 19 20
```

the `:` operator to create integer sequences



### R Data Types: Objects and Attributes

#### Objects 

R has five basic or “atomic” classes of objects:

* character

* numeric (real numbers)

* integer

* complex

* logical (True/False)

The most basic type of R object is a vector.

`vector()` to create empty vector

**A vector can only contain objects of the same class.**

**A list is represented as a vector but can contain objects of different classes.**

* Numbers 1, 2 are numeric objects, unless specify by using 1L, 2L as integer object.

Number **Inf** infinity, can be used in ordinary calculations

value **NaN** an undefined value (“not a number”); e.g. 0 / 0; 

NaN can also be thought of as a missing value (more on that later)

#### Attributes

**metadata, help to describe the object**

names, dimnames

dimensions (e.g. matrices, arrays)

class (e.g. integer, numeric)

length

other user-defined attributes/metadata





### R Data Types: Vectors and Lists

Creating Vectors

 `c()` function to create vectors of objects by concatenating things together.

```

> x <- c(0.5, 0.6)       ## numeric
> x <- c(TRUE, FALSE)    ## logical
> x <- c(T, F)           ## logical
> x <- c("a", "b", "c")  ## character
> x <- 9:29              ## integer
> x <- c(1+0i, 2+4i)     ## complex

```











### R Data Types: Matrices

### R Data Types: Factors

### R Data Types: Missing Values

### R Data Types: Data Frames

### R Data Types: Names Attribute

### R Data Types: Summary

### Reading Tabular Data

### Reading Large Tables

### Textual Data Formats



