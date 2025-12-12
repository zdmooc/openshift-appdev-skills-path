
# Podman — Cheat sheet (EX188-ready)

## Images
- Lister : `podman images`
- Pull : `podman pull IMAGE[:TAG]`
- Pull par digest : `podman pull IMAGE@sha256:...`
- Tag : `podman tag SRC DST`
- Push : `podman push DST`
- Inspect image : `podman image inspect IMAGE`
- History : `podman history IMAGE`

## Containers
- Run : `podman run --name NAME -d -p 8080:8080 -e KEY=VAL IMAGE`
- PS : `podman ps -a`
- Logs : `podman logs -f NAME`
- Exec : `podman exec -it NAME /bin/sh`
- Inspect : `podman inspect NAME`
- Stop/Rm : `podman stop NAME && podman rm NAME`
- Stats : `podman stats`
- Events : `podman events --since 10m`

## Volumes / mounts
- Volume : `podman volume create data`
- Run avec volume : `-v data:/var/lib/...`
- Bind mount : `-v $PWD/conf:/etc/app:Z` (SELinux selon OS)

## Compose
- Up : `podman-compose up -d` (selon installation)
- Down : `podman-compose down -v`
