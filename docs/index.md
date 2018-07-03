# ETS Documentation - Start

## What is the ETS project?

ETS is a collection of components and practices which allow to build applications and libraries with Scala.

It is a software development framework and ecosystem consisting of:

- A strictly managed and reliably versioned Maven POM set which allows to build Scala libraries or applications where conflict-free interoperation of all ETS-covered external dependencies and their transitive dependencies is guaranteed

- A collection of useful libraries built on top of this approach, which are guaranteed to work seamlessly with ETS-covered external dependencies and other ETS libraries

- A collection of Maven archetypes which allows to quickly bootstrap library or application projects that make use of the ETS ecosystem out-of-the-box.


## Table of contents

### General documentation

- [Architecture & philosophy](architecture-and-philosophy.md)


### Documentation for maintainers

These documents support those that extend and maintain ETS components.

- [Rules](Contributing-to-and-maintaining-ETS/rules.md)
- [Versioning](Contributing-to-and-maintaining-ETS/versioning.md)
- [Contributing](Contributing-to-and-maintaining-ETS/contributing.md)


## ETS ecosystem overview

### Version overview

| ETS version                                                          | Lifecycle status    |
|----------------------------------------------------------------------|---------------------|
| [0](https://github.com/Galeria-Kaufhof/ets-documentation/tree/0.x.x) | Upcoming            |


### Managed external dependencies

| ETS version              | 0   |
|--------------------------|-----|
| ElasticSearch            | 6.x |
| Cassandra                | 2.x |
| Postgres                 | 9.6 |
| OpenStack Object Storage |     |


### ETS library availability

| ETS version                  | 0                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Filestorage                  | [code](https://github.com/Galeria-Kaufhof/ets-filestorage/tree/0.x.x),                  [docs](libraries/Filestorage/index.md)                  |
| Akka Stream Utils            | [code](https://github.com/Galeria-Kaufhof/ets-akka-stream-utils/tree/0.x.x),            [docs](libraries/Akka-Stream-Utils/index.md)            |
| ElasticSearch REST Connector | [code](https://github.com/Galeria-Kaufhof/ets-elasticsearch-rest-connector/tree/0.x.x), [docs](libraries/ElasticSearch-REST-Connector/index.md) |



## Meta information

This is the global documentation for the ETS version 0 release. See https://github.com/Galeria-Kaufhof/ets-documentation/tree/0.x.x for its source code.

There is no documentation for previous ETS releases.
