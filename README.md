# ETS - The Galeria Kaufhof eShop Technology Stack

## Documentation project

### About ETS

ETS is a collection of components and practices which allow to build applications and libraries with Scala.

See the [list of all ETS components](https://github.com/topics/galeria-kaufhof-ets) on GitHub.


### About this project

The ETS Documentation project is the central place to learn how to work within the ETS ecosystem and how to extend and grow it.

To view the current release of the HTML version of the ETS documentation, go to [https://galeria-kaufhof.github.io/ets-documentation/](https://galeria-kaufhof.github.io/ets-documentation/).

To browse the latest available content within this branch, start at [docs/index.md](docs/index.md).



### Building and publishing the documentation

Using this codebase, `mkdocs`, and GitHub pages, we regularly publish the documentation for the most recent version of the the current major release of ETS to https://galeria-kaufhof.github.io/ets-documentation/.

To do so, install [mkdocs](https://www.mkdocs.org/#installation) locally, clone this repository, switch to branch `<current-major>.x.x`, and run `mkdocs gh-deploy`.

Documentation for previous major versions of ETS will not be made available as HTML on our GitHub pages. Instead, the most recent published documentation will refer to previous documentation versions by linking directly to the `docs/index.md` file in the branch of the previous release on GitHub.
