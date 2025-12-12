
# M04 — Containerfile (build propre, reproductible, minimal)

## Objectifs
- Écrire un Containerfile lisible et maintenable
- Comprendre USER/WORKDIR/CMD/ENTRYPOINT
- Gérer config runtime (ENV, ports, volumes)

## Règles d’or
- Un build = une intention claire
- Minimiser le nombre de layers “bruyants”
- Ne pas exécuter en root si inutile
- Définir un HEALTHCHECK (si demandé) via app ou orchestration

## Lab principal
Voir `do188/labs/LAB04_containerfile_webapp.md`.
