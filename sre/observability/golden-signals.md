# Golden Signals (SRE)

Os 4 sinais principais para detectar degradação antes de virar incidente:

## 1) Latency
- Tempo de resposta (p95/p99) é mais relevante que média.
- Pergunta-chave: “está mais lento do que o normal?”

## 2) Traffic
- Taxa de requisições, throughput, conexões.
- Pergunta-chave: “o volume mudou drasticamente?”

## 3) Errors
- 4xx/5xx, timeouts, falhas de autenticação, retries.
- Pergunta-chave: “o sistema está falhando mais?”

## 4) Saturation
- CPU, memória, I/O, disco, conexões, filas.
- Pergunta-chave: “estamos próximos do limite?”

## Recomendação prática
Comece simples: logs + métricas básicas + alertas de saturação.
Depois evolua para SLOs e alertas por erro/latência.