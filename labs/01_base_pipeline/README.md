# Create a base pipeline

This folder holds the files for the lab _Create a Base Pipeline_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.
Add task and pipeline to your cluster:
```shell
kubectl apply -f pipeline.yaml
kubectl apply -f tasks.yaml
```

Run the pipeline:

```shell
tkn pipeline start cd-pipeline \
    --showlog \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch="main"
```