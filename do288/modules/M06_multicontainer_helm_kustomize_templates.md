
# M06 — Multi-container : Templates, Helm, Kustomize

## Objectifs
- Packager une même app sous 3 formes
- Paramétrer par environnement (values / overlays / parameters)
- Être capable de debug un rendu (render) et un déploiement

## Diagramme (comparaison)
```mermaid
flowchart TB
  subgraph Template
    T1[template.yaml] --> T2[oc process -p ...]
  end
  subgraph Helm
    H1[Chart] --> H2[values.yaml] --> H3[helm template/install]
  end
  subgraph Kustomize
    K1[base] --> K2[overlays] --> K3[kustomize build]
  end
  T2 --> OCP[OpenShift]
  H3 --> OCP
  K3 --> OCP
```
