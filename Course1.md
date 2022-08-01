## [Coursera 1: The Data Scientist’s Toolbox](https://www.coursera.org/learn/data-scientists-tools/home/welcome)

### Week 1  Data Science Fundamentals
Learning Objectives
* Define data science
* Define data
* Use resources to get help with problems

#### Welcome to the Data Scientist's Toolbox



#### What is data science
volumn velocity variety

* Data science is using data to answer questions.

Data science can involve:
Statistics, computer science, mathematics
Data cleaning and formatting
Data visualization

* Data scientist is someone who use data to answer questions.

An Economist Special Report sums up this melange of skills well - they state that a data scientist is broadly defined as someone:
“who combines the skills of software programmer, statistician and storyteller slash artist to extract the nuggets of gold hidden under mountains of data”

##### Practice Quiz
1.Question 1

Which of the following is an example of structured data?

Lung x-ray images of smokers

A database of individual's addresses, phone numbers, and post codes &check;

A compilation of cat videos

2.Question 2
Which is NOT one of the three V's of Big Data?

variety, vast, visible

vexing, velocity, variety

vibrant, vital, visible &check;

3.Question 3

Which of these is NOT one of the main skills embodied by data scientists?

Machine learning &check;

Hacking skills

Math and stats


#### What is data
* Two definitions of data, one that focuses on the actions surrounding data, and another on what comprises data.

Information, especially facts or numbers, collected to be examined and considered and used to help decision-making. --Cambridge English Dictionary  
A set of values of qualitative or quantitative variables. --Wikipedia  
Set: In statistics, the population you are trying to discover something out.  
Variable: Measurements or characteristics of an item  
Qualitative variables: Measurements or information about qualities, described by words, not numbers, and they are not necessarily ordered  
Quantitative variables: Measurements or information about quantities or numerical items, described by numbers and are measured on a continuous, ordered scale

* The relationship between data and your question and emphasize the importance of question-first strategies. You could have all the data you could ever hope for, but if you don’t have a question to start, the data is useless.

##### Practice Quiz
1.Question 1
Which of these is an example of a quantitative variable?

clothing brand, genre, birthplace

occupation, height, gender

age, weight, height &check;

2.Question 2

Quantitative variables are measured on ordered, continuous scales.

True &check;

False

3.Question 3

What is the most important thing in Data Science?

Statistical inference

Using the right software

The question you are trying to answer &check;


#### Getting help
* forums

https://stackoverflow.com/  
https://stats.stackexchange.com/  
https://www.coursera.org/learn/data-scientists-tools/discussions

tutorials, FAQs, or vignettes of whatever command or program is giving you trouble.

Check for typos!  
Read the error message and make sure you understand it  
Google the error message, exactly

The quickest way to figuring out what went wrong is looking at the output you did get, comparing it to what you wanted, and thinking about how the program may have produced that output instead of what you wanted.

* How to effectively ask questions on forums

Details to include:  
The question you are trying to answer  
How you approached the problem, what steps you have already taken to answer the question  
What steps will reproduce the problem (including sample data for troubleshooters to work from!)  
What was the expected output  
What you saw instead (including any error messages you received!)  
What troubleshooting steps you have already tried  
Details about your set-up, eg: what operating system you are using, what version of the product you have installed (eg: R, Rpackages)  
Be specific in the title of your questions!

Better:  
R 3.4.3 lm() function produces seg fault with large data frame (Windows 10)  
Applied PCA to a matrix - what are U, D, and Vt?

Even better:  
R 3.4.3 lm() function on Windows 10 – seg fault on large dataframe  
Using principle components to discover common variation in rows of a matrix, should I use, U, D or Vt?

##### Practice Quiz
1.Question 1

Which of these might be a good title for a forum post?

How do I get rnorm() to work?

STAT101 quiz

Removing rows with NAs in data.frame using subset(), R 3.4.3 &check;

2.Question 2

Which is a characteristic of a good question when posting to message boards?

Assumes that you've discovered a bug in R

Includes follow-ups if you answer your own question &check;

Asks for a code fix without explanation

3.Question 3

Which is NOT a good strategy for finding the answer to a problem in this course?

