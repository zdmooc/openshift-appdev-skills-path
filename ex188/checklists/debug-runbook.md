
# Runbook Debug (EX188/EX288)

## 0. Observer sans toucher
- `podman ps -a` / `oc get pods`
- regarder **STATUS**, **RESTARTS**, **EXIT CODE**

## 1. Logs
- `podman logs NAME`
- `oc logs POD` (+ `-c` si multi-container)

## 2. Inspect / Describe
- `podman inspect NAME`
- `oc describe pod POD`
- Vérifier : ports, env, mounts, image, cmd, probes

## 3. Accès
- `curl` / `oc port-forward` / route
- vérifier DNS/service/route

## 4. Entrer dans le runtime
- `podman exec -it NAME sh`
- `oc rsh POD` (si autorisé)
- vérifier fichiers, process, config

## 5. Corriger le minimum
- changer un paramètre (env, port, mount) puis re-test

## 6. Preuve
- commande de validation + résultat (HTTP 200, process OK, logs OK)
