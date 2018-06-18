# Versioning

This document describes how different versions of ETS component source codes and artifacts are managed, declared, structured and used within the development and release lifecycles of a component.


## ETS core and components versioning relationships

While there is no single central "ETS application" which is maintained and released in an integrated and central fashion, we nevertheless handle the offical ETS ecosystem as one connected construct, and version accordingly.

To do so, we define major ETS releases following the SemVer schema, thus subsuming ETS core components and ETS libraries under the same major version number for each release.

The result is a collection of components with publicly artifacts, where artifacts that share the same major version number are guaranteed to be compatible with each other.

Thus, for example, the "ETS version 1 release" is the collection of all 1.x.x versions of the different ETS components.

Because there is no central ETS artifact, releases of the general ETS ecosystem are not specified using a `major.minor.patch` schema. Instead, the concrete state of an "ETS version 1 release" is in constant flux - at a given point in time, it could be a collection of `ets-elasticsearch-rest-connector 1.4.3`, `ets-filestorage 1.2.0`, and `ets-akka-stream-utils 1.9.5`, and choosing from a subset of these components, and even choosing non-latest 1.x.x version of these components, as a basis for your "ETS version 1"-based application is legit and safe in terms of interoperability of the components.


## Git branching and tagging

All ETS component git repositories follow these rules:

- As soon as the first major non-0.x.x version of a component is released, the git repository must have a tag named `<current-major>.0.0` which points to the commit with which the release milestone was reached
- As soon as the first major non-0.x.x version of a component is released, the git repository must have a branch named `<current-major>.x.x` whose tip points to the latest version of the code within the current major version
- Whenever new minor/patch versions are released within a major release, `<major>.<minor>.<patch>` tags must be created accordingly
- The latest version of the upcoming but not yet released minor/patch version of a released major version is developed in the `<major>.x.x` branch
- Meanwhile, the latest version of the upcoming but not yet released `<current-major + 1>` version of the component is developed in the `master` branch
- As soon as a new major version (= `<current-major + 1>`) is released, a tag named `<current-major + 1>.0.0` and a new branch `<current-major + 1>.0.0` must be created
- Thus, `<current-major + 1>` becomes the new `<current-major>`
- Again, the latest version of the upcoming but not yet released `<current-major+1>` version of the component is developed in the `master` branch

### Example:

Let's assume that ETS has already been released in versions `1` and `2`, and work on a version `3` release are ongoing. In this case, the git branch and tag structure of a hypothetical ETS component `ets-foo-connector` might look as follows:

- A branch `master` exists, containing the current work that is underway to prepare release `ets-foo-connector 3.0.0` for the upcoming ETS version 3 release
- A branch `1.x.x` exists, because `ets-foo-connector` was part of the ETS version 1 release; it contains the latest code for this major version, up to and including a couple of not-yet-released changes for a bugfix that will be released as `ets-foo-connector 1.2.1`
- The tags `1.0.0`, `1.2.0`, and `1.3.0` exist. They all point to commits that are also included within the commit history of branch `1.x.x`, and mark the different minor versions that this component released within the ETS version 1 release
- A branch `2.x.x` exists, because `ets-foo-connector` was part of the ETS version 2 release
- Only the tag `2.0.0` exists, because after the initial 2.x.x release, the project did not release any new versions under the ETS version 2 release
