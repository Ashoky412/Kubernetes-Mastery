# Kubernetes Deployment Cheat Sheet

| Command | Description |
|---------|-------------|
| `kubectl apply -f` | Apply a deployment YAML |
| `kubectl get deployments` | List deployments |
| `kubectl describe deployment <name>` | Show detailed info |
| `kubectl rollout status deployment <name>` | Monitor rollout progress |
| `kubectl rollout undo deployment <name>` | Rollback deployment |
| `kubectl rollout history deployment <name>` | View deployment history |

### Strategies
- **RollingUpdate**: Gradual, no downtime.
- **Recreate**: Stops old pods, then starts new.

### Tips
- Use `maxSurge` and `maxUnavailable` to control rollout speed.
- Monitor pods via `kubectl get pods` and `kubectl describe pods`.