# Rollback Strategy

## Quando rollback é preferível
- Aumento de 5xx/timeouts
- Latência p95/p99 degradando
- Falhas em dependências críticas após deploy
- Erros que afetam usuários

## Regras
- Rollback deve ser simples e rápido (runbook)
- Não “debugar em prod” se usuários estão sofrendo
- Mitigar primeiro, investigar depois

## Técnicas
- Voltar para tag anterior (imagem/artefato)
- Reverter commit (se apropriado)
- Desativar feature flag
- Trocar tráfego (blue/green)