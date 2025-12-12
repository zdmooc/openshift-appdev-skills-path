
# EX288 — Runbook Troubleshooting (builds, deploy, routes, pipelines)

## 1) Build en échec
- `oc get builds`
- `oc logs -f build/<name>`
- vérifier : git ref, Dockerfile path, permissions, quota, registry auth

## 2) Pod CrashLoopBackOff
- `oc describe pod <pod>` (events + reason)
- `oc logs <pod> -c <container>`
- vérifier : env, configmap/secret, ports, probes, imagePull

## 3) Route 503 / timeout
- vérifier Service endpoints : `oc get endpointslices`
- vérifier readiness : pod Ready?
- vérifier targetPort/port/service selector
- tester via `oc port-forward`

## 4) ImageStream trigger ne déclenche pas
- vérifier `is` et tags
- vérifier annotations/trigger du Deployment/DeploymentConfig
- vérifier que l’image a bien changé (digest)

## 5) Tekton PipelineRun en échec
- `tkn pipelinerun logs -f <name>`
- vérifier workspaces, serviceaccount, permissions, params, tasks refs
