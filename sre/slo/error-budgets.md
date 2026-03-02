# Error Budgets (Orçamento de Erro)

## O que é
O **error budget** é a quantidade de falha permitida antes de violar um SLO.
Ele cria um trade-off saudável entre **velocidade de entrega** e **confiabilidade**.

## Exemplo (30 dias)
SLO: 99.9% de sucesso

- Total permitido de erro: 0.1%
- Em 30 dias (~43.200 minutos):
  - 0.1% = 43.2 minutos de indisponibilidade "aceitável"

## Como usar na prática
- Se o erro budget está saudável:
  - mudanças podem seguir normalmente (feature, deploy, refactor)
- Se o erro budget está “queimando” rápido:
  - reduzir mudanças
  - priorizar correções e estabilidade
- Se o erro budget foi estourado:
  - congelar deploys não críticos
  - foco total em confiabilidade (hardening, capacity, performance)

## Políticas simples (maturidade inicial)
- Budget > 60% restante: OK para mudanças
- Budget entre 30–60%: mudanças com cautela + validações extras
- Budget < 30%: reduzir mudanças e atacar causas
- Budget estourado: freeze de deploys não essenciais

## Benefícios
- Evita debates subjetivos (“deploy pode ou não pode?”)
- Conecta SRE e produto com dados
- Reduz incidentes por pressão de release