
# M07 — OpenShift Pipelines (Tekton)

## Objectifs
- Comprendre Task / Pipeline / PipelineRun / Workspace
- Définir un workflow build→test→deploy
- Diagnostiquer un PipelineRun en échec

## Diagramme
```mermaid
flowchart LR
  Src[Git] --> PR[PipelineRun]
  PR --> T1[Task: build]
  T1 --> T2[Task: test]
  T2 --> T3[Task: deploy]
  T3 --> Route[Route OK]
```
