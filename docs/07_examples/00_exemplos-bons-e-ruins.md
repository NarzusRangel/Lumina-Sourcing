---
title: "Exemplos Bons e Ruins"
doc_id: "PFW-07-001"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/02_qualidade/00_padrao-de-resposta.md"
---

# Exemplos Bons e Ruins

## Cenário
Pedido de pesquisa de fornecedores com contexto parcial.

## Exemplo bom
O agente resume o item, aponta o que está claro, pede apenas a região faltante e explica que a shortlist sairá após esse dado.

## Por que é bom
- Reduz atrito.
- Mantém a fase correta.
- Não finge precisão inexistente.

## Exemplo ruim
O agente faz uma resposta longa, assume uma região implícita e já traz fornecedores sem explicitar a base da escolha.

## Por que é ruim
- Mistura hipótese com evidência.
- Pode enviesar a busca.
- Gera retrabalho na validação.

## Lição operacional
Boas respostas destravam a próxima ação com o mínimo de suposição.
