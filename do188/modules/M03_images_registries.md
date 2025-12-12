
# M03 — Images & registries (tags, digests, sécurité)

## Objectifs
- Comprendre tag vs digest (et pourquoi “latest” est un piège)
- Auth registry privée
- Push/pull multi-registries

## Bonnes pratiques
- En prod : **pin digest** (stabilité) + policy de mise à jour maîtrisée
- Garder une stratégie de tags : `1.0.0`, `1.0`, `stable`, `dev-<sha>`
- Documenter : “source image”, “digest”, “date”, “raison”

## Exercices
- Pull par tag puis par digest
- Retag + push vers registry de test
- Vérifier le digest après push

## Proof
- `podman images` + digest
- `podman pull ...@sha256:...` fonctionne
