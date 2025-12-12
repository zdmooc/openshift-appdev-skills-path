
# M01 — Containers fundamentals (modèle mental)

## Objectifs
- Expliquer : image vs container, layers, tags vs digests, registry
- Comprendre : isolation (namespaces), ressources (cgroups), rootless
- Savoir raisonner “build → run → observe → debug → ship”

## Notions essentielles
- **Image** : artefact immuable (layers + metadata). Tag = alias, Digest = identité.
- **Container** : instance runtime (process + FS union + config + mounts).
- **Rootless** : réduit surface d’attaque, mais impose contraintes (ports <1024, permissions, mounts).
- **Reproductibilité** : containerisation ≠ “ça marche une fois”, mais “ça marche à chaque build”.

## Exercice (15 min)
1) Choisir une image web (nginx ou équivalent).
2) Lancer, inspecter, récupérer logs, stopper/supprimer.
3) Noter les éléments *non évidents* (ports, user, cmd).

## Proof (attendu)
- `podman ps -a` montre l’état
- `podman inspect` montre ports/env/cmd
- `curl http://localhost:PORT` retourne 200
