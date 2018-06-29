# ETS Documentation - Start

## What is the ETS project?

ETS is a collection of components and practices which allow to build applications and libraries with Scala.

It is a software development framework and ecosystem consisting of:

- A strictly managed and reliably versioned Maven POM set which allows to build Scala libraries or applications where conflict-free interoperation of all ETS-covered external dependencies their transitive dependencies is guaranteed

- A collection of useful libraries built on top of this approach, which are guaranteed to work seamlessly with ETS-covered external dependencies and other ETS libraries

- A collection of Maven archetypes which allows to quickly bootstrap library or application projects that make use of the ETS ecosystem out-of-the-box.


## Table of contents

### Documentation for maintainers

These documents support those that extend and maintain ETS components.

- [Rules](Maintaining-ETS/rules.md)
- [Versioning](Maintaining-ETS/versioning.md)


### Official ETS libraries
- ElasticSearch REST Connector: [project home](https://github.com/Galeria-Kaufhof/ets-elasticsearch-rest-connector), [documentation](libraries/ElasticSearch-REST-Connector/index.md)
- Swift Object Store Adapter: [project home](https://github.com/Galeria-Kaufhof/ets-filestorage), [documentation](libraries/Filestorage/index.md)
- Utilities and Stages for Akka Streams: [project home](https://github.com/Galeria-Kaufhof/ets-akka-stream-utils), [documentation](libraries/Akka-Stream-Utils/index.md)


## ETS ecosystem version registry and compatibility matrix

| ETS version                | 0     | 1 |   |   |
|----------------------------|-------|---|---|---|
| ElasticSearch              | 6.x   |   |   |   |
| Cassandra                  | 2.x   |   |   |   |
| Postgres                   | 9.6   |   |   |   |
| OpenStack Object Storage   |       |   |   |   |


## Meta information

This is the global documentation for the ETS version 0 release. See https://github.com/Galeria-Kaufhof/ets-documentation/tree/0.x.x for its source code.

There is no documentation for previous ETS releases.

The documentation for the upcoming ETS 1 release takes place at https://github.com/Galeria-Kaufhof/ets-documentation/tree/master.
