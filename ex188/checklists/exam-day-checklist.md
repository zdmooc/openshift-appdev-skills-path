
# EX188 — Checklist jour J

## Avant de démarrer (5 min)
- Lire toutes les tâches, identifier dépendances.
- Noter : noms imposés, ports, volumes, registries, tags.
- Repérer les tâches “à risque” (auth registry, permissions, volumes).

## Pendant l’exécution
- Toujours valider au fur et à mesure (pas à la fin).
- Après chaque tâche : **Proof** (commande + résultat).
- Si tu bloques > 7 minutes : appliquer le Runbook Debug.

## Fin d’épreuve (10–15 min)
- Refaire un tour : `podman ps -a`, endpoints, ports, tags, push.
- Vérifier que tous les containers requis tournent.
- Vérifier que les images demandées existent et ont été poussées si requis.
