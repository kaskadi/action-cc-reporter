# What is this action for?

This action allows you to upload coverage report to [_Code Climate_](https://codeclimate.com/).

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
|   Input  | Required |           Default           | Description                          |
|:--------:|:--------:|:---------------------------:|--------------------------------------|
| `format` |    No    |            `lcov`           | Format of your coverage report       |
|  `ouput` |    No    | `coverage/codeclimate.json` | Output file for the upload operation |
| `report` |    No    |     `coverage/lcov.info`    | Report file to upload                |

**Environment variables:**
|        Variable       | Required | Description                                 |
|:---------------------:|:--------:|---------------------------------------------|
| `CC_TEST_REPORTER_ID` |    Yes   | Reporter ID associated with your repository |
|      `GIT_BRANCH`     |    Yes   | Branch you want your report to refer to     |
|      `GIT_COMMIT`     |    Yes   | Commit SHA you want your report to refer to |
