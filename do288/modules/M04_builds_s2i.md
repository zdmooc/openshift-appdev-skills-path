
# M04 — Builds (BuildConfig / S2I / custom builder)

## Objectifs
- Créer des builds reproductibles
- Comprendre BuildConfig : sources, strategy, triggers
- S2I : builder existant + customisation

## Exercices
- un build Docker/Containerfile
- un build S2I
- un trigger sur changement (Git ou ImageStream)

## Proof
- `oc get bc`
- `oc logs -f build/...`
