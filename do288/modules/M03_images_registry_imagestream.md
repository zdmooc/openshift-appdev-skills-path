
# M03 — Images, registry interne, ImageStreams

## Objectifs
- Pousser une image vers la registry interne
- Créer/mettre à jour un ImageStream
- Comprendre triggers basés sur ImageStream

## Diagramme
```mermaid
flowchart LR
  Build[BuildConfig/S2I] --> IS[ImageStreamTag]
  IS --> Deploy[Deployment]
  Deploy --> Route[Route]
  IS -->|trigger| Deploy
```
