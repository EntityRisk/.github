---
name: QC Review Template
about: This standard checklist should be used for QC on all projects
title: "[QC]"
labels: qualitycontrol
assignees: ''

---

Before sending an analytic deliverable to a client, someone other than the primary analyst should go through this checklist to confirm the results are correct.

- [ ] All relevant issues and pull requests have been closed
- [ ] A second set of eyes has reviewed all the code being used to support the deliverable
- [ ] You can run the code from start to finish and reproduce the results (to within statistical variation if Monte Carlo techniques are employed)
- [ ] Edge-case and extreme value testing produces expected results
- [ ] The final results are internally consistent
- [ ] When applicable, the results have been compared to external sources
- [ ] New issues have been created for any problems identified above
- [ ] All issues created in the previous step have now been closed

Once everything is complete, the QC review is finished and this issue may be closed.
