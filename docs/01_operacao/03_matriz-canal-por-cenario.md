---
title: "Matriz Canal por Cenário"
doc_id: "PFW-01-004"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/00_fundacao/02_perfis-de-usuarios.md"
---

# Matriz Canal por Cenário

| Cenário | Melhor canal | Justificativa |
|---|---|---|
| Pedido simples de pesquisa com usuário pouco técnico | ChatGPT Web | menor atrito e experiência guiada |
| Pesquisa com múltiplas fases e necessidade de reaproveitar contexto | Codex | operação modular e maior controle |
| Revisão de padrão, skill, workflow ou documentação | Codex | ambiente apropriado para manutenção |
| Registro estruturado e atualização de base operacional | Codex + Notion | requer contrato de dados e auditoria |
| Aprovação final ou decisão crítica | Humano | responsabilidade decisória fora do escopo da IA |

## Política de encaminhamento
- O Web deve absorver o que for simples e orientar o usuário quando o caso exigir Codex.
- O Codex deve assumir casos com fases, contexto persistente, atualização de base ou manutenção do próprio sistema.
- O humano permanece decisor nos casos críticos, regulatórios ou contratuais.
