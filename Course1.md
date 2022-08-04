# [Coursera 1: The Data Scientist’s Toolbox](https://www.coursera.org/learn/data-scientists-tools/home/welcome)

- [Coursera 1: The Data Scientist’s Toolbox](#coursera-1-the-data-scientists-toolbox)
  - [Week 1  Data Science Fundamentals](#week-1--data-science-fundamentals)
    - [Welcome to the Data Scientist's Toolbox](#welcome-to-the-data-scientists-toolbox)
    - [What is data science](#what-is-data-science)
      - [Practice Quiz](#practice-quiz)
    - [What is data](#what-is-data)
      - [Practice Quiz](#practice-quiz-1)
    - [Getting help](#getting-help)
      - [Practice Quiz](#practice-quiz-2)
    - [The data science process](#the-data-science-process)
      - [Practice Quiz](#practice-quiz-3)
    - [Module 1 Quiz](#module-1-quiz)
  - [Week 2  R and RStudio](#week-2--r-and-rstudio)
    - [Installing R](#installing-r)
      - [Practice Quiz](#practice-quiz-4)
    - [Installing RStudio](#installing-rstudio)
      - [Practice Quiz](#practice-quiz-5)
    - [RStudio Tour](#rstudio-tour)
      - [Practice Quiz](#practice-quiz-6)
    - [R Packages](#r-packages)
      - [Practice Quiz](#practice-quiz-7)
    - [Projects in R](#projects-in-r)
      - [Practice Quiz](#practice-quiz-8)
    - [Module 2 Quiz](#module-2-quiz)
  - [Week 3 Version Control and Github](#week-3-version-control-and-github)
    - [Version Control](#version-control)
      - [Practice Quiz](#practice-quiz-9)
    - [Github and Git](#github-and-git)
      - [Practice Quiz](#practice-quiz-10)
    - [Linking Github and RStudio](#linking-github-and-rstudio)
      - [Pratice Quiz](#pratice-quiz)
    - [Projects Under Version Control](#projects-under-version-control)
      - [Practice Quiz](#practice-quiz-11)
    - [Module 3 Quiz](#module-3-quiz)
  - [Week 4 R Markdown, Scientific Thinking, and Big Data](#week-4-r-markdown-scientific-thinking-and-big-data)
    - [R Markdown](#r-markdown)
      - [Practice Quiz](#practice-quiz-12)
    - [Types of Data Science Questions](#types-of-data-science-questions)
      - [Practice Quiz](#practice-quiz-13)
    - [Experimental Design](#experimental-design)
      - [Practice Quiz](#practice-quiz-14)
    - [Big Data](#big-data)
      - [Practice Quiz](#practice-quiz-15)
    - [Module 4 Quiz](#module-4-quiz)
    - [Course Project](#course-project)


<!-- search for installed extension functions: cmd+shift+p -->
<!-- Markdown All in One: Create Table of Contents -->

## Week 1  Data Science Fundamentals
Learning Objectives
* Define data science
* Define data
* Use resources to get help with problems

### Welcome to the Data Scientist's Toolbox



### What is data science
volumn velocity variety

* Data science is using data to answer questions.

Data science can involve:
Statistics, computer science, mathematics
Data cleaning and formatting
Data visualization

* Data scientist is someone who use data to answer questions.

An Economist Special Report sums up this melange of skills well - they state that a data scientist is broadly defined as someone:
“who combines the skills of software programmer, statistician and storyteller slash artist to extract the nuggets of gold hidden under mountains of data”

#### Practice Quiz
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


### What is data
* Two definitions of data, one that focuses on the actions surrounding data, and another on what comprises data.

Information, especially facts or numbers, collected to be examined and considered and used to help decision-making. --Cambridge English Dictionary  
A set of values of qualitative or quantitative variables. --Wikipedia  
Set: In statistics, the population you are trying to discover something out.  
Variable: Measurements or characteristics of an item  
Qualitative variables: Measurements or information about qualities, described by words, not numbers, and they are not necessarily ordered  
Quantitative variables: Measurements or information about quantities or numerical items, described by numbers and are measured on a continuous, ordered scale

* The relationship between data and your question and emphasize the importance of question-first strategies. You could have all the data you could ever hope for, but if you don’t have a question to start, the data is useless.

#### Practice Quiz
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


### Getting help
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

#### Practice Quiz
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



### The data science process

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

#### Practice Quiz
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



### Module 1 Quiz

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




## Week 2  R and RStudio
Learning Objectives
* Complete the R installation process
* Complete the RStudio installation process
* Practice navigating in RStudio
* Give examples of R Packages

### Installing R

R is both a programming language and an environment, focused mainly on statistical analysis and graphics.

R is downloaded from the Comprehensive R Archive Network, or CRAN

Why should you use R?

1. Its popularity

2. Its cost

3. Its extensive functionality

4. Its community


#### Practice Quiz
1.Question 1

What does CRAN stand for?

Calculated R Activity Name

Citizens' R Application Network

Comprehensive R Archive Network &check;

2.Question 2

What does base R focus on?

Graphics &check;

Mapping

Analyzing text

3.Question 3

What is the output when you type into R: mean(mtcars$mpg) ?

20.09062 &check;

5.432

mean()

4.Question 4

Why are we using R for the course track?

R is a general purpose programming language.

R is one of the most widely used programming languages for Data Science. &check;

R is the best cloud computing language.


### Installing RStudio

RStudio is a graphical user interface for R



#### Practice Quiz
1.Question 1

What is RStudio?

A graphical user interface for R &check;

A programming language

An R package for machine learning

2.Question 2
Which is NOT an option for a file type when you go to File > New File in RStudio?

R Beamer Presentation &check;

R Markdown

Shiny Web App



### RStudio Tour

[cheatsheet of the RStudio environment](https://iqss.github.io/dss-workshops/R/Rintro/base-r-cheat-sheet.pdf)

#### Practice Quiz
1.Question 1

How do you see a command you have previously run and save it to source?

History tab > Highlight command > To Source &check;

Environment tab > Open folder > Save

File > History > Save

2.Question 2

What is the name of the quadrant in the bottom left corner of RStudio, in the default layout?

History

Plots

Console &check;

3.Question 3

Which of the following is NOT one of the options available under the Global Options menu in Tools?

Versions &check;

General

Sweave

4.Question 4

Using the Help menu, find out which of the following is one of the three species of Iris present in the base R dataset: iris.

Virginica &check;

Belladonna

Aurea


### R Packages

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

* How do you install packages?

Installing from CRAN

`install.packages("ggplot2")`

`install.packages(c("ggplot2", "devtools", "lme4"))`

OR 

Tools -> install packages

Installing from Bioconductor

source("https://bioconductor.org/biocLite.R")

call the package you want to install

`biocLite("GenomicFeatures")`

Installing from GitHub

check [this guide](http://kbroman.org/pkg_primer/pages/github.html)

`install.packages("devtools")`

`library(devtools)`

`install_github("author/package")`

* Loading packages

`library(ggplot2)`, OR Packages -> checkbox

There is an order to loading packages - some packages require other packages to be loaded first (dependencies). That package’s manual/help pages will help you out in finding that order, if they are picky.

* Checking what packages you have installed

Simply `installed.packages()` or `library()` is a way to check, OR Packages tab

* Updating packages (be careful )

check what packages need an update `old.packages()`, update all packages, use `update.packages()` 

only want to update a specific package, use `install.packages("packagename")`, OR Packages -> update

* Unloading packages

`detach("package:ggplot2", unload=TRUE)` OR uncheckbox in Packages

* Uninstalling packages

`remove.packages("ggplot2")`, OR clicking on the “X” in Packges

* Sidenote

`version` into the console to check the r version

`sessionInfo()` - it will tell you what version of R you are running along with a listing of all of the packages you have loaded.

Include this when post in forum

* Using the commands in a function

`help(package = "ggplot2")` and you will see all of the many functions that ggplot2 provides, OR access the help files through the Packages tab

* Extended help files

Once you know what function within a package you want to use, you simply call it in the console like any other function we’ve been using throughout this lesson. 

Once a package has been loaded, it is as if it were a part of the base R functionality.

“vignettes” are extended help files, including an overview of the package and its functions, and detailed examples of how to use the functions 

`browseVignettes("ggplot2")`

You should see that there are two included vignettes: “Extending ggplot2” and “Aesthetic specifications.” Exploring the Aesthetic specifications vignette is a great example of how vignettes can be helpful, clear instructions on how to use the included functions.

#### Practice Quiz
1.Question 1

How would you install the package ggplot2?

install.packages("ggplot2") &check;

library("ggplot2")

install.package("ggplot2")

2.Question 2

Using the help files, what is NOT a function included in the devtools package?

aes() &check;

check()

install_github()

3.Question 3

Which is NOT one of the main repositories?

RDocumentation &check;

GitHub

CRAN

4.Question 4

What command lists your R version, operating system, and loaded packages?

SESSIONINFO()

sessionInfo() &check;

session.Info()

5.Question 5

Install and load the KernSmooth R package. What does the copyright message say?

Copyright M. P. Wand 1997-2009 &check;

Copyright M. P. Wand 1990-2009

Copyright Matthew Wand 1997-2009




### Projects in R

File OR right top Project toolbar drop down

Open Project OR Open Projects in New Session

Close Project


#### Practice Quiz
1.Question 1
Which is NOT a way to create a new Project?

Session > New Project &check;

File > New Project

Project toolbar > New Project

2.Question 2

What file extension do Projects in R use?

.Rproj &check;

.pRoject

.R

3.Question 3

Creating a new project from scratch will NOT do which of the following?

Initiate version control &check;

Create a new folder

Open a blank RStudio window



### Module 2 Quiz
1.Question 1

What does base R focus on?

Mapping

Statistical analysis &check;

Artificial intelligence

2.Question 2

What is RStudio?

A graphical user interface for R &check;

Version control software

A programming language

3.Question 3

What is the name of the quadrant in the bottom left corner of RStudio, in the default layout?

History

Plots

Console &check;

4.Question 4

What command lists your R version, operating system, and loaded packages?

versions()

Sessioninfo()

sessionInfo() &check;

5.Question 5

What file extension do Projects in R use?

1 point

.Rproj &check;

.R

.RPROJECT



## Week 3 Version Control and Github
Learning Objectives
* Describe version control and its benefits
* Use Git and GitHub
* Complete the process of linking GitHub and RStudio
* Apply version control to projects

### Version Control

* What is version control?

Version control is a system that records changes that are made to a file or a set of files over time. As you make edits, the version control system takes snapshots of your files and the changes, and then saves those snapshots so you can refer or revert back to previous versions later if need be!

* What are the benefits of using version control?

It keeps a record of all changes made to the files. This can be of great help when you are collaborating with many people on the same files - the version control software keeps track of who, when, and why those specific changes were made. 

* What is Git? Why should you use it?

Git is a free and open source version control system. 

the ease with which RStudio and Git interface with each other

* *What is GitHub?

GitHub is an online interface for Git. Git is software used locally on your computer to record changes. GitHub is a host for your files and the records of the changes made.

* Version control vocabulary

* * Repository

Equivalent to the project’s folder/directory - all of your version controlled files (and the recorded changes) are located in a repository. Repositories are hosted on GitHub.

* * Commit

To commit is to save your edits and the changes made. A commit is like a snapshot of your files: Git compares the previous version of all of your files in the repo to the current version and identifies those that have changed since then. 

If you find a mistake, you revert your files to a previous commit. If you want to see what has changed in a file over time, you compare the commits and look at the messages to see why and who.

* * Push

Updating the repository with your edits. Pushing is sending those committed changes to that repository.

* * Pull

Updating your local version of the repository to the current version, pull to check if you are up to date with the main repository.

* * Staging

The act of preparing a file for a commit. Staging allows you to separate out file changes into separate commits.

* * Branch

you have created a branch where your edits are not shared with the main repository (yet) .
Following a branch point, the version history splits into two and tracks the independent changes made to both the original file in the repository that others may be editing, and tracking your changes on your branch, and then merges the files together.

* * Merge

Independent edits of the same file are incorporated into a single, unified file. Independent edits are identified by Git and are brought together into a single file, with both sets of edits incorporated. Git recognizes the disparity (conflict) and asks for user assistance in picking which edit to keep.

* * Conflict

When multiple people make changes to the same file and Git is unable to merge the edits. You are presented with the option to manually try and merge the edits or to keep one edit over the other.


* * Clone

Making a copy of an existing Git repository to get access to, and create a local version of all of the repository’s files and all of the tracked changes.


* * Fork

A personal copy of a repository that you have taken from another person. You can fork somebody's repository and then when you make changes, the edits are logged on your repository, not theirs.


* Best pratice

Purposeful, single issue commmits

informative commit messages

pull and push often

#### Practice Quiz

1.Question 1

I'm done editing a file, I need to ______ those changes then _______ them, and ______ it to the ________.

Commit, merge, push, repository

Pull, push, commit, branch

Stage, commit, push, repository &check;

2.Question 2

What is a good example of a message to accompany a commit?

Modified linear model of height to include new covariate, genotype &check;

Added genotype

Updated thing

3.Question 3

Which of these is NOT true about using a version control system?

Version control should only be used by experts &check;

Version control helps make sure that you do not lose work that you have done

Version control minimizes the need to save different versions of the same file on your computer



### Github and Git

[help files](https://help.github.com/)

Configuring Git

`git config --global user.name "username"`

`git config --global user.email "useremail signedup"`

Confirm

`git config --list`

#### Practice Quiz

1.Question 1

On each repository page in GitHub, in the top right hand corner there are three options. They are:

Commit, contributors, issues

Watch, star, fork &check;

Pull, clone, fork

2.Question 2

To make a new repository on GitHub, which can you NOT do?

Profile > New repository &check;

Plus sign > New repository

Profile > Repositories > New

3.Question 3

What command can you use to change the name associated with each of your commits?

git.config --global username "Jane Doe"

git config --local username "Jane Doe"

git config --global user.name "Jane Doe" &check;

4.Question 4

What command can you use to see your Git configuration?

git load --list

git config -settings

git config --list &check;

5.Question 5

Which of the following will initiate a git repository locally?

git init &check;

git remote add

git boom



### Linking Github and RStudio

* Linking RStudio and Git

In RStudio, go to Tools > Global Options > Git/SVN, Confirm that git.exe resides in the directory, OK or Apply

* Linking RStudio and GitHub

In that same window, Create RSA Key -> Close

View public key, copy the string of numbers and letters, Close

You have now created a key that is specific to you which we will provide to GitHub, so that it knows who you are when you commit a change from within RStudio.

In github account settings, SSH and GPG keys -> New SSH key -> Paste in the public key -> give it a Title related to RStudio -> Confirm add.

* Create a new repository and edit it in RStudio

Github Profile -> Repositories -> New -> Name and give a short description -> Create repository -> Copy URL

In RStudio, File -> New Project -> Version Control -> Git -> Paste in the repository URL -> select the location -> Create Project 

Doing so will initialize a new project, linked to the GitHub repository, and open a new session of RStudio.

File > New File > R Script

write some code and save, note default location is within the new Project directory

environment -> git -> staged checbox -> commit

new window open and details, write Commit message -> commit -> push


#### Pratice Quiz

1.Question 1

In what quadrant of RStudio will you find the Git tab ?

Environment &check;

Files

Viewer

2.Question 2
What is the order of commands to send a file to GitHub from within RStudio?

Commit > Stage > Push

Commit > Push

Stage > Commit message > Commit > Push &check;

3.Question 3

Which can you NOT do from within the Commit window of RStudio?

See the differences between your original file and your updated file

Stage files

Pull and push content from the repository

Write a commit message

None of the above &check;



### Projects Under Version Control

* Linking an existing Project with Git

In RStudio, File -> New Project -> New Directory -> New Project and name it.

Create Project (NOT Create a git repository, already existed and not under version control)

`cd ~/dir/name/of/path/to/file`

`git init`

`git add .`

initializes (init) this directory as a git repository and adds all of the files in the directory

`git commit -m "Initial commit`

Linking this project with GitHub

GitHub.com -> create a new repository

exact same name (Do NOT initialize a README file, .gitignore, or license.)

copy command below "Push an existing repository from the command line" and paste in terminal

* Working on an existing GitHub repository

in RStudio, File -> New Project -> Version Control -> Git -> provide the URL -> select location -> Create the project


#### Practice Quiz
1.Question 1

What do you call it when you create a local copy of a repository that 
you will work on collaboratively with the original repository owner?

Clone &check;

Branch

Merge

2.Question 2

What is the command to initialize git in a directory?

git init &check;

cd ~/dir/name/of/path/to/file

git add .

3.Question 3

How do you add all of the contents of a directory to version control?

git commit -m "Message"

cd ~/dir/name/of/path/to/file

git add . &check;

4.Question 4

How do you make a commit from within the command line?

cd ~/dir/name/of/path/to/file

git commit -m "Message"  &check;

git init




### Module 3 Quiz

1.Question 1

What is a good example of a message to accompany a commit?

Modified linear model of height to include new covariate, genotype &check;

Fixed problem with linear model

Updated thing

2.Question 2

On each repository page in GitHub, in the top right hand corner there are three options. They are:

Watch, star, fork &check;

Pull, clone, fork

Commit, contributors, issues

3.Question 3

Which of the following will initiate a git repository locally?

git init &check;

git remote add

git boom

4.Question 4

What is the order of commands to send a file to GitHub from within RStudio?

Commit > Push

Stage > Commit message > Commit > Push &check;

Pull > Push > Commit

5.Question 5

How do you add all of the contents of a directory to version control?

git add . &check;

cd ~/dir/name/of/path/to/file

git commit -m "Message"




## Week 4 R Markdown, Scientific Thinking, and Big Data

Learning Objectives
* Use R Markdown
* Propose data science questions
* Discuss experimental design and its importance for data science
* Summarize the qualities of big data


### R Markdown

* R Markdown is a way of creating fully reproducible documents, in which both text and code can be combined, can be rendered into HTML pages, or PDFs, or Word documents, or slides.

 reproducible -- share it and re-run the code and get the exact same answers

[A video on R Markdown](https://vimeo.com/178485416)

`install.packages("rmarkdown")`

File -> New File -> R Markdown

There is one of the huge benefits of R Markdown - rendering the results to code inline.

[R Markdown Introduction](https://rmarkdown.rstudio.com/lesson-1.html)

[R Markdown Basics](https://rmarkdown.rstudio.com/authoring_basics.html)

[R Markdown Cheatsheet](https://github.com/rstudio/cheatsheets/raw/main/rmarkdown-2.0.pdf)

[R Markdown Reference Guide](https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf?_ga=2.111473092.1190999278.1659485767-1996794053.1659127725)

[R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/)

[RStudio Cheatsheets](https://www.rstudio.com/resources/cheatsheets/)


* Code chunk

enclose the text between triple Backtick, the ```code chunk```, OR Cmd + Option + I , OR “Insert” button, that will also produce an empty code chunk

See the output of your code, select the line of code you want to run and use Ctrl+Enter or OR “Run” button, get output in your console window. 

Multiple lines of code in a chunk, run the entire chunk by using Ctrl+Shift+Enter, OR hitting the green arrow button on the right side of the chunk, OR going to the Run menu and selecting Run current chunk.


* Bulleted lists

single hyphen(dash), plus or asterisk. and a space before the text

`- text`, `* text`, `+ text`  



* Italicized and bold text

enclose the text between double asterisk 

`*text*`, *text*

`**text**`, **text**


* Knit: produce final document


#### Practice Quiz

1.Question 1

How would you strike through some text?

```\strikethrough\```

```~~strikethrough~~``` &check;

```--strikethrough--```

2.Question 2

What is the format for including a link that appears as blue text in your markdown document?

`![link.com](text that is shown)`

`(text that is shown)[link.com]`

`[text that is shown](link.com)` &check;

3.Question 3

How do you produce bold text?

`**bold**` &check;

`_bold_`

`~~bold~~`

4.Question 4
How do you produce italicized text?

`__some text__`

`**some text**`

`*some text*` &check;

5.Question 5

How do you produce your final document?

Knit &check;

Crochet

Macrame





### Types of Data Science Questions



The main divisions of data science questions

**1.Descriptive**

**2.Exploratory**

**3.Inferential**

**4.Predictive**

**5.Causal**

**6.Mechanistic**




1. Descriptive analysis

describe or **summarize** a set of data, common descriptive statistics: measures of central tendency (eg: mean, median, mode) or measures of variability (eg: range, standard deviations or variance).

2. Exploratory analysis

examine or **explore** the data and find **relationships** that weren’t previously known. however, Correlation does not imply causation

3. Inferential analysis

use a relatively **small sample** of data to **infer** or say something about the **population** at large. 

***Inferential analysis is commonly the goal of statistical modelling***

4. Predictive analysis

use **current** data to make **predictions** about **future** data

5. Causal analysis

see what happens to one variable when we manipulate another variable - looking at the **cause** and **effect** of a **relationship**.

6. Mechanistic analysis

understand the **exact changes in variables** that lead to **exact changes in other variables**.




#### Practice Quiz


1.Question 1

A study examining how modifying a group of adults' diet changes their cholesterol is an example of which kind of study?

Inferential

Causal &check;

Descriptive

2.Question 2

We collect data on all the songs in the Spotify catalogue and want to 
summarize how many are country western, hip-hop, classic rock, or other.
 What type of analysis is this?

Exploratory

Descriptive &check;

Predictive

3.Question 3
We collect data on a small sample of songs from the Spotify catalogue 
and want to figure out the relationship between the use of the word 
"truck" and whether a song is country western. What type of analysis is 
this?

Descriptive

Inferential &check;

Exploratory







### Experimental Design

* Experimental design is organizing an experiment so that you have the correct data (and enough of it!) to clearly and effectively answer your data science question. This process involves clearly formulating your question in advance of any data collection, designing the best set-up possible to gather the data to answer your question, identifying problems or sources of error in your design, and only then, collecting the appropriate data.



* Principles of experimental design






#### Practice Quiz

### Big Data



#### Practice Quiz

### Module 4 Quiz




### Course Project



