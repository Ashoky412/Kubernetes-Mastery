# Kubernetes Deployment Labs

## Contents
- Basic Deployment
- Rolling Update Strategy
- Recreate Strategy
- Failure Simulation
- Canary Deployment
- Blue-Green Deployment

## Usage
```bash
kubectl apply -f <file>.yaml
kubectl rollout status deployment <deployment-name>
kubectl rollout undo deployment <deployment-name>
kubectl get deployments
```

## Failure Simulation
Deploy `04-failure-simulation.yaml` to trigger ImagePullBackoff. Then inspect with:
```bash
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```