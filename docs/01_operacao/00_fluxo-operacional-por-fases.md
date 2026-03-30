---
title: "Fluxo Operacional por Fases"
doc_id: "PFW-01-001"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/00_fundacao/03_taxonomia-de-demandas.md"
---

# Fluxo Operacional por Fases

| Fase | Objetivo | Entrada mínima | Ação do agente | Critério de decisão | Saída | Próxima fase |
|---|---|---|---|---|---|---|
| 1. Triagem | enquadrar a demanda | objetivo, item, urgência | classificar pedido e checar dados faltantes | demanda cabe na taxonomia? | enquadramento + lacunas | 2 |
| 2. Contextualização | consolidar o caso | especificação, contexto comercial, restrições, observações | resumir insumos, identificar fabricante e delimitar escopo | há base suficiente para seguir? | resumo validado do caso | 3 |
| 3. Análise Técnica Inicial | compreender o item antes da busca | caso contextualizado | explicar tecnicamente o item, tentar datasheet fácil, indicar NCM provável e certificações possíveis | há leitura mínima para orientar a pesquisa? | análise técnica curta + insumos de pesquisa | 4 |
| 4. Pesquisa Profunda | localizar e ampliar evidência de mercado | análise técnica inicial | buscar fabricante, distribuidores e revendedores qualificados com prioridade por distribuidores | há evidência mínima confiável para compor a recomendação? | shortlist bruta | 5 |
| 5. Qualificação | separar sinal de ruído | shortlist bruta | avaliar aderência, risco, qualidade do fornecedor e composição ideal da lista | resultado atinge o padrão mínimo da shortlist? | shortlist qualificada com até 9 recomendações | 6 |
| 6. Síntese | entregar saída útil | shortlist qualificada | formatar resposta com análise técnica, datasheet opcional, NCM, certificações possíveis e fornecedores | resposta está clara, acionável e dentro do contrato? | resposta final | 7 |
| 7. Registro | preservar memória operacional | resposta final ou dados enviados pelo usuário para cadastro/atualização | preparar ou executar registro em memória/Notion apenas após autorização explícita | há comando explícito e dados mínimos para gravar? | log ou payload de atualização | encerramento |

## Regras operacionais
- O agente só avança quando a fase atual tiver entrada mínima suficiente.
- Se faltarem dados críticos, o agente deve pedir apenas o necessário para desbloquear a próxima fase.
- Toda fase deve deixar explícito o que é confirmado, inferido ou pendente.
- A especialização principal do sistema está em Oil & Gas e MRO, mas a pesquisa não deve bloquear itens atípicos ou serviços.
- A análise técnica inicial é obrigatória antes da pesquisa profunda quando a demanda for de pesquisa.
- A shortlist padrão deve buscar 9 recomendações no total: fabricante quando identificável e mais 8 recomendações com prioridade para distribuidores.
- Revendedores entram para completar lacunas com limite máximo de 4 quando não houver distribuidores suficientes de alta qualidade.
- A fase de registro só ocorre quando houver utilidade operacional clara e comando explícito do usuário.
- O usuário pode iniciar diretamente na fase de registro quando já trouxer os dados de contato e solicitar cadastro ou atualização no Notion.

## Handoffs previstos
- Para humano comercial: quando houver decisão de prosseguimento, contato ou negociação.
- Para especialista técnico: quando houver risco de compatibilidade ou interpretação regulatória.
- Para curadoria do sistema: quando a taxonomia ou o padrão de resposta não cobrirem o caso.
- Para o próprio usuário: confirmação explícita antes de qualquer gravação em banco operacional.
