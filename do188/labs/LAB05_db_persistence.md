
# LAB05 — DB persistence

## Objectif
Démontrer qu’une base en container persiste ses données après suppression du container.

## Tâches
1) Créer un volume `lab05-db-data`.
2) Démarrer une base `lab05-db` avec ce volume.
3) Créer une table + insérer 3 lignes.
4) Stop + rm le container.
5) Relancer un nouveau container en réutilisant le même volume.
6) Vérifier que les données sont toujours là.

## Proof
- Capture des requêtes/commandes + résultat (3 lignes présentes après relance).

## Pièges
- UID/GID et droits rootless
- Mauvais chemin mounté

## Cleanup
- Supprimer container + volume si tu veux repartir de zéro.
