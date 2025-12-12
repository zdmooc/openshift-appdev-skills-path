
# LAB07 — Compose : stack web + api + db

## Objectif
Avoir un “mini-système” complet sur ton poste.

## Tâches
1) Créer un fichier `compose.yml` avec 3 services :
   - `db` (avec volume persistant)
   - `api` (dépend de db)
   - `web` (reverse proxy ou front)
2) Définir un réseau interne.
3) Exposer uniquement `web` vers l’hôte (ex: 8087).
4) Ajouter un script d’init DB (si applicable).
5) Démarrer, tester bout-en-bout, puis arrêter.

## Proof
- `curl http://localhost:8087` renvoie un contenu cohérent
- `podman ps` montre les 3 containers
- les logs montrent le démarrage ordonné

## Cleanup
- down + suppression volumes selon objectif
