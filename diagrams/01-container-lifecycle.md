
# Diagrammes — Cycle de vie container & image

```mermaid
sequenceDiagram
  participant Dev as Dev
  participant Podman as Podman
  participant Reg as Registry
  Dev->>Podman: podman build -t app:1.0 .
  Podman-->>Dev: image id + layers
  Dev->>Podman: podman run -d -p 8080:8080 app:1.0
  Podman-->>Dev: container id
  Dev->>Podman: podman logs / inspect
  Dev->>Podman: podman tag app:1.0 registry.local/app:1.0
  Dev->>Reg: podman push registry.local/app:1.0
  Reg-->>Dev: digest sha256:...
```

```mermaid
flowchart LR
  SRC[Source code] --> CF[Containerfile]
  CF --> BUILD[Build layers]
  BUILD --> IMG[Image (tag/digest)]
  IMG --> RUN[Container runtime]
  RUN --> LOGS[Logs/events/inspect]
  RUN --> VOL[(Volume / Bind mount)]
```
