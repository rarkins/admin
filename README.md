# Renovate Mirrors

"Renovate Mirrors" is a GitHub org that lets you fully "dry run" a (public) project.

Here's how it works:

* Submit an issue to this repository (renovate-mirrors/admin) suggesting that a repository be added. You do not need to be the owner because we're doing nothing that the public can't already do

* We will (manually) fork the repository into the @renovate-mirrors organization

* Renovate will onboard this repository like usual

* The onboarding PR can be updated/edited like usual, producing an updated onboarding PR decription

* The onboarding PR will be merged into a `renovate-config` branch instead of `master`

* Renovate will keep the `master` branch of the fork in sync with `master` of the source repository, so that the updates in the fork are always compared against the very latest in the source repository

* Renovate PRs will be raised entirely within the forked repository, and not the source

* If you wish, you can manually create PRs from the mirror repository's branch into the source repository


So the main differences are:

1. The source repository never receives any PRs or requires any config
2. You won't see your usual test suites run, because of (1)
