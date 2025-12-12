
# Mock EX188 — Sujet blanc 01 (2h30)

## Contexte
Tu dois containeriser et opérer une petite application web et une base, en respectant des contraintes de nommage, ports et persistance.

## Ressources
- Un dossier `app/` (à créer) contenant un site statique minimal (index.html).
- Une image de base web (au choix).

## Tâches
### Partie A — Image & Containerfile (40 min)
1) Créer `app/index.html` avec un texte “EX188 Mock01 OK”.
2) Écrire un `Containerfile` pour builder une image `mock01-web:1.0` :
   - utilisateur non-root
   - WORKDIR `/opt/app`
   - exposer le port `8080`
   - commande de démarrage déterministe
3) Builder l’image.

**Proof**
- `podman image inspect mock01-web:1.0` (USER/WORKDIR/EXPOSE cohérents)

### Partie B — Exécution & debug (25 min)
4) Lancer un container `mock01-web` sur le port hôte `8088`.
5) Vérifier HTTP 200.
6) Récupérer logs et prouver que la requête apparaît.

**Proof**
- `curl -I http://localhost:8088`
- `podman logs mock01-web`

### Partie C — Registry & tags/digests (25 min)
7) Tagger l’image pour une registry de test (ex: `registry.local/mock01-web:1.0`).
8) Pousser l’image (si tu as une registry), sinon simuler via “sauvegarde image” :
   - sauvegarder l’image **avec layers** (archive)
9) Documenter la différence “backup image” vs “backup container state”.

**Proof**
- Archive image présente (et command lines dans ton fichier Proof)

### Partie D — Persistance (35 min)
10) Démarrer une DB container (au choix) `mock01-db` avec volume `mock01-db-data`.
11) Créer une table et insérer 3 lignes.
12) Supprimer le container DB et le recréer en réutilisant le volume.
13) Vérifier que les 3 lignes sont toujours présentes.

**Proof**
- preuve des 3 lignes après relance

### Partie E — Multi-container (25 min)
14) Créer un `compose.yml` qui démarre `web + db` :
   - DB persistante
   - web exposée sur 8088
15) `up`, test, `down` (avec ou sans volume selon consigne)

## Barème (auto-évaluation)
- A : image conforme (25)
- B : service accessible + logs (20)
- C : registry/backup correct (15)
- D : persistance prouvée (25)
- E : compose ok (15)
