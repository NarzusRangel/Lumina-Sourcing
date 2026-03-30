---
title: "Validação Manual da Skill e do Notion"
doc_id: "PFW-07-004"
version: "0.1.0"
status: "in_review"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-30"
next_review: "2026-04-15"
derived_from:
  - "docs/03_chatgpt_web/04_gpt-instructions-final.md"
  - "docs/05_integracoes/04_blueprint-execucao-notion-mcp.md"
  - ".codex/skills/supplier-research-orchestrator/SKILL.md"
---

# Validação Manual da Skill e do Notion

## Objetivo
Registrar o estado consolidado da skill `supplier-research-orchestrator` e da implementação do banco operacional no Notion após validação manual.

## Artefatos consolidados
- Skill operacional:
  - [SKILL.md](C:\Users\narzu\Documents\Repositorios-Narzus\11_Agent_Pesquisa-de-Fornecedores\.codex\skills\supplier-research-orchestrator\SKILL.md)
- Artefato canônico de pesquisa:
  - [04_gpt-instructions-final.md](C:\Users\narzu\Documents\Repositorios-Narzus\11_Agent_Pesquisa-de-Fornecedores\docs\03_chatgpt_web\04_gpt-instructions-final.md)
- Blueprint técnico do Notion:
  - [04_blueprint-execucao-notion-mcp.md](C:\Users\narzu\Documents\Repositorios-Narzus\11_Agent_Pesquisa-de-Fornecedores\docs\05_integracoes\04_blueprint-execucao-notion-mcp.md)

## Implementação Notion validada
- Página-raiz:
  - [Lumina Group | MRO, Oil & Gas e Comercial](https://www.notion.so/333e34d07ec18101aadbe8c762c8e5c3)
- Bases:
  - [Fornecedores](https://www.notion.so/7e966c0d3c5c431084ab67ea2c506369)
  - [Contatos de Fornecedores](https://www.notion.so/3f470fcfac474b64a6f45898b80608d5)
  - [Catalogo de Materiais/Componentes](https://www.notion.so/15b8fd82bb7d495b8e67ee613b390381)

## O que ficou validado
- A skill funciona em pesquisa manual e segue a estrutura canônica do GPT final.
- A skill preserva o bloqueio de escrita no Notion sem autorização explícita.
- O banco Notion v1 está implementado e relacional.
- A skill e o blueprint convergem nas 3 bases da v1:
  - `Fornecedores`
  - `Contatos de Fornecedores`
  - `Catalogo de Materiais/Componentes`

## Critérios validados manualmente
- Entrada inicial baseada em:
  - `Descrição Técnica detalhada`
  - `Indicação da Região de Pesquisa`
  - `Observações`
  - `*Comandos` opcional
- Análise técnica inicial em uma única frase executiva.
- Datasheet apenas quando fácil e oficial.
- NCM como indicação inicial.
- Certificações como recomendação inicial.
- Pesquisa sem invenção de contatos, homologações ou representações.

## Estado atual
- `04_gpt-instructions-final.md`: referência canônica de pesquisa.
- `supplier-research-orchestrator`: referência operacional no Codex.
- Notion v1: implementado e apto para uso assistido.

## Próxima revisão obrigatória
Melhorar o fluxo de perguntas finais antes da skill atualizar ou registrar contatos e informações no Notion, para garantir curadoria mínima dos requisitos necessários em qualquer novo cadastro.

## Perguntas que a próxima revisão deve fechar
- Quais campos mínimos são obrigatórios para `criar fornecedor`?
- Quais campos mínimos são obrigatórios para `criar contato`?
- Quais campos mínimos são obrigatórios para `criar item normalizado`?
- Em quais cenários a skill deve parar e pedir confirmação adicional antes da escrita?
- Qual checklist curto de curadoria deve anteceder qualquer gravação no Notion?
