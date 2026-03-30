---
title: "Modelo Notion Operacional"
doc_id: "PFW-05-002"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/05_integracoes/00_arquitetura-integracoes-e-mcp.md"
---

# Modelo Notion Operacional

## Bases iniciais sugeridas
- `Solicitacoes de Pesquisa`
- `Resultados de Pesquisa`
- `Fornecedores`
- `Contatos de Fornecedores`
- `Melhorias do Framework`

## Entidades mínimas
- Solicitação: quem pediu, o que pediu, prioridade, status, contexto.
- Resultado: resumo do caso, shortlist, evidência, riscos, data.
- Fornecedor: nome, tipo, região, site, observações, última evidência e marcas representadas.
- Contato de Fornecedor: um e-mail por contato, nome do contato quando houver, fornecedor relacionado, marcas representadas, origem e status.
- Melhoria: lacuna observada, impacto, origem e status.

## Regras operacionais do banco
- `1 e-mail = 1 contato`
- Um contato pode ser relacionado a diversos fabricantes, marcas e tipos de materiais.
- Nenhum contato deve ser criado ou atualizado automaticamente sem autorização explícita do usuário.
- A skill pode preparar payloads de cadastro ou atualização a partir dos dados enviados manualmente pelo usuário no chat.

## Fluxos previstos
- Fluxo 1: pesquisa completa -> resultado de pesquisa -> decisão humana -> cadastro ou atualização sob comando.
- Fluxo 2: cadastro ou atualização direta -> usuário envia e-mails e contexto -> skill prepara e grava sob autorização explícita.

## Campos mínimos sugeridos

### Base `Fornecedores`
- Nome do fornecedor
- Tipo de fornecedor
- País/Região
- Site
- Observações de mercado
- Marcas/Fabricantes representados
- Última evidência revisada

### Base `Contatos de Fornecedores`
- E-mail
- Nome do contato
- Telefone
- Fornecedor relacionado
- Marcas/Fabricantes relacionados
- Tipos de materiais relacionados
- Origem do contato
- Status do contato
- Observações

### Base `Resultados de Pesquisa`
- Item pesquisado
- Resumo técnico
- Datasheet
- NCM provável
- Certificações possíveis
- Lista resumida de fornecedores
- Responsável pela pesquisa
- Data da pesquisa

## Regra
O desenho final do Notion deve ser aprovado depois que os campos mínimos e os relacionamentos forem validados com casos reais, mas este documento já define o contrato operacional de v1.
