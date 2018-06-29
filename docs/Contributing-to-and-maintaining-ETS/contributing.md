# Contributing

## General rules and workflow

Note: read "ETS version" and "ETS release" as "version of the ETS component you want to contribute to" and "release of the ETS component you want to contribute to". We use the short form here to save bytes.

- Even if you have write access to an ETS component repository, always work in a branch to contribute changes
- Only release managers may push changes into the `master` branch and the `<major>.x.x` branches, and may do so only for release related tasks
- If you want your change to become part of an upcoming ETS release (with possible backporting to already released ETS versions), then branch from `master`, and make the PR against `master`
- If you want your changes to be applied to one or more already released ETS versions, but not to the upcoming release, then branch from the `<major>.x.x` branch of the *lowest* ETS version you want to apply your changes to, and make the PR against this branch
- You can open a PR for your changes as soon as you have opened a branch for the changes, even while your branch is still work in progress. However, in this case the PR title must be prefixed with `WIP: `
- Alternatively, open the PR only once your branch is ready to be merged
- force-push on your branch is permitted
- During development, rebase at least once, and do so the moment before offering the PR for merging
- It is recommended to rebase your branch whenever there is a change in the master
- Contribute accompanying documentation changes to the `ets-documentation` repository the same way that you contribute your code changes to the ETS component repository - all of the above rules apply; this means if your code changes demand documentation changes, you must also create a branch and PR on the `ets-documentation` repository, and your code PR description must reference your documentation PR


## How contributions are integrated

For each contribution, the release manager must decide if the contribution shall only be integrated into the upcoming major ETS release, or if it should also be backported to already released ETS versions. 


## Without backporting

- The pull request is merged into the master, and the commit message of the merge must contain `closes: #<id-of-pr>`


## With backporting

- Decide on the lowest ETS version to which the changes shall be backported ("lowest target")
- Fetch the branch containing the changes ("source branch")
- Checkout the `<major>.x.x` branch of the ETS component, where `<major>` is the lowest ETS version you chose ("target branch")
- Cherry-pick the commits of the source branch into the target branch, add `closes #<id-of-pr>` to the commit message
- For each ETS version larger than the lowest target, check out out its `<major>.x.x` branch, which becomes the new "target branch", and merge the previous target branch into it (e.g. `git checkout 2.x.x; git merge 1.x.x`) - this must happen in order, from lowest to largest major version
- Conflicts during merge must be handled as follows:
  - If conflicts arise in `pom.xml` files, simply roll back the changes introduced by the merge on these files
  - Handle new files which are introduced as a conflict that must be manually solved: if these files are not required on this particular version, they must be removed
  - Handle other conflicts as usual
- Commit the merge result, and continue with the next major version branch, if any
- If no major version branches are "left", and the changes must become part of the upcoming ETS release, merge the `<major>.x.x` branch with the largest major version into `master`
- Finally, push all changed branches

It is important to note that we *always* need to merge each PR all the way up to `master`, even if this results in empty changesets for "higher" version branches and/or `master`. This guarantees that a PR which only applies to e.g. `1.x.x` that is followed by a PR which applies to `1.x.x` and `2.x.x` and `master` doesn't need to be handled when merging the latter PR.
