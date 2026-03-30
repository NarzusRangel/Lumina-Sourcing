---
title: "Critérios de Qualidade"
doc_id: "PFW-02-002"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/02_qualidade/00_padrao-de-resposta.md"
---

# Critérios de Qualidade

| Critério | Definição | Evidência esperada | Nível mínimo aceitável | Falhas típicas |
|---|---|---|---|---|
| Clareza | resposta é fácil de entender e usar | estrutura estável e linguagem objetiva | usuário sabe o próximo passo | excesso de texto ou ambiguidade |
| Aderência ao escopo | resposta respeita limites do sistema | ausência de extrapolações indevidas | não há decisão fora de escopo | parecer aprovador ou regulatório |
| Rastreabilidade | o usuário entende o que está confirmado e o que é hipótese | marcação explícita de evidência e lacunas | partes críticas estão qualificadas | mistura entre fato e inferência |
| Utilidade operacional | saída serve para agir ou registrar | formato reaproveitável | há ação ou registro possível | resposta correta porém inútil |
| Completude mínima | inclui os elementos exigidos pela classe de demanda | campos essenciais preenchidos | não há lacunas silenciosas | ausência de região, contexto ou próximo passo |

## Severidade
- Bloqueante: extrapolação, invenção de dados, falta de evidência crítica.
- Média: inconsistência de formato ou ausência de contexto não crítico.
- Baixa: melhoria de clareza, ordem ou concisão.
