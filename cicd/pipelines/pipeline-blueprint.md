# Pipeline Blueprint (CI/CD)

Blueprint genérico para pipelines robustos.

## Objetivos
- Feedback rápido (fail fast)
- Segurança por padrão
- Reprodutibilidade
- Deploys confiáveis e reversíveis

## Etapas recomendadas
1) **Checkout**
2) **Lint / Format**
3) **Unit Tests**
4) **Build**
5) **SAST (Static Analysis)** (opcional, mas recomendado)
6) **SBOM / Dependency Scan** (opcional)
7) **Artifact Publish**
8) **Deploy to Staging**
9) **Smoke Tests**
10) **Deploy to Production**
11) **Post-deploy Verification**

## Princípios
- Mesmo artefato em staging e produção
- Nada de “deploy manual sem rastreio”
- Logs/metrics para validar pós-deploy
- Rollback sempre documentado