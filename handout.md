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

 - Standard life cycle for projects (compile, test, package, deploy)
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

While the dependencies are probably the most useful, but still optional feature of maven, the following properties are mandatory:
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
        src/main/ressources
    src/test
        src/test/java
target
    target/classes        
```

 - `src` - all source code
 - `src/main/java` - entry point for the applications source
 - `src/main/resources` - other files that are needed at runtime
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
[git-scm.com A short history](https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git)]
Some of the goals for Git were:

* Speed
* Simple design
* Support for parallel development
* Fully distributed
* Efficiently handle large projects

## Quick Start Guide
* Get and install git: [https://git-scm.com/downloads](https://git-scm.com/downloads)
* `git clone git@github.com/dude/project` - get a local copy of the project
* `git fetch` - get the latest changes from the server, without applying them to your working copy
* `git status` - list the changes on your working copy and show, if they are included in your next commit
* `git add <pathspec>` - add the specified file (also multiple files and globing allowed) to the next commit (stage the file)
* `git rm --cached <pathspec>` - remove the specified file from the commit list (unstage the file), but keep the local changes
* `git commit -m <message>` - commit the staged files and add the specified commit message
* `git diff` - show changes between the latest commit and the working copy
* `git push` - send the commits of the current branch to the repository
* `git pull` - get the latest commits of the current branch from the repository
* `git checkout <branch>` - switch to the specified branch. Use `-b` to create a new branch

## Version Control
Version control systems (VCS) serve mainly two purposes: 
1) Keeping track of every change that happens to the code
2) Facilitate simultaneous edition (by multiple programmers) of the same project

Thanks to VCS it is possible to easily revert to any revision ever made, find out when exactly a feature (or bug) was introduced etc. Further more, it is also possible to see, who wrote what and when.

The fantastic merging capabilities introduced with Git enable programmers to easily unify their working copies without overwriting each others changes. This outstanding feature made git the most popular VCS today. Still, every programmer has its own version, but git simplifies merging these versions into a new, combined one.

## Branching Model
Apart of the very source of truth, the `main` (or `master`) branch, git allows to have some diverging source trees called branches. Branches allow to make and test some changes, without messing with the main code. A branch can be imagined as if it would be a completely separated copy of the code.

It is very common to develop new features in a dedicated branch. This brings the advantage, that p.ex. an unfinished feature doesn't block the development of a hot-fix in the main branch.

Branches can easily be compared and merged. The hot-fix from above could therefore be merged into the feature branch, so the feature could be finished and tested already with the hot-fix included, before being merged back into the main branch.

## Collaboration

## Data Model

## Tooling

\newpage
![](img/xkcd_1597.png)

[Image Credit: [xkcd.com/1597](https://xkcd.com/1597/)]

![Branching model](img/git-branching-model.png)
[Image Credit: [https://nvie.com/posts/a-successful-git-branching-model/](https://nvie.com/posts/a-successful-git-branching-model/)]
