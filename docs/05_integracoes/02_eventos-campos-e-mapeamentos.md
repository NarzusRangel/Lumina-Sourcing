---
title: "Eventos, Campos e Mapeamentos"
doc_id: "PFW-05-003"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/05_integracoes/01_modelo-notion-operacional.md"
---

# Eventos, Campos e Mapeamentos

| Evento | Origem | Destino | Campos mínimos |
|---|---|---|---|
| pesquisa_iniciada | fase de triagem/contexto | Solicitações de Pesquisa | título, solicitante, área, item, prioridade, status |
| pesquisa_concluida | fase de síntese | Resultados de Pesquisa | item, resumo técnico, datasheet, NCM provável, certificações possíveis, shortlist, riscos, data, referência da solicitação |
| fornecedor_identificado | fase de qualificação | Fornecedores | nome, tipo, região, site, observações, marcas representadas, evidência, data |
| contato_preparado | fase de atualização direta ou registro | Contatos de Fornecedores | e-mail, nome, telefone, fornecedor relacionado, marcas relacionadas, origem |
| registro_atualizado | fase de registro | base correspondente | id do registro, campo alterado, valor anterior, valor novo, responsável, autorização do usuário |

## Observações
- Campos finais dependerão da revisão do modelo Notion, mas os eventos de v1 já estão definidos.
- O evento só deve ser emitido quando a saída estiver no nível mínimo de qualidade.
- Eventos de escrita em `Fornecedores` e `Contatos de Fornecedores` exigem autorização explícita do usuário.
