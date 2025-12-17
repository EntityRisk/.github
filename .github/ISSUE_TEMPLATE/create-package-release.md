---
name: Create Package Release
about: Checklist for new Python package releases
title: "[RELEASE]"
labels: ''
assignees: ''
---

## Instructions

Please do the following steps in order to release a new version of the package:

- [ ] Create or clone a branch for the release and make sure the latest commits from `main` have been merged in
- [ ] Pull all tags with `git pull --tags`
- [ ] Run `pre-commit run --all-files`
- [ ] Run the test suite, including all optional tests
- [ ] Run the `prep_release` command installed by `erutils[dev]` from the command line to generate a stub release notes file for the new version. Edit with an English-language summary (see #guidelines) and commit the file in place.
- [ ] Generate all the documentation and review for errors and placeholders
- [ ] Check your workspace to confirm there are no staged changes or unknown files
- [ ] **If this is planned as the first major release:** Remove the "major_version_zero = true" line from `pyproject.toml`
- [ ] Push any/all local changes
- [ ] Open a PR from back to `main` with the proposed new version number as the title
- [ ] Upon completion of review, the reviewer should approve **by comment only** (as opposed to official approval) to prevert premature merging to `main`
- [ ] Run `cz bump --dry-run` and confirm that the commitizen-derived version bump is the expected increment as per [Semantic Versioning](https://semver.org/)
- [ ] Run `cz bump -ch --no-verify` and then push with `git push && git push --follow-tags`
- [ ] The reviewer must then formally approve the PR to be merged.

## Guidelines

The following are guidelines for preparing the user-facing release notes.

- Inspect the previous releases and follow their conventions, with preference to the most recent ones.
- Include details regarding the changes that are relevant to the user. Do not include implementation details that are not user-facing.
- Updates should be included in all applicable sections. For example, a bug fix that introduces a breaking change should be listed under both the "API changes" and "Bug fixes" sections.
