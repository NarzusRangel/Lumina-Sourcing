---
title: "Arquitetura Codex"
doc_id: "PFW-04-001"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/00_fundacao/04_modelo-de-derivacao-documental.md"
---

# Arquitetura Codex

## Objetivo do canal
Viabilizar a operação avançada da pesquisa de fornecedores com fases explícitas, contexto modular, comandos repetíveis e integração com base operacional.

## O que o Codex fará que o Web não deve fazer
- Executar workflow guiado por fases.
- Trabalhar com context packs sob demanda.
- Preparar cadastros, atualizações e sincronizações estruturadas.
- Servir de ambiente de manutenção da skill, do AGENTS e da documentação.

## Tipos de artefato
- `AGENTS.md`: regras de execução e colaboração no repositório.
- `SKILL.md`: habilidade estreita, reutilizável e acionável.
- `context/`: pacotes de contexto por fase, domínio ou cenário.
- `memory/`: registros locais e exportações operacionais.

## Regra de desenho
- AGENTS enxuto e operacional.
- Skill focada em trabalho recorrente, não em conhecimento enciclopédico.
- Contexto carregado sob demanda.
- Comandos por fase com saída verificável.
