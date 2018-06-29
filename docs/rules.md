# Rules

This document describes the code, architecture, and lifecycle rules that are obligatory for all ETS components.


## General rules

- All public ETS component code repositories have their home at `https://github.com/Galeria-Kaufhof/ets-<name-of-component>`

- All ETS components that release and publish artifacts used by others must follow the [Semantic Versioning 2.0.0 guidelines](https://semver.org/spec/v2.0.0.html) for versioning their releases

- All public ETS components must ship with a root folder `CHANGELOG.md` file that follows the [Keep a Changelog 1.0.0](https://keepachangelog.com/en/1.0.0/) guidelines

- All public ETS components must be released under [The MIT License](https://opensource.org/licenses/MIT) and must be copyright Galeria Kaufhof GmbH if released by Galeria Kaufhof GmbH employees or contractors


## Naming and namespacing rules

- The correct spelling of the long form name of ETS is `Galeria Kaufhof eShop Technology Stack`, the correct spelling of the medium form name is `eShop Technology Stack`, and the short form is `ETS`.

- ETS Software uses the Java namespace `de.kaufhof.ets`

- Within this namespace, each component has its own namespace/artifactId e.g. `filestorage`, resulting in the fully qualified namespace `de.kaufhof.ets.filestorage` 

- Within a component's namespace, each subcomponent has its own namespace/artifactId e.g. `core`, resulting in the fully qualified namespace `de.kaufhof.ets.filestorage.core` 

- The id of all artifacts an ETS component releases must start with `ets-`, e.g. `ets-library-parent`

- If your component is an ETS library or application, then if it has only one subcomponent, its artifactId must end with `-core`, e.g. `ets-filestorage-core`; additional subcomponents can have arbitrary artifactId endings, e.g. `ets-filestorage-nfs`

- Subcomponents of an ETS component must live in root subfolders which are named like the subcomponent's artifactId, e.g. `/ets-filestorage-core`

- Within a subcomponent's subfolder, create a source code hierarchy following the pattern `src/main/scala/de/kaufhof/ets/<component-name>/<subcomponent-name>`, e.g. `src/main/scala/de/kaufhof/ets/filestorage/core`

- Component and subcomponent names must be one-word all-lowercase UTF-8 `[a-z0-9]` strings
