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

* Creating Vectors

 `c()` function to create vectors of objects by concatenating things together.

```
> x <- c(0.5, 0.6)       ## numeric
> x <- c(TRUE, FALSE)    ## logical
> x <- c(T, F)           ## logical
> x <- c("a", "b", "c")  ## character
> x <- 9:29              ## integer
> x <- c(1+0i, 2+4i)     ## complex
```

```
> x <- vector("numeric", length = 10) 
> x
 [1] 0 0 0 0 0 0 0 0 0 0
```

* Mixing Objects

implicit coercion

```
 > y <- c(1.7, "a")   ## character
> y <- c(TRUE, 2)    ## numeric
> y <- c("a", TRUE)  ## character
```


* Explicit Coercion

as.* functions

```
> x <- 0:6
> class(x)
[1] "integer"
> as.numeric(x)
[1] 0 1 2 3 4 5 6
> as.logical(x)
[1] FALSE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE
> as.character(x)
[1] "0" "1" "2" "3" "4" "5" "6"
```

```
> x <- c("a", "b", "c")
> as.numeric(x)
Warning: NAs introduced by coercion
[1] NA NA NA
> as.logical(x)
[1] NA NA NA
> as.complex(x)
Warning: NAs introduced by coercion
[1] NA NA NA
```

```
> x <- c("a", "b", "c")
> as.numeric(x)
Warning: NAs introduced by coercion
[1] NA NA NA
> as.logical(x)
[1] NA NA NA
> as.complex(x)
Warning: NAs introduced by coercion
[1] NA NA NA
```

nonsensical coercion results in NA



* Lists

Lists are a special type of vector that can contain elements of different classes.
very important data type in R

```
> x <- list(1, "a", TRUE, 1 + 4i) 
> x
[[1]]
[1] 1

[[2]]
[1] "a"

[[3]]
[1] TRUE

[[4]]
[1] 1+4i
```

the elements are double brackets [[1]]














### R Data Types: Matrices


* dimension attribute

Matrices are vectors with a dimension attribute that is an integer vector of length 2 (number of rows, number of columns)

```
> m <- matrix(nrow = 2, ncol = 3) 
> m
     [,1] [,2] [,3]
[1,]   NA   NA   NA
[2,]   NA   NA   NA
> dim(m)
[1] 2 3
> attributes(m)
$dim
[1] 2 3

```


* column-wise

Matrices are constructed column-wise, so entries can be thought of starting in the “upper left” corner and running down the columns.


```
> m <- matrix(1:6, nrow = 2, ncol = 3) 
> m
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6
```

* dimension attribute direct create

* Matrices can also be created directly from vectors by adding a dimension attribute.

```
> m <- 1:10
> m
 [1]  1  2  3  4  5  6  7  8  9 10
> dim(m)<-c(2,5)
> m
     [,1] [,2] [,3] [,4] [,5]
[1,]    1    3    5    7    9
[2,]    2    4    6    8   10
```

* cbinging and rbinding

Matrices can be created by column-binding or row-binding with the cbind() and rbind() functions.

```
> x <- 1:3
> y <- 10:12
> cbind(x, y)
     x  y
[1,] 1 10
[2,] 2 11
[3,] 3 12
> rbind(x, y) 
  [,1] [,2] [,3]
x    1    2    3
y   10   11   12
```






### R Data Types: Factors


* categorical

To represent categorical data, unordered or ordered. 

* label

as an integer vector where each integer has a label. 

important in statistical modeling and are treated specially by modelling functions like lm() and glm().

* self-describing

Using factors with labels is better than using integers because factors are self-describing. Having a variable that has values “Male” and “Female” is better than a variable that has values 1 and 2.


```
> x <- factor(c("yes", "yes", "no", "yes", "no")) 
> x
[1] yes yes no  yes no 
Levels: no yes
> table(x) 
x
 no yes 
  2   3 
> ## See the underlying representation of factor
> unclass(x)  
[1] 2 2 1 2 1
attr(,"levels")
[1] "no"  "yes"
```

* set order of levels
The order of the levels of a factor can be set using the levels argument to factor(). This can be important in linear modelling because the first level is used as the baseline level.

```
> x <- factor(c("yes", "yes", "no", "yes", "no"))
> x  ## Levels are put in alphabetical order
[1] yes yes no  yes no 
Levels: no yes
> x <- factor(c("yes", "yes", "no", "yes", "no"),
+             levels = c("yes", "no"))
> x
[1] yes yes no  yes no 
Levels: yes no
```


### R Data Types: Missing Values

Missing values are denoted by NA or NaN for undefined mathematical operations.

* is.na() is used to test objects if they are NA

* is.nan() is used to test for NaN

* NA values have a class also, so there are integer NA, character NA, etc.

* A NaN value is also NA but the converse is not true


```
> ## Create a vector with NAs in it
> x <- c(1, 2, NA, 10, 3)  
> ## Return a logical vector indicating which elements are NA
> is.na(x)    
[1] FALSE FALSE  TRUE FALSE FALSE
> ## Return a logical vector indicating which elements are NaN
> is.nan(x)   
[1] FALSE FALSE FALSE FALSE FALSE
```


### R Data Types: Data Frames

* store tabular data

* Data frames are represented as a special type of list where every element of the list has to have the same length. Each element of the list can be thought of as a column and the length of each element of the list is the number of rows.

* Unlike matrices, data frames can store different classes of objects in each column. Matrices must have every element be the same class.

* Data frames have a special attribute called row.names.

* Data frames are usually created by reading in a dataset using the read.table() or read.csv().

* Data frames can be converted to a matrix by calling data.matrix(). 

```
> x <- data.frame(foo = 1:4, bar = c(T, T, F, F)) 
> x
  foo   bar
1   1  TRUE
2   2  TRUE
3   3 FALSE
4   4 FALSE
> nrow(x)
[1] 4
> ncol(x)
[1] 2
```



### R Data Types: Names Attribute

R objects can have names, which is very useful for writing readable code and self-describing objects. 

```
> x <- 1:3
> names(x)
NULL
> names(x) <- c("New York", "Seattle", "Los Angeles") 
> x
   New York     Seattle Los Angeles 
          1           2           3 
> names(x)
[1] "New York"    "Seattle"     "Los Angeles"
```


Lists can also have names

```
> x <- list("Los Angeles" = 1, Boston = 2, London = 3) 
> x
$`Los Angeles`
[1] 1
$Boston
[1] 2
$London
[1] 3
> names(x)
[1] "Los Angeles" "Boston"      "London"     
```

Matrices can have both column and row names.

```
> m <- matrix(1:4, nrow = 2, ncol = 2)
> dimnames(m) <- list(c("a", "b"), c("c", "d")) 
> m
  c d
a 1 3
b 2 4
```


| Object     | Set column names | Set row names |
| ---------- | ---------------- | ------------- |
| data frame | names()          | row.names()   |
| matrix     | colnames()       | rownames()    |


### R Data Types: Summary







### Reading Tabular Data






### Reading Large Tables





### Textual Data Formats



