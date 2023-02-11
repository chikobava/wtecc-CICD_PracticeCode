# Adding GitHub Triggers

This folder holds the files for the lab: _Adding GitHub Triggers_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Trigger the pipeline:

```shell
curl -X POST http://localhost:8090 \
  -H 'Content-Type: application/json' \
  -d '{"ref":"main","repository":{"url":"https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode"}}'
```

Check running pipelines:

```shell
tkn pipelinerun ls
```

Check logs:

```shell
tkn pipeline logs --last
```
