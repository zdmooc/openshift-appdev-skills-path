
# Démarrage — Poste, outils, cluster, règles de travail

## Objectif
Mettre en place un environnement de pratique **reproductible** et **proche des contraintes d’examen** (tâches pratiques, preuves objectives, documentation locale).

## Outils minimum
### Local (DO188 / EX188)
- podman (rootless), podman-compose (ou compose v2 si supporté), git
- un éditeur (VS Code + extension YAML conseillé)
- curl, jq

### Cluster (DO288 / EX288)
- oc CLI (OpenShift)
- helm
- kustomize (ou `kubectl kustomize` selon ton setup)
- accès à la console OpenShift

## Cluster de pratique (choisir 1)
- OpenShift Local (CRC) : idéal solo
- Un cluster OCP existant : idéal si tu peux créer des projets et routes

## Règles “mode examen”
1) **Tout ce que tu fais doit être vérifiable** : pas de “ça marche chez moi”.  
2) À la fin de chaque lab : section **Proof** (commandes + sorties attendues).  
3) Tu nettoies : scripts de cleanup, suppression projets, suppression images si besoin.  
4) Tu ne copies pas des manifest sans comprendre : tu sais expliquer chaque champ critique.

## Conventions du dépôt
- Chaque module : objectifs → notions → check → pièges → exercices
- Chaque lab : contexte → tâches → contraintes → validation (Proof) → cleanup

## Tracker de progression
Voir `docs/PROGRESS-TRACKER.csv`.
