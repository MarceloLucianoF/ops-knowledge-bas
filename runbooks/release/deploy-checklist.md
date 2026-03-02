# Deploy Checklist (pré e pós)

## Pré-deploy
- [ ] Mudança aprovada via PR
- [ ] Pipeline verde (tests/build)
- [ ] Observabilidade pronta (dashboards/alerts)
- [ ] Rollback definido (tag anterior)
- [ ] Janela de mudança e comunicação alinhadas
- [ ] Backups (se mexer em DB)

## Deploy
- [ ] Deploy em staging
- [ ] Smoke tests
- [ ] Deploy em produção (rolling/canary/blue-green)
- [ ] Monitorar p95/p99, 5xx, saturação

## Pós-deploy
- [ ] Verificação de saúde do serviço
- [ ] Registrar release notes
- [ ] Se degradação: executar rollback-runbook