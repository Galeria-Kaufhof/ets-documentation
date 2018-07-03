# Introduction

Using the ETS ecosystem makes building and maintaining Scala applications and libraries less error-prone and allows for higher productivity.

To achieve this, the ETS project offers the following components:

- A strictly managed and reliably versioned Maven POM set which allows to build Scala libraries or applications where conflict-free interoperation of all ETS-covered external dependencies and their transitive dependencies is guaranteed

- A collection of useful libraries built on top of this approach, which are guaranteed to work seamlessly with ETS-covered external dependencies and other ETS libraries

- A collection of Maven archetypes which allows to quickly bootstrap library or application projects that make use of the ETS ecosystem out-of-the-box.


## What ETS can be used for

Some senseful use cases for ETS are:

### Building an application

When building any kind of Scala application, a lot of non-functional aspects need to be covered:

- You need to think about how to structure your code base

- You need to manage the external dependencies of your application, initially and over time; this includes conflict management and subtle classpath problems which can arise if some of your dependencies pull identical transitive dependencies

- You need to think about how implement and manage software tests


Although ETS doesn't make these things go away, it can help you to start your project in a sane way and to keep it manageable and growable over time, because it offers several ready-to-use components and tools plus an opinionated take on the most important aspects of your project's lifecycle management.

While this limits your freedom in terms of code base structure, tool choice, dependency management and library choice a bit, this is actually key to reducing errors and increasing productivity, by reducing [yak shaving](https://en.wiktionary.org/wiki/yak_shaving) when starting off, and offering guard rails down the road.


### Building a library


### Cherry picking ETS libraries for your own project

