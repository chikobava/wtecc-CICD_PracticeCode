# Integrate Unit Test Automation

This folder holds the files for the lab: _Integrate Unit Test Automation_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Install lint task:

```shell
tkn hub install task flake8
```

Run the pipeline:

```shell
tkn pipeline start cd-pipeline \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch="main" \
    -w name=pipeline-workspace,claimName=pipelinerun-pvc \
    --showlog
```