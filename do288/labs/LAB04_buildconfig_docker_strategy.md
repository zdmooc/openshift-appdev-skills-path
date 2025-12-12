
# LAB04 — BuildConfig (Docker/Containerfile strategy)

## Objectif
Build une image depuis un repo Git (ou dossier local importé) et publier dans registry interne.

## Tâches
- Créer BuildConfig Docker strategy
- Lancer un build
- Vérifier ImageStreamTag créé
- Déployer depuis ImageStreamTag

## Proof
- `oc get bc,is`
- `oc describe is ...`
