
# LAB06 — Packager la même app (Template / Helm / Kustomize)

## Objectif
Une app multi-services (web+api) packagée en 3 méthodes.

## Tâches (résumé)
- Template : ajouter paramètres (image, replicas, hostname)
- Helm : values par env (dev/test/prod)
- Kustomize : base + overlays (patch replicas/env/route)

## Proof
- `helm template` rend un manifest valide
- `kustomize build overlays/dev` rend un manifest valide
- `oc process -f template.yaml -p ... | oc apply -f -` fonctionne
