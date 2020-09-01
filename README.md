# What is this action for?

This action allows you to upload coverage report to [_Code Climate_](https://codeclimate.com/).

# How to use it?

You can use the following code as a new _GitHub Actions Workflow_:

```yaml
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
        format: {FORMAT-VALUE}
        output: {OUTPUT-VALUE}
        report: {REPORT-VALUE}
      env:
        CC_TEST_REPORTER_ID: {CC_TEST_REPORTER_ID-VALUE}
        GIT_BRANCH: {GIT_BRANCH-VALUE}
        GIT_COMMIT: {GIT_COMMIT-VALUE}
```

**Note:** everything contained in single curly brackets (`{ }`) needs to be replaced by your desired values

**Inputs:**
|   Input  | Required |           Default           | Description                             |
| :------: | :------: | :-------------------------: | :-------------------------------------- |
| `format` |  `false` |            `lcov`           | Format of the coverage report to upload |
| `output` |  `false` | `coverage/codeclimate.json` | Output file for the upload operation    |
| `report` |  `false` |     `coverage/lcov.info`    | Report file to upload                   |

**Environment variables:**
|        Variable       | Required | Description                                   |
| :-------------------: | :------: | :-------------------------------------------- |
| `CC_TEST_REPORTER_ID` |  `true`  | Code Climate reporter ID                      |
|      `GIT_BRANCH`     |  `true`  | Branch that the coverage report refers to     |
|      `GIT_COMMIT`     |  `true`  | Commit SHA that the coverage report refers to |
