
# M06 — Troubleshooting & debug

## Objectifs
- Résoudre rapidement : port, env, volume, permission, image incorrecte
- Utiliser logs + inspect + exec comme trépied de diagnostic

## Scénarios à maîtriser
1) Le container quitte immédiatement (exit 1)
2) Le service ne répond pas (port / bind / firewall)
3) La config n’est pas lue (ENV/volume)
4) Permissions volume (rootless)
5) Dépendance externe (DB) non prête

## Runbook (ordre recommandé)
- Voir `ex188/checklists/debug-runbook.md` (réutilisable EX288).
