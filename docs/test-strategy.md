# Estratégia de Testes

## Contexto
Produto web com entregas ágeis (sprints de 2 semanas) e time de 2–4 QAs.

## Pirâmide de Testes

```
         /\
        /E2E\          10% — fluxos críticos de negócio
       /------\
      /  Integr \      20% — contratos de API e banco
     /------------\
    /   Unitários  \   70% — responsabilidade dos devs
   /________________\
```

| Camada | Responsável | Ferramenta | Frequência |
|---|---|---|---|
| Unitários | Dev | Jest / Vitest | A cada commit |
| Integração | Dev + QA | Playwright API / Newman | A cada PR |
| E2E | QA | Playwright | Diário + pré-release |
| Exploratório | QA | Manual | Toda sprint |

## Ambientes

| Ambiente | Propósito | Dados |
|---|---|---|
| Local | Desenvolvimento | Mock |
| QA | Testes funcionais | Sintéticos |
| Homologação | Validação UAT | Anonimizados |
| Produção | Smoke test pós-deploy | Reais (somente leitura) |

## Métricas Acompanhadas

- **Defect Escape Rate** — meta: < 2% de bugs chegando à produção
- **Test Pass Rate** — meta: > 95% na suite de regressão
- **Automation Rate** — meta: > 70% dos casos críticos automatizados
- **Flaky Test Rate** — meta: < 3% de testes instáveis
- **MTTR** — Críticos < 4h, Altos < 24h