# SLI, SLO e SLA (SRE)

## Definições
- **SLI (Service Level Indicator):** métrica que mede a saúde percebida pelo usuário.
  - Exemplos: disponibilidade de requests, latência p95, taxa de erro.
- **SLO (Service Level Objective):** alvo para um SLI em um período.
  - Ex.: 99.9% de requests bem-sucedidos em 30 dias.
- **SLA (Service Level Agreement):** compromisso contratual (externo) com penalidades.
  - Normalmente baseado em SLOs, mas com linguagem e termos jurídicos.

## SLIs recomendados (comece simples)
### Availability (sucesso de request)
- SLI: % de requests 2xx/3xx (ou “não-erro”) sobre total de requests
- Atenção: defina o que conta como “sucesso” (ex.: 2xx/3xx, ou 2xx apenas)

### Latency
- SLI: latência p95 e p99
- Por que: média esconde cauda longa.

### Errors
- SLI: taxa de 5xx, timeouts, falhas de dependência.

### Saturation
- SLI: CPU/mem/IO/filas/conexões próximas do limite.
- Saturation é “leading indicator” de incidentes.

## Como definir um SLO prático
1) Escolha 1 SLI principal (sucesso ou latência)
2) Defina o período (7d, 30d)
3) Comece com um alvo realista e evolua
4) Use o erro budget para governar mudanças

## Exemplo (API)
- SLI: % requests bem-sucedidos
- SLO: 99.9% em 30 dias
- Observabilidade: dashboard com requests totais, sucesso, p95/p99 e 5xx

## Anti-padrões
- Alertar em SLI que não representa usuário
- SLO “perfeito” sem capacidade de sustentação
- Alertas em “média” (use p95/p99)