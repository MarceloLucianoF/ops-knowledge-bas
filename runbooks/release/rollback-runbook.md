# Rollback Runbook

## Quando executar
- Erros/latência aumentam após deploy
- Falhas em smoke checks
- Reclamações e impacto em usuários

## Passos
1) Confirmar impacto nos dashboards (errors/latency)
2) Identificar versão atual e versão estável anterior
3) Executar rollback para tag anterior
4) Validar recuperação (p95/p99, 5xx, sucesso)
5) Comunicar status e registrar timeline
6) Abrir postmortem (blameless) se SEV1/SEV2

## Pós
- Capturar logs e métricas relevantes (sem dados sensíveis)
- Criar ação corretiva e preventiva