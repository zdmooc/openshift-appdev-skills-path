
# M02 — Podman basics (run/exec/logs/inspect)

## Objectifs
- Lancer des containers en mode détaché, exposer des ports
- Injecter des variables, monter un volume
- Debug rapide via `logs`, `exec`, `inspect`, `events`

## Pattern “debug en 90 secondes”
1) `podman ps -a` (statut / exit code)
2) `podman logs NAME` (erreur applicative)
3) `podman inspect NAME` (cmd, env, ports, mounts)
4) `podman exec -it NAME sh` (si le container tourne)
5) `podman events --since 5m` (erreurs runtime)

## Lab guidé
Voir `do188/labs/LAB02_podman_runtime.md`.
