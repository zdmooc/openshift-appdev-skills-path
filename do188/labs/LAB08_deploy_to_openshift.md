
# LAB08 — Premier déploiement sur OpenShift (image existante)

## Objectif
Déployer une image dans OpenShift et l’exposer via Route.

## Tâches (CLI)
1) Créer un projet `do188-lab08`.
2) Déployer une application (Deployment) depuis une image.
3) Créer un Service.
4) Créer une Route.
5) Vérifier l’accès HTTP.
6) Récupérer logs + events.

## Proof
- `oc get all -n do188-lab08`
- Route accessible (curl)
- `oc logs` montre des accès

## Cleanup
- supprimer le projet
