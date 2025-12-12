
# LAB07 — Tekton pipeline build→test→deploy

## Objectif
Avoir un PipelineRun qui :
1) build une image
2) exécute un test simple (curl endpoint ou unit test)
3) déploie/maj un Deployment

## Proof
- `tkn pipelinerun logs -f ...`
- route OK
