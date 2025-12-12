
# Capstone — Fil rouge DO288 → EX288

## But
Construire une application “réaliste” (web + api + db optionnelle) et la livrer de 3 façons :
- Template
- Helm
- Kustomize
… puis automatiser via Tekton.

## Livrables
- `apps/` : code minimal + Containerfile
- `openshift/` :
  - `templates/`
  - `helm/`
  - `kustomize/`
- `pipelines/` : Tekton (Task/Pipeline)
- `runbooks/` : debug + exploit + cleanup
