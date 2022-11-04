---
title: "Unhinged Engineering"
date: 2022-11-04T08:37:09-04:00
draft: false
---
This is a loose collection of aggressive development process ideas. Some I have implemented and others I haven't although I will as soon as the opportunity arises.

1. **Automated testing**: tests are run automatically on each new `feature` branch and must meet coverage and quality requirements - these should be treated as "baseline" regression and constantly updated.
2. **Automated process**: between `git branch feature` and `git merge feature` no step should be manual - running tests, checking coverage, enforcing formatting, moving stories, alerting testers, and everything else should be automated.
3. **Anti-conveyor belt**: no change is "handed off" to the next team (e.g. QA) - every proposed change is closely followed by the requesting developer through each step of the process which should ideally be short.
4. **Reverse QA bottleneck**: developers join QA teams in manually reviewing `feature` branches - this should a) make testing requirements explicit and b) allow developers to immediately understand issues as they are discovered turning a bottleneck into a value-add.
5. **Dual branches**: only `master` and `feature` branches exist in the development process - `feature` branches are created on-demand for each pull request with `master` as the source of truth protected by merge requirements and is constantly deployed to production from `HEAD`.
6. **Single pull requests deploys**: a single, logical piece of work attached to a story under the responsibility of a sole developer - this isolates blast radius and decreases complexity in understanding errors as they arise.
7. **Roll forward fixes**: bug in production are fixed via pull request incrementing the release number - rollback strategies are admitting you were wrong while rollforward strategies are declaring you just weren't right yet.
8. **Single file deploys**: individual pull requests contain a single changed production file - this excludes test files and mandates small, incremental deployments.
9. **Test in production**: developers manually testing new features in the production environment - this would come _after_ automated tests on feature branches but is still critical because they're never _quite_ the real thing.

This is a non-exhaustive listing but what is here is to encourage _speed_ and _dynamism_ throughout the development cycle.

> Our enemy is entropy