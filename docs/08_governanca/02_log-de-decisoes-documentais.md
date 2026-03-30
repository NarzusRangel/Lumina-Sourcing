---
title: "Log de Decisões Documentais"
doc_id: "PFW-08-003"
version: "0.2.0"
status: "in_review"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-30"
next_review: "2026-06-30"
derived_from:
  - "docs/08_governanca/00_governanca-e-versionamento.md"
---

# Log de Decisões Documentais

| Data | ID | Decisão | Racional | Impacto |
|---|---|---|---|---|
| 2026-03-29 | ADR-DOC-001 | Criar base documental completa em `docs/` antes de construir GPT Custom e skill. | Reduzir drift, personalização excessiva e dependência de instruções legadas. | Toda a implementação futura deve derivar desta base. |
| 2026-03-30 | ADR-DOC-002 | Adotar `04_gpt-instructions-final.md` como referência canônica da pesquisa e sincronizar a skill do Codex com essa versão. | Garantir que Web e Codex usem a mesma lógica de pesquisa, mudando apenas o fluxo operacional de Codex/Notion. | A skill `supplier-research-orchestrator` passa a herdar o comportamento de pesquisa do GPT final. |
| 2026-03-30 | ADR-DOC-003 | Consolidar a v1 do Notion com 3 bases relacionais e uso assistido por autorização explícita. | Fechar uma estrutura operacional simples, relacional e segura para cadastros e atualizações. | O fluxo de escrita no Notion fica condicionado a autorização e a próxima revisão deverá melhorar a curadoria mínima pré-cadastro. |
