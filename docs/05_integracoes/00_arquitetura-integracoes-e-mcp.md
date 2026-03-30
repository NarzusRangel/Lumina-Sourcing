---
title: "Arquitetura Integrações e MCP"
doc_id: "PFW-05-001"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/00_fundacao/00_visao-geral-do-sistema.md"
---

# Arquitetura Integrações e MCP

## Objetivo
Preparar a camada de integrações para leitura e escrita operacional sem acoplar a regra do sistema ao banco.

## Princípios
- Integração é adaptador, não fonte normativa.
- Só registrar o que terá valor de operação, auditoria ou melhoria.
- Eventos e campos precisam de contrato explícito antes da automação.
- Atualizações devem preservar histórico e autoria.

## Casos previstos
- Criar solicitação de pesquisa.
- Atualizar status de pesquisa.
- Registrar shortlist consolidada.
- Atualizar fornecedor, evidência ou observação operacional.
