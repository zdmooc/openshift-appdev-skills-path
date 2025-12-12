
# LAB04 — Containerfile : builder une webapp “propre”

## Objectif
Produire une image custom `lab04-app:1.0` avec :
- utilisateur non-root
- WORKDIR explicite
- port exposé
- commande de démarrage déterministe

## Tâches
1) Créer un répertoire `app/` avec une mini app (ex: static web).
2) Écrire un `Containerfile`.
3) Builder l’image `lab04-app:1.0`.
4) Lancer `lab04-app` sur `8084`.
5) Ajouter une variable d’environnement (ex: `APP_GREETING`) et vérifier qu’elle est lue.

## Proof
- `podman run ...` démarre et `curl` répond.
- `podman inspect` montre l’utilisateur non-root.
- `podman history` montre une construction cohérente.

## Bonus (optionnel)
- Ajouter un label (ex: `org.opencontainers.image.source`).
