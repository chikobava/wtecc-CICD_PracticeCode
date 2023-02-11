# Building an Image

This folder holds the files for the lab: _Building an Image_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

```shell
tkn hub search --kinds task build
```

```shell
tkn clustertask ls
```

```shell
tkn pipeline start cd-pipeline \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch=main \
    -p build-image=image-registry.openshift-image-registry.svc:5000/$SN_ICR_NAMESPACE/tekton-lab:latest \
    -w name=pipeline-workspace,claimName=pipelinerun-pvc \
    --showlog
```

```shell
tkn pipelinerun ls
tkn pipelinerun logs --last
```