---
name: Create Package Release
about: Checklist for new Python package releases
title: "[RELEASE]"
labels: ''
assignees: ''

---

Please do the following steps in order to release a new version of the package:

- [ ] Clone `origin/releases` and make sure the latest commits from `main` have been merged in
- [ ] Run `pylint` and `velin` on the entire package
- [ ] Run the test suite, including all optional tests
- [ ] Generate all the documentation and review for errors and placeholders
- [ ] Check your workspace to confirm there are no staged changes or unknown files
- [ ] **If this is planned as the first major release:** Remove the "major_version_zero = true" line from `pyproject.toml`
- [ ] Run `cz bump` to update the changelog, bump the version number, and generate the proper tags
- [ ] Push all commits, including tags, with `git push --tags`
- [ ] Go to the "Tags" section of the github repository and draft a new release from the appropriate tagged version.
