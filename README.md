[![Build status](https://img.shields.io/github/workflow/status/kaskadi/action-cc-reporter/build?label=build&logo=mocha)](https://github.com/kaskadi/action-cc-reporter/actions?query=workflow%3Abuild)

**CodeClimate**

[![](https://img.shields.io/codeclimate/maintainability/kaskadi/action-cc-reporter?label=maintainability&logo=Code%20Climate)](https://codeclimate.com/github/kaskadi/action-cc-reporter)
[![](https://img.shields.io/codeclimate/tech-debt/kaskadi/action-cc-reporter?label=technical%20debt&logo=Code%20Climate)](https://codeclimate.com/github/kaskadi/action-cc-reporter)
<!-- ******** Can uncomment this when your coverage is in place ******** -->
<!-- [![](https://img.shields.io/codeclimate/coverage/kaskadi/action-cc-reporter?label=test%20coverage&logo=Code%20Climate)](https://codeclimate.com/github/kaskadi/action-cc-reporter) -->

**LGTM**

[![](https://img.shields.io/lgtm/grade/javascript/github/kaskadi/action-cc-reporter?label=code%20quality&logo=lgtm)](https://lgtm.com/projects/g/kaskadi/action-cc-reporter/?mode=list)

****

# Testing

`mocha`, `chai` & `standard` are available as dev dependencies.

****

# What is this action for?

:point_right: **Describe here what the action should do** :point_left:

# How to use it?

You can use the following code as a new _GitHub Actions Workflow_:

```
name: {YOUR-ACTION-NAME}
on: [{YOUR-ACTION-EVENT}]
jobs:
  {YOUR-JOB-NAME}:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: {YOUR-STEP-NAME}
      uses: kaskadi/action-cc-reporter@master
```

:point_down: **Here goes any extra details on how to use the action (environment variables/inputs description for example)** :point_down:

**Note:** everything contained in single curly brackets (`{ }`) needs to be replaced by your desired values
