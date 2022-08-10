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
    - [Connections: Interfaces to the outside world](#connections-interfaces-to-the-outside-world)
    - [Subsetting - Basics](#subsetting---basics)
    - [Subsetting - Lists](#subsetting---lists)
    - [Subsetting - Matrices](#subsetting---matrices)
    - [Subsetting - Partial Matching](#subsetting---partial-matching)
    - [Subsetting - Removing Missing Values](#subsetting---removing-missing-values)
    - [Vectorized Operations](#vectorized-operations)
  - [Quiz](#quiz)
  - [Week 2 Programming with R](#week-2-programming-with-r)
    - [Control Structures - Introduction](#control-structures---introduction)
    - [Control Structures - If-else](#control-structures---if-else)
    - [Control Structures - For loops](#control-structures---for-loops)
    - [Control Structures - While loops](#control-structures---while-loops)
    - [Control Structures - Repeat, Next, Break](#control-structures---repeat-next-break)
    - [Your First R Function](#your-first-r-function)
    - [Functions (part 1)](#functions-part-1)
    - [Functions (part 2)](#functions-part-2)
    - [Scoping Rules Symbol Binding](#scoping-rules-symbol-binding)
    - [Scoping Rules - R Scoping Rules](#scoping-rules---r-scoping-rules)
    - [Scoping Rules - Optimization Example (Optional)](#scoping-rules---optimization-example-optional)
    - [Coding Standards](#coding-standards)
    - [Dates and times](#dates-and-times)
    - [Quiz](#quiz-1)
    - [Programming Assignment](#programming-assignment)



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

* atomic classes: numeric, logical, character, integer, complex

* vectors, lists

* factors

* missing values

* data frames

* names

Attributes: name (column or row name), dim


### Reading Tabular Data

* Reading data

There are a few principal functions reading data into R.

read.table, read.csv, for reading tabular data

readLines, for reading lines of a text file

source, for reading in R code files (inverse of dump)

dget, for reading in R code files (inverse of dput)

load, for reading in saved workspaces

unserialize, for reading single R objects in binary form

* Writing data

There are analogous functions for writing data to files

write.table, for writing tabular data to text files (i.e. CSV) or connections

writeLines, for writing character data line-by-line to a file or connection

dump, for dumping a textual representation of multiple R objects

dput, for outputting a textual representation of an R object

save, for saving an arbitrary number of R objects in binary format (possibly compressed) to a file.

serialize, for converting an R object into a binary format for outputting to a connection (or file).


* Reading Data Files with read.table()

The read.table() function is one of the most commonly used functions for reading data.

file, the name of a file, or a connection

header, logical indicating if the file has a header line

sep, a string indicating how the columns are separated

colClasses, a character vector indicating the class of each column in the dataset

nrows, the number of rows in the dataset. By default read.table() reads an entire file.

comment.char, a character string indicating the comment character. This defalts to "#". If there are no commented lines in your file, it’s worth setting this to be the empty string "".

skip, the number of lines to skip from the beginning

stringsAsFactors, should character variables be coded as factors?


* For small to moderately sized datasets, you can usually call read.table without specifying any other arguments

`> data <- read.table("foo.txt")`

R will automatically

* * skip lines that begin with a #

* * figure out how many rows there are (and how much memory needs to be allocated)

* * figure what type of variable is in each column of the table.



### Reading Large Tables

With much larger datasets, there are a few things that you can do that will make your life easier and will prevent R from choking.

* Read the help page for read.table, which contains many hints

* Make a rough calculation of the memory required to store your dataset. If the dataset is larger than the amount of RAM on your computer, you can probably stop right here.

* Set comment.char = "" if there are no commented lines in your file.

* Use the colClasses argument. Specifying this option instead of using the default can make ’read.table’ run MUCH faster, often twice as fast. In order to use this option, you have to know the class of each column in your data frame. If all of the columns are “numeric”, for example, then you can just set colClasses = "numeric". A quick an dirty way to figure out the classes of each column is the following:

```
> initial <- read.table("datatable.txt", nrows = 100)
> classes <- sapply(initial, class)
> tabAll <- read.table("datatable.txt", colClasses = classes)
```

* Set nrows. This doesn’t make R run faster but it helps with memory usage. A mild overestimate is okay. You can use the Unix tool wc to calculate the number of lines in a file.

* know the system

In general, when using R with larger datasets, it’s also useful to know a few things about your system.

* * How much memory is available on your system?
* * What other applications are in use? Can you close any of them?
* * Are there other users logged into the same system?
* * What operating system ar you using? Some operating systems can limit the amount of memory a single process can access


* Calculating Memory Requirements for R Objects

I have a data frame with 1,500,000 rows and 120 columns, all of which are numeric data. Roughly, how much memory is required to store this data frame? 

1,500,000 × 120 × 8 bytes/numeric	= 1,440,000,000 bytes
 	= 1,440,000,000 / 2^20 bytes/MB
 	= 1,373.29 MB
 	= 1.34 GB


### Textual Data Formats

Using the dput() or dump() functions to create a more descriptive representation of an R object

* The dump() and dput() functions are useful because the resulting textual format is edit-able, and in the case of corruption, potentially recoverable. 

* Unlike writing out a table or CSV file, dump() and dput() preserve the metadata (sacrificing some readability), so that another user doesn’t have to specify it all over again.

* Textual formats can work much better with version control programs like subversion or git which can only track changes meaningfully in text files.

* Textual formats can be longer-lived; if there is corruption somewhere in the file, it can be easier to fix the problem

* Textual formats adhere to the Unix philosophy

* DownsideThe format is not very space-efficient


One way to pass data around is by deparsing the R object with dput() and reading it back in (parsing it) using dget().

```
> ## Create a data frame
> y <- data.frame(a = 1, b = "a")  
> ## Print 'dput' output to console
> dput(y)                          
structure(list(a = 1, b = "a"), class = "data.frame", row.names = c(NA, 
-1L))
```

```
> ## Send 'dput' output to a file
> dput(y, file = "y.R")            
> ## Read in 'dput' output from a file
> new.y <- dget("y.R")             
> new.y
  a b
1 1 a
```

Multiple objects can be deparsed at once using the dump function and read back in using source.

```
> x <- "foo"
> y <- data.frame(a = 1L, b = "a")

> dump(c("x", "y"), file = "data.R") 
> rm(x, y)

> source ("data.R")
> y
  a b
1 1 a
> x
[1] "foo"
```


### Connections: Interfaces to the outside world

* connection interfaces

Data are read in using connection interfaces. Connections can be made to files (most common) or to other more exotic things.

file, opens a connection to a file

gzfile, opens a connection to a file compressed with gzip

bzfile, opens a connection to a file compressed with bzip2

url, opens a connection to a webpage

* File Connections

Connections to text files can be created with the file() function.

```
> str(file)
function (description = "", open = "", blocking = TRUE, encoding = getOption("encoding"), 
    raw = FALSE, method = getOption("url.method", "default"))  
```

str(file): Str() function is to output the structure of a R object

* * description is the name of the file

* * open is a code indicating what mode the file should be opened in, is the only important option

“r” open file in read only mode

“w” open a file for writing (and initializing a new file)

“a” open a file for appending

“rb”, “wb”, “ab” reading, writing, or appending in binary mode (Windows)


In general, connections are powerful tools that let you navigate files or other external objects. 

* In practice, we often don’t need to deal with the connection interface directly as many functions for reading and writing data just deal with it in the background.

If explicitly use connections to read a CSV file in to R

```
> ## Create a connection to 'foo.txt'
> con <- file("foo.txt")       
> 
> ## Open connection to 'foo.txt' in read-only mode
> open(con, "r")               
> 
> ## Read from the connection
> data <- read.csv(con)        
> 
> ## Close the connection
> close(con)                   
```

**which is the same as**

```
> data <- read.csv("foo.txt")
```

In the background, read.csv() opens a connection to the file foo.txt, reads from it, and closes the connection when it’s done.


* Reading Lines of a Text File

Sometimes connection is useful if wanna read parts of a file

Text files can be read line by line using the readLines() function. This function is useful for reading text files that may be unstructured or contain non-standard data.

```
> ## Open connection to gz-compressed text file
> con <- gzfile("words.gz")   
> x <- readLines(con, 10) 
> x
 [1] "1080"     "10-point" "10th"     "11-point" "12-point" "16-point"
 [7] "18-point" "1st"      "2"        "20-point"
```

gzfile(): to read from a file without uncompress the file first, which would be a waste of space and time.

Similarly, writeLines() that takes a character vector and writes each element of the vector one line at a time to a text file.


* Reading From a URL Connection

The readLines() function can be useful for reading in lines of webpages.

This code might take time depending on connection speed.

```
> ## Open a URL connection for reading
> con <- url("https://www.jhu.edu", "r")  
> 
> ## Read the web page
> x <- readLines(con)                      
> 
> ## Print out the first few lines
> head(x)                                  
[1] "<!doctype html>"                    ""                                  
[3] "<html class=\"no-js\" lang=\"en\">" "  <head>"                          
[5] "    <script>"                       "    dataLayer = [];"               
```

the lines from html will be stored in character vector x

url() function to create a url connection to a web server.

more commonly, use URL connection to read in specific data files that are stored on web servers, and preferable to opening a web browser and downloading a dataset by hand




### Subsetting - Basics

There are three operators that can be used to extract subsets of R objects.

* The [ operator always returns an object of the same class as the original. It can be used to select multiple elements of an object

* The [[ operator is used to extract elements of a list or a data frame. It can only be used to extract a single element and the class of the returned object will not necessarily be a list or data frame.

* The $ operator is used to extract elements of a list or data frame by literal name. Its semantics are similar to that of [[.


* Subsetting a Vector

```
> x <- c("a", "b", "c", "c", "d", "a")  
> x[1]    ## Extract the first element
[1] "a"
> x[2]    ## Extract the second element
[1] "b"

```

passing the operator an integer sequence

```

> x[1:4]
[1] "a" "b" "c" "c"
```

pass a logical sequence

```

> x[x > "a"]
[1] "b" "c" "c" "d"

> u <- x > "a"
> u
[1] FALSE  TRUE  TRUE  TRUE  TRUE FALSE
> x[u]
[1] "b" "c" "c" "d"
```


### Subsetting - Lists


`> x <- list(foo = 1:4, bar = 0.6)`

* []

```
> x[1]
$foo
[1] 1 2 3 4
```

get a list that contain sequence 1-4

* [[]]

```
> x[[1]]
[1] 1 2 3 4
```

get just the sequence

* $

```
> x[["bar"]]
[1] 0.6
> x$bar
[1] 0.6
> x["bar"]
$bar
[1] 0.6
```

get the element associated with the name bar

extract multiple element of the list

```
> x <- list(foo = 1:4, bar = 0.6, baz = "hello")
> x[c(1,3)]
$foo
[1] 1 2 3 4

$baz
[1] "hello"
```


The [[ operator can be used with computed index; $ can only be used with literal names

```
> x <- list(foo = 1:4, bar = 0.6, baz = "hello")
> name <- "foo"
> 
> ## computed index for "foo"
> x[[name]]  
[1] 1 2 3 4
> 
> ## element "name" doesn't exist! (but no error here)
> x$name     
NULL
> 
> ## element "foo" does exist
> x$foo      
[1] 1 2 3 4
```

The [[ operator can take an integer sequence if you want to extract a nested element of a list.

```
> x <- list(a = list(10, 12, 14), b = c(3.14, 2.81))
> 
> ## Get the 3rd element of the 1st element
> x[[c(1, 3)]]  
[1] 14
> 
> ## Same as above
> x[[1]][[3]]   
[1] 14
> 
> ## 1st element of the 2nd element
> x[[c(2, 1)]]  
[1] 3.14
```




### Subsetting - Matrices

Matrices can be subsetted in the usual way with (i,j) type indices

```
> x <- matrix(1:6, 2, 3)
> x
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6

> x[1, 2]
[1] 3
> x[2, 1]
[1] 2
```

indices can also be missing

```
> x[1, ]  ## Extract the first row
[1] 1 3 5
> x[, 2]  ## Extract the second column
[1] 3 4
```


* By default, when a single element of a matrix is retrieved, it is returned as a vector of length 1 rather than a 1\times1 matrix. Often, this is exactly what we want, but this behavior can be turned off by setting drop = FALSE.

```
> x <- matrix(1:6, 2, 3)
> x[1, 2]
[1] 3
> x[1, 2, drop = FALSE]
     [,1]
[1,]    3
```


Similarly, subsetting a single column or a single row will give you a vector, not a martrix (by default).

```
> x <- matrix(1:6, 2, 3)
> x[1, ]
[1] 1 3 5
> x[1, , drop = FALSE]
     [,1] [,2] [,3]
[1,]    1    3    5
```



### Subsetting - Partial Matching



Partial matching of names is allowed with [[ and $

```
> x <- list(aardvark = 1:5)
> x$a
[1] 1 2 3 4 5
> x[["a"]]
NULL
> x[["a", exact = FALSE]]
[1] 1 2 3 4 5
```



### Subsetting - Removing Missing Values

A common task is to remove missing values (NAS)

```
> x <- c(1, 2, NA, 4, NA, 5)
> bad <- is.na(x)
> print(bad)
[1] FALSE FALSE  TRUE FALSE  TRUE FALSE
> x[!bad]
[1] 1 2 4 5
```

What if there are multiple things and you want to take the subset with no missing values


```
> x <- c(1, 2, NA, 4, NA, 5)
> y <- c("a", "b", NA, "d", NA, "f")
> good <- complete.cases(x, y)
> good
[1]  TRUE  TRUE FALSE  TRUE FALSE  TRUE
> x[good]
[1] 1 2 4 5
> y[good]
[1] "a" "b" "d" "f"
```

check which position both elements not missing, if the 5 becomes NA, then x wont print element in the position for both

use complete.cases on data frames too.

```
> airquality[1:6, ]
  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2
3    12     149 12.6   74     5   3
4    18     313 11.5   62     5   4
5    NA      NA 14.3   56     5   5
6    28      NA 14.9   66     5   6
> good <- complete.cases(airquality)
> airquality[good, ][1:6, ]
  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2
3    12     149 12.6   74     5   3
4    18     313 11.5   62     5   4
7    23     299  8.6   65     5   7
8    19      99 13.8   59     5   8
```


### Vectorized Operations


Many operations in R are vectorized, meaning that operations occur in parallel in certain R objects, making code more efficient, concise, and easier to read

To replace loop operation like for or while

```
> x <- 1:4; y <- 6:9
> x+y
[1]  7  9 11 13
> x>2
[1] FALSE FALSE  TRUE  TRUE
> x>=2
[1] FALSE  TRUE  TRUE  TRUE
> x==8
[1] FALSE FALSE FALSE FALSE
> x*y
[1]  6 14 24 36
> x/y
[1] 0.1666667 0.2857143 0.3750000 0.4444444
```

Vectorized Matrix Operations

```
> x <- matrix(1:4, 2, 2)
> y <- matrix(rep(10, 4), 2, 2)
> x
     [,1] [,2]
[1,]    1    3
[2,]    2    4
> y
     [,1] [,2]
[1,]   10   10
[2,]   10   10
>
> ## element-wise multiplication
> x * y       
     [,1] [,2]
[1,]   10   30
[2,]   20   40
>
> ## element-wise division
> x / y       
     [,1] [,2]
[1,]  0.1  0.3
[2,]  0.2  0.4
> 
> ## true matrix multiplication
> x %*% y     
     [,1] [,2]
[1,]   40   40
[2,]   60   60
```



## Quiz

1.Question 1
R was developed by statisticians working at

The University of Auckland

Bell Labs &check;

Harvard University

The University of New South Wales

2.Question 2
The definition of free software consists of four freedoms (freedoms 0 through 3). Which of the following is NOT one of the freedoms that are part of the definition?  Select all that apply.

The freedom to prevent users from using the software for undesirable purposes. &check;

The freedom to redistribute copies so you can help your neighbor.

The freedom to run the program, for any purpose.

The freedom to sell the software for any price. &check;

The freedom to improve the program, and release your improvements to the public, so that the whole community benefits.

The freedom to study how the program works, and adapt it to your needs.

The freedom to restrict access to the source code for the software. &check;

3.Question 3
In R the following are all atomic data types EXCEPT: (Select all that apply)

table

logical &check;

list

integer &check;

data frame

matrix

array

complex &check;

numeric &check;

character &check;

4.Question 4
If I execute the expression x <- 4L in R, what is the class of the object `x' as determined by the `class()' function?

matrix

complex

character

numeric

integer &check;

logical

5.Question 5
What is the class of the object defined by the expression x <- c(4, "a", TRUE)?

mixed

numeric

integer

logical

character &check;

6.Question 6
If I have two vectors x <- c(1,3, 5) and y <- c(3, 2, 10), what is produced by the expression rbind(x, y)?

a vector of length 3

a matrix with two rows and three columns &check;

a 3 by 3 matrix

a 3 by 2 matrix

a 2 by 2 matrix

a vector of length 2

7.Question 7
A key property of vectors in R is that

the length of a vector must be less than 32,768

a vector cannot have have attributes like dimensions

elements of a vector can be of different classes

elements of a vector all must be of the same class &check;

elements of a vector can only be character or numeric

8.Question 8
Suppose I have a list defined as x <- list(2, "a", "b", TRUE). What does x[[1]] give me? Select all that apply.

a list containing the number 2.

a numeric vector containing the element 2. &check;

a list containing a numeric vector of length 1.

a character vector containing the element "2".

a numeric vector of length 1. &check;

9.Question 9
Suppose I have a vector x <- 1:4 and a vector y <- 2. What is produced by the expression x + y?

a numeric vector with elements 3, 4, 5, 6. &check;

a numeric vector with elements 3, 2, 3, 6.

an integer vector with elements 3, 2, 3, 4.

a numeric vector with elements 3, 2, 3, 4.

an integer vector with elements 3, 2, 3, 6.

a numeric vector with elements 1, 2, 3, 6.

10.Question 10
Suppose I have a vector x <- c(17, 14, 4, 5, 13, 12, 10) and I want to set all elements of this vector that are greater than 10 to be equal to 4. What R code achieves this? Select all that apply.

x[x >= 10] <- 4

x[x > 10] <- 4 &check;

x[x == 10] <- 4

x[x >= 11] <- 4 &check;

x[x > 10] == 4

x[x > 4] <- 10

x[x == 4] > 10

x[x < 10] <- 4

11.Question 11
Use the Week 1 Quiz Data Set to answer questions 11-20.

In the dataset provided for this Quiz, what are the column names of the dataset? 

Ozone, Solar.R, Wind

Ozone, Solar.R, Wind, Temp, Month, Day &check;

1, 2, 3, 4, 5, 6

Month, Day, Temp, Wind

```
>getwd()
>dir()
>tall<-read.csv("hw1_data.csv")
> names(tall)
[1] "Ozone"   "Solar.R" "Wind"    "Temp"    "Month"   "Day"  
```

12.Question 12
Extract the first 2 rows of the data frame and print them to the console. What does the output look like?

```
> tall[1:2,]
  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2
```


13.Question 13
How many observations (i.e. rows) are in this data frame?

```
> nrow(tall)
[1] 153
```

14.Question 14
Extract the last 2 rows of the data frame and print them to the console. What does the output look like?

```
> tall[152:153,]
    Ozone Solar.R Wind Temp Month Day
152    18     131  8.0   76     9  29
153    20     223 11.5   68     9  30
```

15.Question 15
What is the value of Ozone in the 47th row?

```
> tall[47,"Ozone"]
[1] 21
```

16.Question 16
How many missing values are in the Ozone column of this data frame?

```
> bad<-is.na(tall["Ozone"])
> length(tall["Ozone"][bad])
[1] 37
```

17.Question 17
What is the mean of the Ozone column in this dataset? Exclude missing values (coded as NA) from this calculation.

```
> mean(tall["Ozone"][!bad])
[1] 42.12931
```

18.Question 18
Extract the subset of rows of the data frame where Ozone values are above 31 and Temp values are above 90. What is the mean of Solar.R in this subset?

```
> subset18<-subset(tall,Ozone>31 & Temp>90)
> mean(subset18[["Solar.R"]])
[1] 212.8
```

subset18[["Solar.R"]] is integer (vector)

subset18["Solar.R"] is data frame

subset18$Solar.R is integer (vector)

```
> subset18[["Solar.R"]]
 [1] 267 272 203 225 237 188 167 197 183 189
> class(subset18[["Solar.R"]])
[1] "integer"
> subset18["Solar.R"]
    Solar.R
69      267
70      272
120     203
121     225
122     237
123     188
124     167
125     197
126     183
127     189
> class(subset18["Solar.R"])
[1] "data.frame"
> subset18$Solar.R
 [1] 267 272 203 225 237 188 167 197 183 189
> class(subset18$Solar.R)
[1] "integer"
```


19.Question 19
What is the mean of "Temp" when "Month" is equal to 6? 

```
> subset19<-subset(tall,Month==6)
> mean(subset19$Temp)
[1] 79.1
```

20.Question 20
What was the maximum ozone value in the month of May (i.e. Month is equal to 5)?

```
> subset20<-subset(tall,Month==5)
> subOzone<-subset20$Ozone
> good<-complete.cases(subOzone)
> class(subOzone[good])
[1] "integer"
> max(subOzone[good])
[1] 115
```








## Week 2 Programming with R

functions and about controlling the flow

lexical scoping features of the language

Learning Objectives

Write an if-else expression

Write a for loop, a while loop, and a repeat loop

Define a function in R and specify its return value [see Functions Part 1 and Part 2]

Describe how R binds a value to a symbol via the search list

Define what lexical scoping is with respect to how the value of free variables are resolved in R

Describe the difference between lexical scoping and dynamic scoping rules

Convert a character string representing a date/time into an R datetime object. [see Dates and Times]



Assessments


Quiz 2 

Programming assignment 1: Air Pollution

[Tutorial](https://github.com/rdpeng/practice_assignment/blob/master/practice_assignment.rmd)


### Control Structures - Introduction


if and else: testing a condition and acting on it

for: execute a loop a fixed number of times

while: execute a loop while a condition is true

repeat: execute an infinite loop (must break out of it to stop)

break: break the execution of a loop

next: skip an interation of a loop





### Control Structures - If-else

```
if(<condition>) {
        ## do something
} 
## Continue with rest of code
```

```
if(<condition>) {
        ## do something
} 
else {
        ## do something else
}
```

```
if(<condition1>) {
        ## do something
} else if(<condition2>)  {
        ## do something different
} else {
        ## do something different
}
```

```
x <- runif(1, 0, 10)  
if(x > 3) {
        y <- 10
} else {
        y <- 0
}
```

```
y <- if(x > 3) {
        10
} else { 
        0
}
```

```
if(<condition1>) {

}

if(<condition2>) {

}
```



### Control Structures - For loops


```
> for(i in 1:10) {
+         print(i)
+ }
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
[1] 6
[1] 7
[1] 8
[1] 9
[1] 10
```

```
> x <- c("a", "b", "c", "d")
> 
> for(i in 1:4) {
+         ## Print out each element of 'x'
+         print(x[i])  
+ }
[1] "a"
[1] "b"
[1] "c"
[1] "d"
```

The seq_along() function is commonly used in conjunction with for loops in order to generate an integer sequence based on the length of an object (in this case, the object x).

```
> ## Generate a sequence based on length of 'x'
> for(i in seq_along(x)) {   
+         print(x[i])
+ }
[1] "a"
[1] "b"
[1] "c"
[1] "d"
```

It is not necessary to use an index-type variable.

```
> for(letter in x) {
+         print(letter)
+ }
[1] "a"
[1] "b"
[1] "c"
[1] "d"
```

For one line loops, the curly braces are not strictly necessary.

```
> for(i in 1:4) print(x[i])
[1] "a"
[1] "b"
[1] "c"
[1] "d"
```







### Control Structures - While loops

### Control Structures - Repeat, Next, Break

### Your First R Function

### Functions (part 1)

### Functions (part 2)

### Scoping Rules Symbol Binding

### Scoping Rules - R Scoping Rules

### Scoping Rules - Optimization Example (Optional)

### Coding Standards

### Dates and times

### Quiz

### Programming Assignment

