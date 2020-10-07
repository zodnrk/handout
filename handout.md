---
title: Maven & Git
titlepage: false
lot: false
toc: false
fontsize: 10pt
classoption:
- twocolumn
...

# Maven
## Build tool
Maven is a powerful build tool for java projects.
It is used to manage and describes Java Projects:

 

 - Standard-Lifecycle for projects
 - Structure of projects
 - Definition and management of project dependencies
 - Creation of projects from templates
 - Versioning

 

To get and install maven:
[http://maven.apache.org](http://maven.apache.org/)

 

-   GroupId  - a package of a new project.
-   ArtifactId  - a name of your project.
-   Version  - a version of a new project. By default, this field is specified automatically.

 

Maven can be used for:
 - Compile
 - Runtime
 - Provided (only to compile, not on runtime. It is used as example from Servlet API)
 - Test (JUnit tests to check the code every built time)

 

#### configuration file: pom.xml
pom.xml is a **p**roject **o**bject **m**odel with xml format.

 

#### Java structure

 

    src
        src/main
            src/main/java
            src/main/resources
        src/test
            src/test/java
    target
        target/classes        

 

 - src = all insert files
 - main =  main directory
 - main/java = Java source code
 - main/ressources = other files that are needed at runtime
 - test = files for automated test runs
 - test/java = JUnit Classes

 

#### Quick start guide


# Git
## Further Reading
For further reading about git,
I recommend the book _Pro Git_.
It's free, and can be found on [the Git website](https://git-scm.com/book/en/v2).
If you're looking for something in video form,
[Lecture 6 of _The Missing Semester_](https://missing.csail.mit.edu/2020/version-control/)
is also quite good.

## History
Git is an open source version control system (VCS),
which was developed by Linus Torvalds in 2005
because the current VCS used for Linux Kernel development
was no longer sufficient.
^[[git-scm.com A short history](https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git)]
Some of the goals for Git were:

* Speed
* Simple design
* Support for parallel development
* Fully distributed
* Efficiently handle large projects

## Quick Start Guide

## Version Control

## Branching Model

## Collaboration

## Data Model

## Tooling

\newpage
![](img/xkcd_1597.png)

^[Image Credit: [xkcd.com/1597](https://xkcd.com/1597/)]
