---
title: "Taxonomia de Demandas"
doc_id: "PFW-00-004"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "Arquitetura Nova Para Framework de Pesquisa de Fornecedores.md"
---

# Taxonomia de Demandas

| Categoria | Subcategoria | Sinais de identificação | Entrada mínima | Saída esperada | Canal ideal |
|---|---|---|---|---|---|
| Triagem | Enquadramento inicial | usuário ainda não sabe como pedir | objetivo do item, contexto comercial | checklist de dados faltantes | ChatGPT Web |
| Pesquisa | Busca de fornecedores | foco em encontrar empresas, produtos ou serviços | descrição técnica mínima, região, observações | análise técnica básica + shortlist comentada | ChatGPT Web / Codex |
| Comparação | Avaliação inicial entre opções | múltiplos fornecedores ou produtos | lista de opções, critérios | tabela comparativa e recomendação | Codex |
| Estruturação | Padronização para uso interno | necessidade de planilha, relatório ou pré-cadastro | dados coletados | saída estruturada e limpa | Codex |
| Atualização | Manutenção de registro operacional | alteração de cadastro, status ou evidência sob comando do usuário | identificador do registro, nova evidência, autorização explícita | proposta de atualização e log | Codex |
| Enriquecimento de Cadastro/Contato | Cadastro ou ampliação de dados úteis no banco | usuário traz e-mails, telefones, marcas representadas ou vínculo comercial | dados de contato + autorização explícita | payload estruturado para cadastro/atualização | Codex |
| Governança | Revisão do sistema | pedido sobre padrão, canal, template ou melhoria | problema observado, artefato afetado | decisão documentada | Codex |

## Regras de uso da taxonomia
- A taxonomia classifica o tipo de trabalho, não o assunto do item pesquisado.
- Uma demanda pode atravessar mais de uma categoria, mas sempre inicia pela categoria dominante.
- Novas categorias só devem ser criadas quando alterarem o fluxo, o contrato de saída ou o canal recomendado.
- `Pesquisa` é a categoria dominante do sistema e absorve tanto itens do nicho principal quanto pesquisas atípicas.
- Produto e serviço permanecem dentro da mesma categoria de pesquisa; a diferença aparece na profundidade e na evidência disponível.
- `Atualização` e `Enriquecimento de Cadastro/Contato` exigem autorização explícita do usuário antes de qualquer gravação em banco operacional.

## Exemplos de enquadramento
- "Preciso achar fornecedores para este componente" → Pesquisa
- "Pesquise um serviço de inspeção tipo Q" → Pesquisa
- "Compare estas três opções e diga qual seguir" → Comparação
- "Transforme isso em cadastro operacional" → Estruturação
- "Atualize o banco com nova evidência" → Atualização
- "Cadastre estes e-mails e relacione às marcas representadas" → Enriquecimento de Cadastro/Contato
