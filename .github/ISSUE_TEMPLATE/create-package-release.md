---
name: Create Package Release
about: Checklist for new Python package releases
title: "[RELEASE]"
labels: ''
assignees: ''

---

Please do the following steps in order to release a new version of the package:

- [ ] Create or clone a branch for the release and make sure the latest commits from `main` have been merged in
- [ ] Run `pylint` and `velin` on the entire package
- [ ] Run the test suite, including all optional tests
- [ ] Run the `prep_release` command installed by `erutils[dev]` from the command-line to generate a stub release notes file for the new version. Edit with an English-language summary and commit the file in place.
- [ ] Generate all the documentation and review for errors and placeholders
- [ ] Check your workspace to confirm there are no staged changes or unknown files
- [ ] **If this is planned as the first major release:** Remove the "major_version_zero = true" line from `pyproject.toml`
- [ ] Push any/all local changes
- [ ] Open a PR from back to `main` with the proposed new version number as the title
- [ ] Once that is approved, but before it is merged, run `cz bump -ch` and then push with `git push --follow-tags`

Please only push once whenever possible. Multiple pushes will result in multiple releases, often with minor to no differences.
