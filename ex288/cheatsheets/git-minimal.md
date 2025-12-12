
# Git minimal pour EX288

## Lire/inspecter un repo
- `git clone URL`
- `git status`
- `git log --oneline -n 10`
- `git branch -a`
- `git rev-parse HEAD`

## Basculer sur une branche / tag
- `git checkout <branch>`
- `git checkout <tag>`

## Diagnostiquer “ça ne build pas”
- vérifier le chemin du Containerfile/Dockerfile
- vérifier la présence de manifest (`package.json`, `pom.xml`, etc.)
