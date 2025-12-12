# Mock EX288 — Sujet blanc 03 (3h)

## Objectif global
Déployer une application sur OpenShift **avec preuves objectives**, en utilisant au minimum :
- projets multiples
- build (BuildConfig/S2I) + registry interne
- imagestream + trigger
- configmap + secret
- health checks (readiness/liveness)
- packaging (Helm ou Kustomize) selon partie
- pipeline Tekton (partie finale)

## Setup (5 min)
- Créer projets : `mock03-dev` et `mock03-prod`
- Labeler les projets et noter les noms.

## Partie A — Déploiement simple (30 min)
1) Déployer une app depuis image dans `mock03-dev`
2) Exposer Service + Route
3) Ajouter une variable d’environnement
**Proof** : route répond + logs ok

## Partie B — Build + ImageStream (45 min)
4) Créer un BuildConfig (Docker/Containerfile ou S2I)
5) Lancer un build et publier dans registry interne
6) Créer/valider un ImageStreamTag
7) Déployer depuis l’ImageStreamTag
**Proof** : build complete + is tag + route ok

## Partie C — ConfigMaps/Secrets + Probes (30 min)
8) Injecter une ConfigMap (fichier ou env)
9) Injecter un Secret (env ou mount)
10) Ajouter readiness & liveness probes (port correct)
**Proof** : pod Ready + pas de restart

## Partie D — Multi-container packaging (40 min)
11) Packager une app multi-container :
    - Option 1 : Helm chart (values dev/prod)
    - Option 2 : Kustomize (base + overlays)
12) Déployer dans `mock03-prod`
**Proof** : rendu manifest ok + déploiement ok

## Partie E — Pipelines Tekton (35 min)
13) Définir un Pipeline (build→test→deploy)
14) Exécuter un PipelineRun
15) Diagnostiquer une erreur volontaire (ex: param manquant), puis corriger
**Proof** : PipelineRun succeed + route prod OK

## Barème (auto)
- A 15, B 25, C 20, D 20, E 20
