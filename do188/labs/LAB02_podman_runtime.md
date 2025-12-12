
# LAB02 — Podman runtime (run/exec/logs/inspect)

## Contexte
Tu dois lancer un service web en container, l’observer, puis diagnostiquer un problème simple.

## Tâches
1) Lancer un container web en détaché, exposer un port vers localhost.
2) Vérifier que l’endpoint répond (HTTP 200).
3) Lire les logs et identifier le process principal.
4) Entrer dans le container, vérifier la config (fichier + process).
5) Modifier la config via variable d’environnement (si l’image le permet) OU via un bind mount (fichier de conf).
6) Nettoyer.

## Contraintes
- Le container doit s’appeler `lab02-web`.
- Le port hôte doit être `8082`.

## Proof
- `curl -I http://localhost:8082` retourne 200/301/302 attendu selon image.
- `podman logs lab02-web` affiche des accès.
- `podman inspect lab02-web` montre le mapping `8082->...`.

## Cleanup
- stop/rm container
