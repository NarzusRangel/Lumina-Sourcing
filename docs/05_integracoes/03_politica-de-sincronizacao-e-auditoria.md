---
title: "Política de Sincronização e Auditoria"
doc_id: "PFW-05-004"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/05_integracoes/02_eventos-campos-e-mapeamentos.md"
---

# Política de Sincronização e Auditoria

## Regras gerais
- Toda escrita deve registrar data, origem da ação e tipo de evento.
- Atualizações devem ser idempotentes quando possível.
- Falhas de sincronização não podem ser silenciosas.
- Alterações manuais relevantes precisam ser distinguíveis das automáticas.

## Política inicial
- Sincronização sob demanda nas fases de registro.
- Log local mínimo em `docs/memory/export-mcp/` para depuração ou auditoria documental.
- Revisão humana para campos críticos antes da automação total.
