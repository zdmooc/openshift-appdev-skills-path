
# Diagrammes — Vue d’ensemble du skills path

```mermaid
flowchart LR
  A[DO188\nContainers + Podman + bases OCP] --> B[EX188\nPratique: container ops]
  B --> C[DO288\nBuild/Deploy cloud-native sur OCP]
  C --> D[EX288\nPratique: déploiement applicatif OCP]

  subgraph DO188
    A1[Podman] --> A2[Images/Registries]
    A2 --> A3[Containerfile]
    A3 --> A4[Volumes/Persistence]
    A4 --> A5[Troubleshooting]
    A5 --> A6[Compose]
    A6 --> A7[K8s/OCP basics]
  end

  subgraph DO288
    C1[Console dev + oc] --> C2[Registry interne]
    C2 --> C3[Builds/S2I]
    C3 --> C4[Deployments + probes]
    C4 --> C5[Templates/Helm/Kustomize]
    C5 --> C6[Tekton Pipelines]
  end
```

```mermaid
flowchart TB
  Dev[Code] -->|git push| Build[Build (S2I / Docker)\nBuildConfig]
  Build --> IS[ImageStream]
  IS --> Deploy[Deployment/DeploymentConfig]
  Deploy --> SVC[Service]
  SVC --> Route[Route]
  Route --> Users[Users]
```
