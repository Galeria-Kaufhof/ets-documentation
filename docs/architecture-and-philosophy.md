# Architecture and Philosophy

## Architecture

### ETS is not an artifact, it's an ecosystem

There is no such thing as an integrated and deployable "ETS software" artifact. Neither is it a software development framework.

It is an ecosystem of components that are developed under the same [rules](rules.md), the same [versioning approach](versioning.md), and the same philosophy, which leads to a collection of artifacts that are guaranteed to play well together, and which can be used to build applications on top of them with a minimal amount of yak shaving. Additionally, the ecosystem provides helpers like our [archetypes](archetypes.md) to boost development productivity even more.


## Philosophy

### Always stay near the cutting edge

 We upgrade all external dependencies (including Scala and the JVM) to their most recent stable versions as soon as possible, keeping the ETS ecosystem compatible with the youngest iteration of the real world as soon as we can. While we do maintain previous ETS releases for a while, backwards-compatibility and long-term support of released versions is not our primary goal. We believe that this is better for a healthy and maintainable application landscape.
