
# M05 — Persistance (volumes, bind mounts, permissions)

## Objectifs
- Faire persister une base (ou équivalent) sur redémarrage
- Diagnostiquer les erreurs de permissions en rootless
- Savoir expliquer volume vs bind mount

## Pièges fréquents
- UID/GID attendu par l’image (ex: postgres)
- Bind mount en lecture seule involontaire
- Mauvais chemin / droits insuffisants

## Lab principal
Voir `do188/labs/LAB05_db_persistence.md`.
