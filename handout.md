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
It is used to manage and describe:

 - Standard lifecycle for projects (compile, test, package, deploy)
 - Structuring projects (predefined file structure)
 - Definition and management of project dependencies
 - Version management of dependencies
 - Creation of projects from templates

Maven can scope dependencies to be included on:
 - Compilation
 - Runtime
 - Provided (only to compile, not on runtime. Example: Servlet API)
 - Test (dependency is only included for automated testing. Example: JUnit)

## Configuration file: pom.xml
The `pom.xml` is a **p**roject **o**bject **m**odel with xml format.

Example `pom.xml`
```xml
<project>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.mycompany.app</groupId>
  <artifactId>my-app</artifactId>
  <version>1</version>
  <dependencies>
    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-core</artifactId>
      <version>5.2.9.RELEASE</version>
      </dependency>
  </dependencies>
</project>
```

While the dependencies are probabely the most useful, but still optional feature of maven, the following properties are mandatory:
 - `groupId`  - package path of the project
 - `artifactId`  - name of your project
 - `version`  - a version your project.

Via the `pom.xml` it is also possible the specify arbitrary code repositories, custom plugins, project inheritance etc. Any details may be found in the official [introduction](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html).

## File structure
Maven embraces the convention over configuration principle. This incites to adhere to the following file structure:
```
src
    src/main
        src/main/java
        src/main/resources
    src/test
        src/test/java
target
    target/classes        
```

 - `src` - all source code
 - `src/main/java` - entrypoint for the applications source
 - `src/main/ressources` - other files that are needed at runtime
 - `src/test` - anything related to automated tests
 - `src/test/java` - the test sources (p.ex. JUnit classes)

## Quick start guide
* Get and install maven: [http://maven.apache.org](http://maven.apache.org/)
* `mvn validate` - check if configuration is valid and all necessary information is available
* `mvn compile` - does what is says :)
* `mvn test` - runs automated tests (if set up)
* `mvn package` - builds your `.jar`, `.war` or whatever you've configured
* `mvn deploy` - ships your package
* `mvn clean` - removes all (intermediate) build files


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
