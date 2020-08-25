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
