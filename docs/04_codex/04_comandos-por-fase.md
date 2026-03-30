---
title: "Comandos por Fase"
doc_id: "PFW-04-005"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/01_operacao/00_fluxo-operacional-por-fases.md"
---

# Comandos por Fase

| Fase | Comando proposto | Objetivo | Saída esperada |
|---|---|---|---|
| Triagem | `*fase-triagem` | enquadrar pedido e lacunas | classe da demanda + dados faltantes |
| Contextualização | `*fase-contexto` | consolidar insumos úteis | resumo operacional do caso |
| Análise Técnica Inicial | `*fase-analise` | compreender o item e orientar a busca | análise curta + datasheet opcional + NCM + certificações possíveis |
| Pesquisa Profunda | `*fase-pesquisa` | localizar fornecedores com profundidade e evidência | shortlist bruta priorizada |
| Qualificação | `*fase-qualificacao` | priorizar distribuidores, completar com revendedores e validar composição | shortlist qualificada com 9 fornecedores |
| Síntese | `*fase-sintese` | gerar entrega final da pesquisa | resposta estruturada pronta para uso comercial |
| Registro | `*fase-registro` | preparar criação ou atualização em base sob autorização | payload ou checklist de atualização |
| Atualização Direta | `*fase-atualizacao` | cadastrar ou atualizar contatos enviados pelo usuário sem pesquisa completa | payload estruturado para Notion |

## Contrato resumido dos comandos

### `*fase-triagem`
- Entrada: descrição mínima, região, observações e comandos opcionais.
- Saída: enquadramento da demanda, lacunas e definição do caminho do fluxo.

### `*fase-contexto`
- Entrada: dados já fornecidos pelo usuário.
- Saída: resumo operacional consolidado, incluindo fabricante e part number quando identificáveis.

### `*fase-analise`
- Entrada: caso contextualizado.
- Saída: explicação técnica curta, link de datasheet se fácil, NCM provável e certificações possíveis.

### `*fase-pesquisa`
- Entrada: análise técnica inicial.
- Saída: levantamento bruto de fabricante, distribuidores e revendedores potenciais.

### `*fase-qualificacao`
- Entrada: shortlist bruta.
- Saída: shortlist final com regra de composição, priorizando distribuidores e limitando revendedores.

### `*fase-sintese`
- Entrada: shortlist qualificada.
- Saída: entrega final pronta para uso comercial.

### `*fase-registro`
- Entrada: autorização explícita do usuário e dados mínimos para gravação.
- Saída: payload estruturado de criação ou atualização no Notion.

### `*fase-atualizacao`
- Entrada: e-mails, contatos, marcas representadas e demais dados trazidos pelo usuário.
- Saída: atualização ou cadastro estruturado sem necessidade de pesquisa completa.

## Regra
Os nomes finais dos comandos ainda podem ser refinados na implementação da skill, mas o contrato funcional de cada fase já está definido neste documento.
