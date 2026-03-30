---
title: "Modelo de Derivação Documental"
doc_id: "PFW-00-005"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "Arquitetura Nova Para Framework de Pesquisa de Fornecedores.md"
---

# Modelo de Derivação Documental

## Objetivo
Definir como a base normativa é derivada para instruções operacionais, canais e integrações sem duplicação incoerente.

## Camadas
1. Base-mãe normativa: `00_fundacao`, `01_operacao`, `02_qualidade`
2. Adaptadores de canal: `03_chatgpt_web`, `04_codex`
3. Artefatos executáveis e registros: `05_integracoes`, `context/`, `memory/`

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
- Nunca editar GPT instructions finais sem atualizar `03_chatgpt_web/01_gpt-instructions-source.md`.
- Nunca editar AGENTS.md ou SKILL.md finais sem atualizar primeiro os documentos-fontes em `04_codex/`.
- Mudanças relevantes devem ser registradas em `08_governanca/02_log-de-decisoes-documentais.md`.

## Uso do agente legado
- O arquivo legado deve ser tratado como insumo histórico.
- Regras reaproveitadas do legado precisam ser reescritas, justificadas e normalizadas nesta base.
