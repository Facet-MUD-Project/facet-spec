# Stage 0 - Skeleton Repository

This is the very beginning of an implementation, before any actual development
work happens. The goal here is to get the repository set up with all of the
basic pieces needed to ensure a successful project.

## Required Files

A stage 0 repository MUST have all of the following files:

* `.editorconfig`
* `.gitignore` - SHOULD be created from a GitHub template
* `CODE_OF_CONDUCT.md` - Contributor Covenant >=v1.4
* `LICENSE` - The MIT license
* `README.md` - At this stage, no required content in this file

## Optional Files

A stage 0 repository SHOULD have the following files:

* Issue templates
* Pull request templates
* `.pre-commit-config.yaml` - Set up pre-commit to run appropriate checks
  before git commits.

## Required Config

A stage 0 repository MUST have the following configuration set up:

* Branch protection rules for the default branch including at least 1 required
  reviewer.
* Merge commits MUST NOT be allowed
* "Automatically delete head branches" SHOULD be enabled

## Recommended Setup

A stage 0 repository SHOULD use a package manager appropriate for the language,
when possible. When multiple are available, every effort should be made to find
the option which will work best for our scenario, and has the largest body of community support available.
