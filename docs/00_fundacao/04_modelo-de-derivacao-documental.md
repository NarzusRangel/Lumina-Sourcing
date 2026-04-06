---
title: "Modelo de Derivação Documental"
doc_id: "PFW-00-005"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - ".codex/skills/orquestrador-de-pesquisa-de-fornecedores/SKILL.md"
---

# Modelo de Derivação Documental

## Objetivo
Definir como a base normativa é derivada para instruções operacionais, canais e integrações sem duplicação incoerente.

## Camadas
1. Base normativa de referência: `00_fundacao`
2. Adaptador de canal Web: `03_chatgpt_web/04_gpt-instructions-final.md`
3. Artefato operacional principal: `.codex/skills/orquestrador-de-pesquisa-de-fornecedores/`

## Regra de prevalência
- Documento normativo vence documento de canal.
- Documento de canal vence exemplo.
- Exemplo nunca redefine regra.
- Registro operacional nunca redefine regra.

## Tipos de derivação
- `derived_from` obrigatório em documentos de canal e governança relacionada.
- `references/` concentra conhecimento estável e de consulta.
- `context/` concentra contexto carregável por fase, domínio ou caso.

## Anti-drift
- Nunca editar GPT instructions finais sem alinhar a skill `orquestrador-de-pesquisa-de-fornecedores`.
- Nunca editar a operação do sistema fora da skill quando a regra ou o fluxo forem específicos dela.
- Mudanças relevantes devem priorizar a skill como fonte operacional principal.

## Uso do agente legado
- O arquivo legado deve ser tratado como insumo histórico.
- Regras reaproveitadas do legado precisam ser reescritas, justificadas e normalizadas nesta base.
