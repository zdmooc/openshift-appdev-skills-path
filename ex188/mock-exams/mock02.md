
# Mock EX188 — Sujet blanc 02 (2h30)

## Contexte
Tu récupères une image existante “cassée” (mauvaise config) et tu dois la rendre opérationnelle via un Containerfile et une exécution propre.

## Tâches
1) Choisir une image “app” (au choix) et la lancer volontairement avec une mauvaise variable d’environnement (provoquer un échec).
2) Diagnostiquer via logs/inspect/events et documenter la cause.
3) Construire une nouvelle image `mock02-fixed:1.0` (Containerfile) qui corrige la configuration :
   - variable par défaut
   - port correct exposé
4) Relancer et valider service.
5) Ajouter un volume (bind mount) pour la config et prouver que le changement de fichier modifie le comportement.
6) Créer un `compose.yml` qui lance 2 services et assure l’ordre de démarrage (ou retry côté app).

## Proof
- capture commandes + résultats + explication courte “cause → fix”.
