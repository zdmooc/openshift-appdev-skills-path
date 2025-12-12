
# M05 — Déploiements & health checks

## Objectifs
- Ajouter readiness/liveness probes pertinentes
- Surveiller un rollout, diagnostiquer un crashloop
- Expliquer la différence readiness vs liveness

## Scénarios
- Readiness trop stricte : app jamais “Ready”
- Liveness trop agressive : redémarrages
- Mauvais port de probe

## Proof
- `oc get deploy`
- `oc describe pod` montre probes
