# Containerization and Orchestration

> **Section:** 19  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `docker run IMAGE` | Run a container from an image. | Source |  |
| `docker ps` | List running containers. | Source |  |
| `docker ps -a` | List all containers, including stopped ones. | Source |  |
| `docker build -t IMAGE_NAME .` | Build an image from a Dockerfile. | Source |  |
| `docker exec -it CONTAINER_ID bash` | Open an interactive Bash shell inside a running container. | Source |  |
| `docker stop CONTAINER_ID` | Stop a container. | Source |  |
| `docker rm CONTAINER_ID` | Remove a container. | Source |  |
| `docker logs CONTAINER_ID` | View container logs. | Source |  |
| `docker images` | List local images. | Source |  |
| `docker rmi IMAGE_NAME` | Remove an image. | Source |  |
| `docker network ls` | List Docker networks. | Source |  |
| `docker-compose up` | Start a multi-container Compose application. | Source | Legacy standalone syntax; modern Docker uses docker compose. |
| `docker-compose down` | Stop/remove a Compose application. | Source | Legacy standalone syntax; modern Docker uses docker compose. |
| `docker-compose logs` | View Compose logs. | Source | Legacy standalone syntax; modern Docker uses docker compose. |
| `kubectl get pods` | List pods in the current namespace. | Source |  |
| `kubectl get nodes` | List cluster nodes. | Source |  |
| `kubectl get services` | List services. | Source |  |
| `kubectl apply -f FILE.yaml` | Apply declarative Kubernetes configuration. | Source |  |
| `kubectl create -f FILE.yaml` | Create Kubernetes resources from a file. | Source |  |
| `kubectl delete -f FILE.yaml` | Delete resources described by a file. | Source |  |
| `kubectl exec -it POD -- bash` | Execute Bash in a pod. | Source |  |
| `kubectl logs POD` | View pod logs. | Source |  |
| `kubectl describe pod POD` | Show detailed pod information and events. | Source |  |
| `kubectl scale deployment DEPLOYMENT --replicas=N` | Scale a deployment. | Source |  |
| `kubectl rollout restart deployment DEPLOYMENT` | Restart a deployment rollout. | Source |  |
| `kubectl port-forward pod/POD LOCAL:REMOTE` | Forward a pod port to localhost. | Source |  |
| `helm install RELEASE CHART` | Install a Helm chart. | Source |  |
| `helm upgrade RELEASE CHART` | Upgrade a Helm release. | Source |  |
| `helm list` | List Helm releases. | Source |  |
| `helm delete RELEASE` | Delete a Helm release. | Source | helm uninstall is the preferred modern spelling. |
| `helm search repo TERM` | Search configured Helm repositories. | Source |  |
| `docker pull IMAGE` | Pull an image from a registry. | Added |  |
| `docker inspect OBJECT` | Show detailed JSON metadata for a Docker object. | Added |  |
| `docker stats` | Stream container CPU, memory, network and I/O usage. | Added |  |
| `docker system df` | Show Docker disk usage. | Added |  |
| `docker system prune` | Remove unused Docker objects. | Added | Review what will be removed before confirming. |
| `docker volume ls` | List Docker volumes. | Added |  |
| `docker compose up -d` | Start a Compose application in detached mode. | Added |  |
| `docker compose ps` | Show Compose application containers. | Added |  |
| `docker compose logs -f` | Follow Compose logs. | Added |  |
| `docker compose down -v` | Stop Compose services and remove volumes. | Added | Removing volumes can delete persisted application data. |
| `kubectl get pods -A -o wide` | List pods across namespaces with node/IP information. | Added |  |
| `kubectl config get-contexts` | List kubeconfig contexts. | Added |  |
| `kubectl config use-context CONTEXT` | Switch the active Kubernetes context. | Added |  |
| `kubectl get events --sort-by=.metadata.creationTimestamp` | List events chronologically. | Added |  |
| `kubectl logs -f POD` | Follow pod logs. | Added |  |
| `kubectl logs POD --previous` | Show logs from the previous terminated container instance. | Added |  |
| `kubectl exec -it POD -- /bin/sh` | Open a POSIX shell in a pod when Bash is unavailable. | Added |  |
| `kubectl rollout status deployment/DEPLOYMENT` | Wait for and report rollout status. | Added |  |
| `kubectl rollout undo deployment/DEPLOYMENT` | Roll back a deployment to the previous revision. | Added |  |
| `kubectl top pods` | Show pod CPU/memory metrics when metrics-server is available. | Added |  |
| `kubectl diff -f FILE.yaml` | Preview declarative changes before applying. | Added |  |
| `kubectl explain RESOURCE` | Show schema/help for a Kubernetes resource. | Added |  |
| `helm repo add NAME URL` | Add a Helm chart repository. | Added |  |
| `helm repo update` | Refresh chart repository indexes. | Added |  |
| `helm upgrade --install RELEASE CHART` | Install or upgrade a release idempotently. | Added |  |
| `helm status RELEASE` | Show release status. | Added |  |
| `helm history RELEASE` | Show release revisions. | Added |  |
| `helm rollback RELEASE REVISION` | Roll back to a prior revision. | Added |  |
| `helm uninstall RELEASE` | Uninstall a release. | Added |  |
| `helm template RELEASE CHART` | Render chart templates locally without installing. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
