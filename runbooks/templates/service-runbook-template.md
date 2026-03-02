# Runbook — <Service Name>

## Visão geral
- Responsabilidade:
- Criticidade:
- Dependências:
- Dono/Time:

## SLOs / Indicadores
- Latência p95:
- Taxa de erros:
- Saturação (CPU/Mem/IO):
- Disponibilidade:

## Dashboards e logs
- Métricas:
- Logs:
- Alertas:

## Deploy / Mudanças
- Como fazer rollback:
- Feature flags:
- Janela de mudança:

## Troubleshooting por sintoma
### Sintoma: latência alta
- Verificar saturação (CPU/mem/disk IO)
- Verificar DB/filas
- Verificar erros/timeouts

### Sintoma: aumento de 5xx/timeouts
- Verificar logs
- Verificar DNS/rede
- Verificar conexões DB

## Ações seguras
- Restart seguro:
- Scale out:
- Desativar funcionalidade não crítica: