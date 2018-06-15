# ETS Documentation - Rules

This document describes the code, architecture, and lifecycle rules that are obligatory for all ETS components.


## General rules

- All public ETS component code repositories have their home at https://github.com/Galeria-Kaufhof/ets-<name-of-component>

- All ETS components that release software used by others must follow the [Semantic Versioning 2.0.0 guidelines](https://semver.org/spec/v2.0.0.html) for versioning their releases

- All public ETS components must ship with a root folder CHANGELOG.md file that follows the [Keep a Changelog 1.0.0](https://keepachangelog.com/en/1.0.0/) guidelines

- All public ETS components must be released under [The MIT License](https://opensource.org/licenses/MIT) and must be copyright Galeria Kaufhof GmbH if released by Galeria Kaufhof GmbH employees or contractors


## Naming and namespacing rules

- ETS Software uses the Java namespace `de.kaufhof.ets`

- Within this namespace, each component has its own namespace/artifactId which must start with ` ets-`, e.g. `ets-library-parent`
