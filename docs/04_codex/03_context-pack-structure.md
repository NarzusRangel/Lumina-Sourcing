---
title: "Context Pack Structure"
doc_id: "PFW-04-004"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/context/"
---

# Context Pack Structure

## Tipos de pack
- `operacao/triagem`: taxonomia, contexto mínimo e regras de enquadramento.
- `operacao/pesquisa`: critérios de busca, classificação de evidência e formato de shortlist.
- `operacao/registro`: contrato de campos e eventos para criação/atualização.
- `dominio/*`: contexto por linha de produto ou segmento, quando aprovado.

## Regras
- Carregar apenas o pack necessário para a fase atual.
- Packs devem apontar para documentos-fonte, não replicar tudo.
- Contexto volátil do caso não deve ser salvo como referência estável.
