
# M01 — OpenShift pour développeurs

## Objectifs
- Être à l’aise avec la console, `oc`, namespaces/projets
- Comprendre les objets “dev” : Deployment, Service, Route, ConfigMap, Secret
- Savoir lire des events et diagnostiquer un pod

## Mini-labs
- Créer 3 projets : dev/test/prod + labels
- Déployer un Pod simple et lire logs/events
- Nettoyer

## Proof
- `oc get project`
- `oc get events --sort-by=.metadata.creationTimestamp | tail`
