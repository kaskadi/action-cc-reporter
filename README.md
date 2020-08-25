# What is this action for?

This action allows you to upload

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
      with:
        format: {REPORT-FORMAT}
        output: {OUTPUT-FILE}
        report: {REPORT-FILE}
      env:
        CC_TEST_REPORTER_ID: ${{ secrets.{YOUR-CODE-CLIMATE-REPORTER-ID} }}
        GIT_BRANCH: {DESIRED-GIT-BRANCH}
        GIT_COMMIT: {DESIRED-GIT-COMMIT-SHA}
```

**Note:** everything contained in single curly brackets (`{ }`) needs to be replaced by your desired values

**Inputs:**
- `format` **[optional]**: defines the format used by your report _(default: `lcov`)_
- `ouput` **[optional]**: defines the output file where the output is written while uploading _(default: `coverage/codeclimate.json`)_
- `report` **[optional]**: defines the report file to upload _(default: `coverage/lcov.info`)_

**Environment variables:**
- `CC_TEST_REPORTER_ID` **[required]**: the reporter ID for your repository (see _Code Climate_)
- `GIT_BRANCH` **[required]**: the branch you want your report to refer to _(default: branch from which the action is running inside of the runner)_
- `GIT_COMMIT` **[required]**: the commit SHA you want your report to refer to _(default: SHA of the commit that triggered the workflow)_
