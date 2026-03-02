# Filosofia de Alertas (SRE)

## Objetivo
Alertas devem:
- Acordar alguém apenas quando há ação imediata necessária
- Reduzir ruído (alert fatigue)
- Ser orientados ao usuário (impacto real)

## Regras práticas
- **Páginas (pager):** apenas quando o usuário está impactado ou prestes a ser.
- **Tickets:** problemas que podem esperar (capacidade, warnings).
- Alertar em **sintomas**, não em causas (causas variam; sintomas são consistentes).

## Anti-padrões
- Alertas em CPU alta isolada sem impacto
- Alertas sem runbook
- Alertas sem dono
- Alertas que disparam sempre e ninguém corrige

## Golden Signals como base
- Latency, Traffic, Errors, Saturation

## “Alertas bons” normalmente têm
- Condição clara
- Severidade
- Ação sugerida
- Link para dashboard e runbook