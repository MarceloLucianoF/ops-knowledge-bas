# Alert Runbook — Padrão

Use este padrão para qualquer alerta.

## Campos obrigatórios
- **Nome do alerta:**
- **Severidade:** (SEV1/2/3/4)
- **Impacto esperado:**
- **Sinais associados:** (Golden Signals)
- **Dashboards:**
- **Logs:**
- **Runbook de mitigação:**

## Fluxo de resposta (rápido)
1) Confirmar impacto (usuário/serviço)
2) Checar dashboards (latência, erro, saturação)
3) Identificar mudança recente (deploy/config)
4) Mitigar (rollback/scale/restart)
5) Comunicar status
6) Registrar timeline (para postmortem)

## Exemplos de ações seguras
- Escalar horizontalmente (quando aplicável)
- Rollback do último deploy
- Restart controlado do serviço
- Desabilitar feature não crítica (feature flag)

## Pós-incidente
- Registrar causa
- Ação corretiva (curto prazo)
- Ação preventiva (médio prazo)
- Ajustar alertas e SLOs se necessário