# Flux CD (visão geral)

Flux é uma alternativa GitOps para Kubernetes.

## Ideia central
- Controllers aplicam manifests do Git no cluster
- Suporta Helm e Kustomize

## Boas práticas
- Separar apps e environments
- Imagem automatizada (image update controllers) com governança
- Alertas para drift e falhas de sync