# Deploy to Kubernetes / OpenShift

This folder holds the files for the lab: _Deploy to Kubernetes_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Search for cli plugin:

```shell
tkn hub search cli
```

Get info on the openshift plugin:

```shell
tkn hub info task openshift-client
```

To start the app:

```shell
tkn pipeline start cd-pipeline \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch=main \
    -p app-name=hitcounter \
    -p build-image=image-registry.openshift-image-registry.svc:5000/$SN_ICR_NAMESPACE/tekton-lab:latest \
    -w name=pipeline-workspace,claimName=pipelinerun-pvc \
    --showlog
```