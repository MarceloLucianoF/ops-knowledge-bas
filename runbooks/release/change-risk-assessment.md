# Change Risk Assessment

## Classificação rápida
### Baixo risco
- Mudança interna sem impacto
- Feature flag off por padrão
- Sem alterações de schema/infra

### Médio risco
- Mudança com impacto em caminho crítico
- Novo endpoint
- Ajuste em configuração

### Alto risco
- DB migrations
- Mudança de rede/VPN/Firewall
- Alterações em auth
- Mudanças sem rollback simples

## Mitigações
- Canary/Blue-Green
- Rollback definido e testado
- Janela de manutenção
- Observabilidade reforçada