# ETS Documentation - Start

## What is the ETS project?

ETS is a collection of components and practices which allow to build applications and libraries with Scala.

It is a software development framework and ecosystem consisting of:

- A strictly managed and reliably versioned Maven POM set which allows to build Scala libraries or applications where conflict-free interoperation of all ETS-covered external dependencies their transitive dependencies is guaranteed

- A collection of useful libraries built on top of this approach, which are guaranteed to work seamlessly with ETS-covered external dependencies and other ETS libraries

- A collection of Maven archetypes which allows to quickly bootstrap library or application projects that make use of the ETS ecosystem out-of-the-box.


## Table of contents

### General documentation
- [Rules](rules.md)


### Official ETS libraries
- ElasticSearch REST Connector: [project home](https://github.com/Galeria-Kaufhof/ets-elasticsearch-rest-connector), [documentation](libraries/elasticsearch-rest-connector/index.md)
- Swift Object Store Adapter: [project home](https://github.com/Galeria-Kaufhof/ets-filestorage), [documentation](libraries/ets-filestorage/index.md)
- Utilities and Stages for Akka Streams: [project home](https://github.com/Galeria-Kaufhof/ets-akka-stream-utils), [documentation](libraries/ets-akka-stream-utils/index.md)


## ETS ecosystem version registry and compatibility matrix

| ETS version                | 0.1.x |   |   |   |
|----------------------------|-------|---|---|---|
| ElasticSearch              | 6.x   |   |   |   |
| Cassandra                  | 2.x   |   |   |   |
| OpenStack Object Storage   |       |   |   |   |
