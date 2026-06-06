# Risk-Based Testing

Priorizamos esforços de teste pelo **impacto e probabilidade de falha**,
não cobrindo 100% das funcionalidades de forma igual.

## Matriz de Risco

```
Prioridade = Probabilidade (1–5) × Impacto ao Negócio (1–5)
```

| Score | Prioridade | Ação |
|---|---|---|
| 15–25 | 🔴 Crítica | Automatizar + teste manual toda sprint |
| 8–14 | 🟡 Alta | Automatizar fluxo principal |
| 3–7 | 🟢 Média | Testar manualmente nas sprints relevantes |
| 1–2 | ⚪ Baixa | Apenas em releases maiores |

## Exemplo Aplicado

| Funcionalidade | Prob. | Impacto | Score | Prioridade |
|---|---|---|---|---|
| Checkout / Pagamento | 3 | 5 | 15 | 🔴 Crítica |
| Login com OAuth | 4 | 4 | 16 | 🔴 Crítica |
| Busca de produtos | 3 | 4 | 12 | 🟡 Alta |
| Editar perfil | 2 | 2 | 4 | 🟢 Média |
| Mudar tema de cor | 1 | 1 | 1 | ⚪ Baixa |

## Revisão da Matriz

Revisar a cada sprint planning, após incidentes em produção
e quando houver mudança arquitetural significativa.