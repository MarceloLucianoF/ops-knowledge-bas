# GitOps (conceitos)

## Definição
Git é a fonte da verdade para o estado desejado do sistema.
O cluster/infra converge automaticamente para o que está no Git.

## Benefícios
- Auditoria (histórico de mudanças)
- Reprodutibilidade
- Rollback via Git
- Menos mudanças manuais

## Práticas
- Pull-based deploy (controller puxa do Git)
- PRs para mudanças
- Aprovações (policies)
- Separar repositórios:
  - app repo (código)
  - env repo (manifests/helm/kustomize)

## Anti-padrões
- Aplicar mudanças direto no cluster sem registrar no Git
- “Config drift” não monitorado