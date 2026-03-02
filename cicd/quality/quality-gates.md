# Quality Gates

## Gate mínimo (começo)
- Lint/format passando
- Unit tests passando
- Build reproduzível
- Sem secrets no código

## Gate recomendado (maturidade)
- Coverage mínimo (ex.: 70% unit)
- SAST (ex.: sem falhas críticas)
- Dependency scanning (sem CVE crítico)
- Smoke tests em staging antes de prod

## Antipadrões
- Merge direto em main sem checks
- Deploy sem artifact versionado
- Testar “na produção”