Searching the course forum

Emailing the professor &check;

Explaining your problem to a friend/coworker



#### The data science process

* The Question

have your question well-defined

* The Data

* Data Analysis

it is important to know that after getting the data together, the next step is figuring out what you need to do with that data in order to answer your question.

* Exploratory Data Analysis

Figuring out how to do what you want to do to answer your question of interest is part of the process

* Data Analysis Results

It’s always good to consider whether or not the results were what you were expecting, from any analysis!
figure out what was specifically going on

* Communication

it was time to share it with the world. An important part of any data science project is effectively communicating the results of the project.
writing a wonderful blog post that communicated the results of your analysis, answered the question you set out to answer, and did so in an entertaining way.

You have to form your question, get data, explore and analyse your data, and communicate your results. 

##### Practice Quiz
1.Question 1

Which of these is NOT an effective way to communicate the findings of your analysis?

Save code locally on your computer &check;

Presentation at a conference

Write a scientific article

2.Question 2

What's the first step in the data science process?

Modeling the data

Getting the data

Generating the question &check;

3.Question 3

Why should you include links or citations to others' work?

It helps other quickly find information you've reference. &check;

Others' work is more important than your.

Citations prove how relevant your work is.

4.Question 4

What does Hilary Parker suggest led to the popularity of the name "Dewey" in the late 1800s? (You may have to reference Hilary's blog post  for this question.

People named their daughters after Dewey, the famous opera singer.

People named their daughters after Farrah Dewey, after Charlie's Angels.

People named their daughters after George Dewey, after the Spanish-American War. &check;



#### Module 1 Quiz

1.Question 1
Which of these is NOT one of the main skills embodied by data scientists?

Hacking skills

Machine learning &check;

Math and stats

2.Question 2

What is the most important thing in Data Science?

The question you are trying to answer &check;

Statistical inference

Working with large data sets

3.Question 3

Which of these might be a good title for a forum post?

URGENT! R isn't working!

Removing rows with NAs in data.frame using subset(), R 3.4.3 &check;

How do I get rnorm() to work?

4.Question 4

What's the first step in the data science process? 

Communicate your findings

Exploring the data

Generating the question &check;

5.Question 5

Which of these is an example of a quantitative variable?

Latitude &check;

Occupation

Educational level




### Week 2  R and R Studio

#### Installing R

R is both a programming language and an environment, focused mainly on statistical analysis and graphics.

R is downloaded from the Comprehensive R Archive Network, or CRAN

Why should you use R?

1. Its popularity

2. Its cost

3. Its extensive functionality

4. Its community

#### Installing RStudio

RStudio is a graphical user interface for R

#### RStudio Tour

[cheatsheet of the RStudio environment](https://iqss.github.io/dss-workshops/R/Rintro/base-r-cheat-sheet.pdf)

#### R Packages

To expand upon R’s basic functionality, people have developed packages. A package is a collection of functions, data, and code 

A library is the place where the package is located on your computer. To think of an analogy, a library is, well, a library… and a package is a book within the library. The library is where the books/packages are located.

* What are repositories?

A repository is a central location where many developed packages are located and available for download.
There are three big repositories:
1. [CRAN (Comprehensive R Archive Network)](https://cran.r-project.org/web/packages/): R’s main repository (>12,100 packages available!)
2. [BioConductor](https://bioconductor.org/packages/release/BiocViews.html#___Software): A repository mainly for bioinformatic-focused packages
3. GitHub: A very popular, open source repository (not R specific!)

* How do you know what package is right for you?

CRAN groups all of its packages by their functionality/topic into 35 “themes.

[Task View](https://cran.r-project.org/web/views/): 

How do you install packages?

Installing from CRAN

'install.packages("ggplot2")'

'install.packages(c("ggplot2", "devtools", "lme4"))'

OR 

Tools -> install packages

Installing from Bioconductor

source("https://bioconductor.org/biocLite.R")

call the package you want to install

'biocLite("GenomicFeatures")'

Installing from GitHub

check [this guide](http://kbroman.org/pkg_primer/pages/github.html)

'install.packages("devtools")'

'library(devtools)'

'install_github("author/package")'
