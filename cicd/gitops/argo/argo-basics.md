# Argo CD (visão geral)

Argo CD é um controlador GitOps comum em Kubernetes.

## Ideia central
- Observa um repositório com manifests/Helm/Kustomize
- Sincroniza o cluster com o estado desejado no Git

## Práticas recomendadas
- Apps por serviço e por ambiente
- Sync policies (manual/auto)
- Health checks e waves (ordem de deploy)
- RBAC e approvals via PR