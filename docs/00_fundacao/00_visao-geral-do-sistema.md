---
title: "Visão Geral do Sistema"
doc_id: "PFW-00-001"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - ".codex/skills/orquestrador-de-pesquisa-de-fornecedores/SKILL.md"
---

# Visão Geral do Sistema

## Objetivo
Definir a visão-mãe do framework de pesquisa de fornecedores da Lumina Group, que servirá de base para um GPT Custom Web e para uma skill agentica no Codex.

## Contexto do negócio
A Lumina Group já possui um agente legado de pesquisa de fornecedores usado por um único setor. A nova iniciativa busca substituir essa lógica local por um sistema transversal, revisável e aderente a múltiplos setores comerciais.

## Problema que o sistema resolve
- Reduz a dependência de conhecimento tácito e instruções pessoais.
- Padroniza a triagem, a pesquisa, a qualificação e o registro de fornecedores.
- Separa claramente regra normativa, contexto operacional e memória transacional.

## Objetivos principais
- Criar uma base documental única para orientar a construção dos canais Web e Codex.
- Atender demandas comerciais de pesquisa de fornecedores com fases, critérios de qualidade e handoffs claros.
- Preparar a futura integração com Notion para cadastro, atualização e auditoria operacional.

## Resultados esperados
- Menor variação entre analistas e setores.
- Respostas mais úteis e rastreáveis.
- Evolução contínua do agente e da skill sem drift documental.

## Canais suportados
- ChatGPT Web para uso amplo, simples e guiado.
- Codex para uso avançado, execução em fases, manutenção de contexto e automação operacional.
- Notion como memória operacional estruturada, não como fonte normativa.

## Princípios arquiteturais
- A base-mãe vive na documentação normativa.
- Regras de canal derivam da base-mãe; não a substituem.
- Conhecimento estável vive em `references/`.
- Contexto de execução vive em `context/`.
- Registros e sincronizações vivem em `memory/` e nas integrações externas.
- O agente legado é apenas referência histórica e não dita o padrão futuro.

## Restrições relevantes
- O sistema deve servir a todos os setores comerciais, não a um fluxo único.
- O desenho precisa prever operação por fases e futura escrita em banco Notion.
- Toda derivação futura para GPT instructions, AGENTS.md e SKILL.md deve apontar para esta base.

## Perguntas em aberto para revisão
- Quais setores comerciais terão prioridade na fase inicial de adoção?
- Quais classes de fornecedor entram no primeiro escopo além do contexto elétrico legado?
- Quais indicadores de sucesso serão usados para validar a nova operação?
