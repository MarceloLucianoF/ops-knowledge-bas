# Severidade de Incidente (SEV)

Classificação simples e corporativa.

## SEV1 — Crítico
- Impacto amplo ou sistema principal fora.
- Ex.: indisponibilidade total, perda de dados, falha de autenticação global.
**Ação:** war room imediato + updates frequentes.

## SEV2 — Alto
- Impacto relevante, mas há mitigação parcial.
- Ex.: degradação severa, falhas intermitentes, fila crescendo rápido.
**Ação:** resposta rápida + coordenação.

## SEV3 — Médio
- Impacto limitado / parcial.
- Ex.: falha em funcionalidade secundária, erros em subset.
**Ação:** tratar com prioridade, sem war room.

## SEV4 — Baixo
- Incidente pequeno / inconveniente.
- Ex.: bug menor, alerta falso, ajuste operacional.
**Ação:** backlog com triagem.

## Princípios
- Melhor “elevar severidade” cedo do que tarde.
- Rebaixar após mitigação confirmada.