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
    - [Summary](#summary)
    - [Your First R Function](#your-first-r-function)
    - [Functions (part 1)](#functions-part-1)
    - [Functions (part 2)](#functions-part-2)
    - [Scoping Rules - Symbol Binding](#scoping-rules---symbol-binding)
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



### Quiz

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
     print(i)
}
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

* seq_along()

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

* It is not necessary to use an index-type variable.

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

* Nested for loops

```
x <- matrix(1:6, 2, 3)

for(i in seq_len(nrow(x))) {
        for(j in seq_len(ncol(x))) {
                print(x[i, j])
        }   
}
```

Sometimes it can go around loops by using functions.



### Control Structures - While loops


While loops begin by testing a condition. If it is true, then they execute the loop body. Once the loop body is executed, the condition is tested again, and so forth, until the condition is false, after which the loop exits.

```
> count <- 0
> while(count < 10) {
+         print(count)
+         count <- count + 1
+ }
```

Sometimes there will be more than one condition in the test.

Conditions are always evaluated from left to right.

```
> z <- 5
> set.seed(1)
> 
> while(z >= 3 && z <= 10) {
+         coin <- rbinom(1, 1, 0.5)
+         
+         if(coin == 1) {  ## random walk
+                 z <- z + 1
+         } else {
+                 z <- z - 1
+         } 
+ }
> print(z)
[1] 2
```


### Control Structures - Repeat, Next, Break

* repeat Loops

repeat initiates an infinite loop right from the start. These are not commonly used in statistical or data analysis applications but they do have their uses. The only way to exit a repeat loop is to call break.

```
x0 <- 1
tol <- 1e-8

repeat {
        x1 <- computeEstimate()
        
        if(abs(x1 - x0) < tol) {  ## Close enough?
                break
        } else {
                x0 <- x1
        } 
}
```

* next, return

next is used to skip an iteration of a loop.

```
for(i in 1:100) {
        if(i <= 20) {
                ## Skip the first 20 iterations
                next                 
        }
        ## Do something here
}
```

break is used to exit a loop immediately, regardless of what iteration the loop may be on.

```
for(i in 1:100) {
      print(i)

      if(i > 20) {
              ## Stop loop after 20 iterations
              break  
      }		
}
```


### Summary

* Control structures like if, while, and for allow you to control the flow of an R program

* Infinite loops should generally be avoided, even if (you believe) they are theoretically correct.

* Control structures mentioned here are primarily useful for writing programs; for command-line interactive work, the “apply” functions are more useful.




### Your First R Function


```
above<-function(x,n){
  use <- x > n
  x[use]
}
```

```
> x<-1:20
> above(x,15)
[1] 16 17 18 19 20
```

```
> class(x[TRUE])
[1] "integer"
> class(x[FALSE])
[1] "integer"
> x[TRUE]
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
> x[FALSE]
integer(0)
```

* default above<-function(x,n=10)



### Functions (part 1)

Functions are defined using the function() directive and are stored as R objects just like anything else. In particular, they are R objects of class “function”.

```
f<-function(<arguments>){
     ##do something interesting
}
```

* Functions in R are first class objects, which means that they can be treated much like any other R object. Importantly, 

* Functions can be passed as arguments to other functions 
* Functions can be nested, so that you can define a function inside of another function 
* **The return value of a function is the last expression in the function body to be evaluated**



* Function Arguments

Functions have named arguments which potentially have default values

* The formal arguments are the arguments included in the function definition

* The formals function returns a list of all the formal arguments of a function

* Not every function call in R make use of all the formal arguments

* Function arguments can be missing or might have default values



* Argument Matching

R functions arguments can be matched positionally or by name

```
> str(rnorm)
function (n, mean = 0, sd = 1)  
> mydata <- rnorm(100, 2, 1)              ## Generate some data
> ## Positional match first argument, default for 'na.rm'
> sd(mydata)                     
[1] 0.9328666
> ## Specify 'x' argument by name, default for 'na.rm'
> sd(x = mydata)                 
[1] 0.9328666
> ## Specify both arguments by name
> sd(x = mydata, na.rm = FALSE)  
[1] 0.9328666
> ## Specify both arguments by name
> sd(na.rm = FALSE, x = mydata)     
[1] 0.9328666
> sd(na.rm = FALSE, mydata)
[1] 0.9328666
```

standard deviation `sd()` has two arguments: x indicates the vector of numbers and na.rm is a logical indicating whether missing values should be removed or not.

Even though it is legal, I dont recommend missing around with the order of the arguments too much, since it can lead to some confusion.

You can mix positional matching with matching by name. When an argument is matched by name, it is “taken out” of the argument list and the remaining unnamed arguments are matched in the order that they are listed in the function definition.

```
> args(lm)
function (formula, data, subset, weights, na.action, method = "qr", 
    model = TRUE, x = FALSE, y = FALSE, qr = TRUE, singular.ok = TRUE, 
    contrasts = NULL, offset, ...) 
NULL
```

The following two calls are equivalent.

```
lm(data = mydata, y ~ x, model = FALSE, 1:100)
lm(y ~ x, mydata, 1:100, model = FALSE)
```

Most of the time, named arguments are useful on the command line when you have a long argument list and you want to use the defaults for everything except for an argument near the end of the list. 

Named arguments also help if you can remember the name of the argument and not its position on the argument list. 

For example, plotting functions often have a lot of options to allow for customization, but this makes it difficult to remember exactly the position of every argument on the argument list.


Function arguments can also be partially matched, which is useful for interactive work. 

The order of operations when given an argument is

* Check for exact match for a named argument

* Check for a partial match

* Check for a positional match




### Functions (part 2)

In addition to not specifying a default value, you can also set an argument value to NULL.

```
f <- function(a, b = 1, c = 2, d = NULL) {

}
```

You can check to see whether an R object is NULL with the is.null() function. 


* Lazy Evaluation
Arguments to functions are evaluated lazily, so they are evaluated only as needed in the body of the function.

```
> f <- function(a, b) {
+         a^2
+ } 
> f(2)
[1] 4
```

This function never actually uses the argument b, so calling f(2) will not produce an error because the 2 gets positionally matched to a. 

```
> f <- function(a, b) {
+         print(a)
+         print(b)
+ }
> f(45)
[1] 45
```

Error in print(b): argument "b" is missing, with no default
Notice that “45” got printed first before the error was triggered. This is because b did not have to be evaluated until after print(a). Once the function tried to evaluate print(b) the function had to throw an error.


* The ...argument

The ... argument indicates a variable number of arguments that are usually passed on to other functions. 

The ... argument is often used when extending another function and you don’t want to copy the entire argument list of the original function

```
myplot <- function(x, y, type = "l", ...) {
        plot(x, y, type = type, ...)         ## Pass '...' to 'plot' function
}
```

Generic functions use ... so that extra arguments can be passed to methods.

```
> mean
function (x, ...) 
UseMethod("mean")
```

The ... argument is necessary when the number of arguments passed to the function cannot be known in advance. This is clear in functions like paste() and cat().


The ... argument is necessary when the number of arguments passed to the function cannot be known in advance. This is clear in functions like paste() and cat().

```
> args(paste)
function (..., sep = " ", collapse = NULL, recycle0 = FALSE) 
NULL
> args(cat)
function (..., file = "", sep = " ", fill = FALSE, labels = NULL, 
    append = FALSE) 
NULL
```



One catch with ... is that any arguments that appear after ... on the argument list must be named explicitly and cannot be partially matched

```
> args(paste)
function (..., sep = " ", collapse = NULL, recycle0 = FALSE) 
NULL

> paste("a", "b", sep = ":")
[1] "a:b"

> paste("a", "b", se = ":")
[1] "a b :"
```




### Scoping Rules - Symbol Binding

* A Diversion on Binding Values to Symbol

How does R know which value to assign to which symbol? When I type

```
> lm <- function(x) { x * x }
> lm
function(x) { x * x }
```

how does R know what value to assign to the symbol lm? Why doesn’t it give it the value of lm that is in the stats package?

When R tries to bind a value to a symbol, it searches through a series of environments to find the appropriate value. When you are working on the command line and need to retrieve the value of an R object, the order in which things occur is roughly

Search the global environment (i.e. your workspace) for a symbol name matching the one requested.
Search the namespaces of each of the packages on the search list
The search list can be found by using the search() function.

```
> search()
[1] ".GlobalEnv"        "package:stats"     "package:graphics" 
[4] "package:grDevices" "package:utils"     "package:datasets" 
[7] "package:methods"   "Autoloads"         "package:base"    
```

* Bring values to symbol

The global environment or the user’s workspace is always the first element of the search list and the base package is always the last.

The order of the packages on the search list matters

Users can configure which packages get loaded on startup so if you are writing a function (or a package), you cannot assume that there will be a set list of packages available in a given order.

When a user loads a package with library() the namespace of that package gets put in position 2 of the search list (by default) and everything else gets shifted down the list.

Note that R has separate namespaces for functions and non-functions so it’s possible to have an object named c and a function named c().

* Scoping rules

The scoping rules for R are the main feature that make it different from the original S language

The scoping rules of a language determine how a value is associated with a free variable in a function. 

R uses **lexical scoping** or static scoping. An alternative to lexical scoping is dynamic scoping which is implemented by some languages.

Lexical scoping turns out to be particularly useful for simplifying statistical computations


* lexical scoping

Consider the following function.

```
> f <- function(x, y) {
+         x^2 + y / z
+ }
```

This function has 2 formal arguments x and y. In the body of the function there is another symbol z. In this case z is called a free variable.

The scoping rules of a language determine how values are assigned to free variables. 

Free variables are not formal arguments and are not local variables (assigned insided the function body).



Lexical scoping in R means that

**The values of free variables are searched for in the environment in which the function was defined.**


**what is an environment?**

* An environment is a collection of (symbol, value) pairs, i.e. x is a symbol and 3.14 might be its value. 

* Every environment has a parent environment and it is possible for an environment to have multiple “children”. 

* The only environment without a parent is the empty environment.

* A function and an environment make up what is called a closure or function closure.



**Search process** that occurs that goes as follows:

* If the value of a symbol is not found in the environment in which a function was defined, then the search is continued in the parent environment.

* The search continues down the sequence of parent environments until we hit the top-level environment; this usually the global environment (workspace) or the namespace of a package.

* After the top-level environment, the search continues down the search list until we hit the empty environment.

* If a value for a given symbol cannot be found once the empty environment is arrived at, then an error is thrown.







### Scoping Rules - R Scoping Rules

* Why Does It Matter?

Typically, a function is defined in the global environment, so that the values of free variables are just found in the user’s workspace. 

This behavior is logical for most people and is usually the “right thing” to do. 

However, in R you can have functions defined inside other functions (languages like C don’t let you do this). 

Now things get interesting — in this case the environment in which a function is defined is the body of another function!

```
> make.power <- function(n) {
+         pow <- function(x) {
+                 x^n 
+         }
+         pow 
+ }
```

* The make.power() function is a kind of “constructor function” that can be used to construct other functions.

```
> cube <- make.power(3)
> square <- make.power(2)
> cube(3)
[1] 27
> square(3)
[1] 9
```

* Exploring a function closure

What's in a function's environment

```
> ls(environment(cube))
[1] "n"   "pow"
> get("n", environment(cube))
[1] 3
```

We can also take a look at the square() function.

```
> ls(environment(square))
[1] "n"   "pow"
> get("n", environment(square))
[1] 2
```


* Lexical VS Dynamic Scoping

```
> y <- 10
> 
> f <- function(x) {
+         y <- 2
+         y^2 + g(x)
+ }
> 
> g <- function(x) { 
+         x*y
+ }
What is the value of the following expression?

f(3)
```

When a function is defined in the global environment and is subsequently called from the global environment, then the defining environment and the calling environment are the same. This can sometimes give the appearance of dynamic scoping.

```
> g <- function(x) { 
+         a <- 3
+         x+a+y   
+         ## 'y' is a free variable
+ }
> g(2)
Error in g(2): object 'y' not found
> y <- 3
> g(2)
[1] 8
```

* Consequences of Lexical Scoping

All objects must be stored in memory in R

All functions must carry a pointer to their respective defining environments, which could be anywhere. 

In the S language (R’s close cousin), free variables are always looked up in the global workspace, so everything can be stored on the disk because the “defining environment” of all functions is the same.



### Scoping Rules - Optimization Example (Optional)

* Application: Optimization

Why is any of this information about lexical scoping useful?

Optimization routines in R like optim(), nlm(), and optimize() require you to pass a function whose argument is a vector of parameters (e.g. a log-likelihood, or a cost function)

However, an objective function that needs to be minimized might depend on a host of other things besides its parameters (like data). 

When writing software which does optimization, it may also be desirable to allow the user to hold certain parameters fixed.


* Maximizing a Normal Likelihood

Here is an example of a “constructor” function

It creates a negative log-likelihood function that can be minimized to find maximum likelihood estimates in a statistical model.

```
> make.NegLogLik <- function(data, fixed = c(FALSE, FALSE)) {
+         params <- fixed
+         function(p) {
+                 params[!fixed] <- p
+                 mu <- params[1]
+                 sigma <- params[2]
+                 
+                 ## Calculate the Normal density
+                 a <- -0.5*length(data)*log(2*pi*sigma^2)
+                 b <- -0.5*sum((data-mu)^2) / (sigma^2)
+                 -(a + b)
+         } 
+ }
```

Note: Optimization functions in R minimize functions, so you need to use the negative log-likelihood.

```
> set.seed(1)
> normals <- rnorm(100, 1, 2)
> nLL <- make.NegLogLik(normals)
> nLL
function(p) {
                params[!fixed] <- p
                mu <- params[1]
                sigma <- params[2]
                
                ## Calculate the Normal density
                a <- -0.5*length(data)*log(2*pi*sigma^2)
                b <- -0.5*sum((data-mu)^2) / (sigma^2)
                -(a + b)
        }
<bytecode: 0x7fcb87ef9120>
<environment: 0x7fcba1ec4668>
> 
> ## What's in the function environment?
> ls(environment(nLL))   
[1] "data"   "fixed"  "params"
```


* Estimate Parameters


Now that we have our nLL() function, we can try to minimize it with optim() to estimate the parameters.

```
> optim(c(mu = 0, sigma = 1), nLL)$par
      mu    sigma 
1.218239 1.787343 
```

You can see that the algorithm converged and obtained an estimate of mu and sigma.

We can also try to estimate one parameter while holding another parameter fixed. Here we fix sigma to be equal to 2.

```
> nLL <- make.NegLogLik(normals, c(FALSE, 2))
> optimize(nLL, c(-1, 3))$minimum
[1] 1.217775
```

Because we now have a one-dimensional problem, we can use the simpler optimize() function rather than optim().

We can also try to estimate sigma while holding mu fixed at 1.

```
> nLL <- make.NegLogLik(normals, c(1, FALSE))
> optimize(nLL, c(1e-6, 10))$minimum
[1] 1.800596
```

* Plotting the Likelihood

Another nice feature that you can take advantage of is plotting the negative log-likelihood to see how peaked or flat it is.

Here is the function when mu is fixed.

```
> ## Fix 'mu' to be equalt o 1
> nLL <- make.NegLogLik(normals, c(1, FALSE))  
> x <- seq(1.7, 1.9, len = 100)
> 
> ## Evaluate 'nLL()' at every point in 'x'
> y <- sapply(x, nLL)    
> plot(x, exp(-(y - min(y))), type = "l")
```

Here is the function when sigma is fixed.

```
> ## Fix 'sigma' to be equal to 2
> nLL <- make.NegLogLik(normals, c(FALSE, 2))
> x <- seq(0.5, 1.5, len = 100)
> ## Evaluate 'nLL()' at every point in 'x'
> y <- sapply(x, nLL)     
> plot(x, exp(-(y - min(y))), type = "l")
```


* Lexical Scoping Summary

Objective functions can be “built” which contain all of the necessary data for evaluating the function

No need to carry around long argument lists — useful for interactive and exploratory work.

Code can be simplified and cleaned up

Reference: Robert Gentleman and Ross Ihaka (2000). “Lexical Scope and Statistical Computing,” JCGS, 9, 491–508.


### Coding Standards

1. text editor/ text files
2. indent your code
3. limit the width of your code (80 columns)
4. Limit the length of individual functions.




### Dates and times

Times in R

R has developed a special representation for dates and times. 

1. Dates are represented by the Date classT
2. imes are represented by the POSIXct or the POSIXlt class. 
3. Dates are stored internally as the number of days since 1970-01-01
4. Times are stored internally as the number of seconds since 1970-01-01.

Dates are represented by the Date class and can be coerced from a character string using the as.Date() function. 

```
> ## Coerce a 'Date' object from character
> x <- as.Date("1970-01-01")   
> x
[1] "1970-01-01"
```

* Times are represented by the POSIXct or the POSIXlt class. 

1. POSIXct is just a very large integer under the hood. It use a useful class when you want to store times in something like a data frame. 
2. POSIXlt is a list underneath and it stores a bunch of other useful information like the day of the week, day of the year, month, day of the month. This is useful when you need that kind of information.

* There are a number of generic functions that work on dates and times to help you extract pieces of dates and/or times.

1. weekdays: give the day of the week
2. months: give the month name
3. quarters: give the quarter number (“Q1”, “Q2”, “Q3”, or “Q4”)


* Times can be coerced from a character string using the as.POSIXlt or as.POSIXct function.

```
> x <- Sys.time()
> x
[1] "2022-05-31 09:18:49 EDT"
> class(x)   ## 'POSIXct' object
[1] "POSIXct" "POSIXt" 
```

The POSIXlt object contains some useful metadata.

```
> p <- as.POSIXlt(x)
> names(unclass(p))
 [1] "sec"    "min"    "hour"   "mday"   "mon"    "year"   "wday"   "yday"  
 [9] "isdst"  "zone"   "gmtoff"
> p$wday     ## day of the week
[1] 2
```

You can also use the POSIXct format.

```
> x <- Sys.time()
> x             ## Already in ‘POSIXct’ format
[1] "2022-05-31 09:18:49 EDT"
> unclass(x)    ## Internal representation
[1] 1654003130
> x$sec         ## Can't do this with 'POSIXct'!
Error in x$sec: $ operator is invalid for atomic vectors
> p <- as.POSIXlt(x)
> p$sec         ## That's better
[1] 49.77399
```

Finally, there is the strptime() function in case your dates are written in a different format. 

```
> datestring <- c("January 10, 2012 10:40", "December 9, 2011 9:10")
> x <- strptime(datestring, "%B %d, %Y %H:%M")
> x
[1] "2012-01-10 10:40:00 EST" "2011-12-09 09:10:00 EST"
> class(x)
[1] "POSIXlt" "POSIXt" 
```

Check strptime for details on formatting strings.


* Operations on Dates and Times

You can use mathematical operations on dates and times. Well, really just + and -. You can do comparisons too (i.e. ==, <=)

```
> x <- as.Date("2012-01-01")
> y <- strptime("9 Jan 2011 11:34:21", "%d %b %Y %H:%M:%S") 
> x-y
Warning: Incompatible methods ("-.Date", "-.POSIXt") for "-"
Error in x - y: non-numeric argument to binary operator
> x <- as.POSIXlt(x) 
> x-y
Time difference of 356.3095 days
```

keep track of all the annoying things about dates and times, like leap years, leap seconds, daylight savings, and time zones.

```
> x <- as.Date("2012-03-01") 
> y <- as.Date("2012-02-28") 
> x-y
Time difference of 2 days
```

Here’s an example where two different time zones are in play (unless you live in GMT timezone, in which case they will be the same!).

```
> ## My local time zone
> x <- as.POSIXct("2012-10-25 01:00:00")     
> y <- as.POSIXct("2012-10-25 06:00:00", tz = "GMT") 
> y-x
Time difference of 1 hours
```

* Summary

Dates and times have special classes in R that allow for numerical and statistical calculations

Dates use the Date class

Times use the POSIXct and POSIXlt class

Character strings can be coerced to Date/Time classes using the strptime function or the as.Date, as.POSIXlt, or as.POSIXct



### Quiz


1.Question 1

Suppose I define the following function in R

```
cube <- function(x, n) {
        x^3
}
```

What is the result of running

`cube(3)`

in R after defining this function?

An error is returned because 'n' is not specified in the call to 'cube'

A warning is given with no value returned.

The number 27 is returned &check;

The users is prompted to specify the value of 'n'.


2.Question 2

The following code will produce a warning in R.

```
x <- 1:10
if(x > 5) {
        x <- 0
}
```

Why?

The syntax of this R expression is incorrect.

'x' is a vector of length 10 and 'if' can only test a single logical statement. &check;

The expression uses curly braces.

You cannot set 'x' to be 0 because 'x' is a vector and 0 is a scalar.

There are no elements in 'x' that are greater than 5


3.Question 3

Consider the following function

```
f <- function(x) {
        g <- function(y) {
                y + z
        }
        z <- 4
        x + g(x)
}
```

If I then run in R

```
z <- 10
f(3)
```

What value is returned?

`10`


4.Question 4

Consider the following expression:

```
x <- 5
y <- if(x < 3) {
        NA
} else {
        10
}
```

What is the value of 'y' after evaluating this expression?

`10`

5.Question 5

Consider the following R function

```
h <- function(x, y = NULL, d = 3L) {
        z <- cbind(x, d)
        if(!is.null(y))
                z <- z + y
        else
                z <- z + f
        g <- x + y / z
        if(d == 3L)
                return(g)
        g <- g + 10
        g
}
```

Which symbol in the above function is a free variable?

`f`

6.Question 6

What is an environment in R?

a collection of symbol/value pairs &check;

a list whose elements are all functions

an R package that only contains data

a special type of function


7.Question 7

The R language uses what type of scoping rule for resolving free variables?

dynamic scoping

compilation scoping

global scoping

lexical scoping &check;


8.Question 8

How are free variables in R functions resolved?

The values of free variables are searched for in the environment in which the function was defined &check;

The values of free variables are searched for in the global environment

The values of free variables are searched for in the environment in which the function was called

The values of free variables are searched for in the working directory



9.Question 9

What is one of the consequences of the scoping rules used in R?

Functions cannot be nested

All objects must be stored in memory &check;

All objects can be stored on the disk

R objects cannot be larger than 100 MB


10.Question 10

In R, what is the parent frame?

It is the package search list

It is always the global environment

It is the environment in which a function was called

It is the environment in which a function was defined &check;





### Programming Assignment

