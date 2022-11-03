---
name: Create Package Release
about: Checklist for new Python package releases
title: "[RELEASE]"
labels: ''
assignees: ''

---

Please do the following steps in order to release a new version of the package:

- [ ] Check out a new branch from `origin/main` just for the purpose of the release (link it to this issue)
- [ ] Run `pylint` and `velin` on the entire package
- [ ] Run the test suite, including all optional tests
- [ ] Generate all the documentation and review for errors and placeholders
- [ ] Check your workspace to confirm there are no staged changes or unknown files
- [ ] **If this is planned as the first major release:** Remove the "major_version_zero = true" line from `pyproject.toml`
- [ ] Run `cz bump` to update the changelog, bump the version number, and generate the proper tags
- [ ] Push all commits, including tags, with `git push --tags`
- [ ] Open a pull request for the release and request the relevant approvals
- [ ] Once approved, go to the "Tags" section of the github repository and draft a new release from the appropriate tagged version.
- [ ] Merge the PR
