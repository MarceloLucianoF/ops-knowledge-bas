# Estratégias de Release

## Rolling
Atualiza gradualmente instâncias.
- Pró: simples
- Contra: rollback pode ser lento

## Blue/Green
Dois ambientes (blue e green). Troca de tráfego.
- Pró: rollback rápido
- Contra: custo maior

## Canary
Pequena % do tráfego recebe a versão nova.
- Pró: reduz blast radius
- Contra: exige observabilidade e controle de tráfego

## Feature Flags
Desacopla deploy de release.
- Pró: liga/desliga rapidamente
- Contra: precisa governança e limpeza