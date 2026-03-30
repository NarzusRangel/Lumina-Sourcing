# AGENTS.md - Synkra AIOX (Codex CLI)

Este arquivo define as instrucoes do projeto para o Codex CLI.

<!-- AIOX-MANAGED-START: core -->
## Core Rules

1. Siga a Constitution em `.aiox-core/constitution.md`
2. Priorize `CLI First -> Observability Second -> UI Third`
3. Trabalhe por stories em `docs/stories/`
4. Nao invente requisitos fora dos artefatos existentes
<!-- AIOX-MANAGED-END: core -->

<!-- AIOX-MANAGED-START: quality -->
## Quality Gates

- Rode `npm run lint`
- Rode `npm run typecheck`
- Rode `npm test`
- Atualize checklist e file list da story antes de concluir
<!-- AIOX-MANAGED-END: quality -->

<!-- AIOX-MANAGED-START: codebase -->
## Project Map

- Core framework: `.aiox-core/`
- CLI entrypoints: `bin/`
- Shared packages: `packages/`
- Tests: `tests/`
- Docs: `docs/`
<!-- AIOX-MANAGED-END: codebase -->

<!-- AIOX-MANAGED-START: commands -->
## Common Commands

- `npm run sync:ide`
- `npm run sync:ide:codex` (opcional; sincroniza apenas os arquivos auxiliares do Codex)
- `npm run sync:skills:codex`
- `npm run sync:skills:codex:global` (use apenas fora deste projeto para evitar duplicidade no `/skills`)
- `npm run validate:codex-sync`
- `npm run validate:codex-integration`
- `npm run validate:codex-skills`
- `npm run validate:paths`
<!-- AIOX-MANAGED-END: commands -->

<!-- AIOX-MANAGED-START: shortcuts -->
## Agent Shortcuts

Preferencia de ativacao no Codex CLI:
1. Use `/skills` e selecione `aiox-<agent-id>` vindo de `.codex/skills` (ex.: `aiox-architect`)
2. Se preferir, use os atalhos abaixo (`@architect`, `/architect`, etc.)

Interprete os atalhos abaixo carregando o arquivo correspondente em `.aiox-core/development/agents/` (fallback: `.codex/agents/`), renderize o greeting via `generate-greeting.js` e assuma a persona ate `*exit`:

- `@architect`, `/architect`, `/architect.md` -> `.aiox-core/development/agents/architect.md`
- `@dev`, `/dev`, `/dev.md` -> `.aiox-core/development/agents/dev.md`
- `@qa`, `/qa`, `/qa.md` -> `.aiox-core/development/agents/qa.md`
- `@pm`, `/pm`, `/pm.md` -> `.aiox-core/development/agents/pm.md`
- `@po`, `/po`, `/po.md` -> `.aiox-core/development/agents/po.md`
- `@sm`, `/sm`, `/sm.md` -> `.aiox-core/development/agents/sm.md`
- `@analyst`, `/analyst`, `/analyst.md` -> `.aiox-core/development/agents/analyst.md`
- `@devops`, `/devops`, `/devops.md` -> `.aiox-core/development/agents/devops.md`
- `@data-engineer`, `/data-engineer`, `/data-engineer.md` -> `.aiox-core/development/agents/data-engineer.md`
- `@ux-design-expert`, `/ux-design-expert`, `/ux-design-expert.md` -> `.aiox-core/development/agents/ux-design-expert.md`
- `@squad-creator`, `/squad-creator`, `/squad-creator.md` -> `.aiox-core/development/agents/squad-creator.md`
- `@aiox-master`, `/aiox-master`, `/aiox-master.md` -> `.aiox-core/development/agents/aiox-master.md`
<!-- AIOX-MANAGED-END: shortcuts -->

## Supplier Research Rules

Estas regras complementam o AGENTS base para o workflow de pesquisa de fornecedores da Lumina Group.

- Para pesquisas de fornecedores, use como fontes principais:
  - `docs/03_chatgpt_web/01_gpt-instructions-source.md`
  - `docs/04_codex/02_skill-catalog-and-pattern.md`
  - `docs/04_codex/04_comandos-por-fase.md`
  - `docs/05_integracoes/01_modelo-notion-operacional.md`
  - `docs/05_integracoes/02_eventos-campos-e-mapeamentos.md`
- Trate Oil & Gas e MRO como núcleo de especialidade, sem bloquear itens ou serviços atípicos.
- Em fluxos de pesquisa, mantenha a ordem: triagem, contexto, análise técnica inicial, pesquisa profunda, qualificação, síntese e registro.
- A entrega padrão de pesquisa deve incluir:
  - análise técnica curta
  - datasheet, apenas se for fácil e oficial
  - NCM provável, quando aplicável
  - certificações possíveis como recomendação
  - shortlist com 9 fornecedores sempre que a oferta permitir
- Priorize distribuidores. Revendedores entram apenas para preencher lacunas e no máximo 4.
- Se o fabricante já estiver identificado, não sugerir fabricante alternativo sem pedido explícito do usuário.
- Nunca invente fornecedores, sites, e-mails, telefones ou certificações.
- Nenhum cadastro ou atualização em Notion pode ocorrer sem autorização explícita do usuário.
- Para contatos operacionais, siga a regra `1 e-mail = 1 contato`.

## Supplier Research Rules

Estas regras complementam o AGENTS base para o workflow de pesquisa de fornecedores da Lumina Group.

- Para pesquisas de fornecedores, use como fontes principais:
  - `docs/03_chatgpt_web/01_gpt-instructions-source.md`
  - `docs/04_codex/02_skill-catalog-and-pattern.md`
  - `docs/04_codex/04_comandos-por-fase.md`
  - `docs/05_integracoes/01_modelo-notion-operacional.md`
  - `docs/05_integracoes/02_eventos-campos-e-mapeamentos.md`
- Trate Oil & Gas e MRO como núcleo de especialidade, sem bloquear itens ou serviços atípicos.
- Em fluxos de pesquisa, mantenha a ordem: triagem, contexto, análise técnica inicial, pesquisa profunda, qualificação, síntese e registro.
- A entrega padrão de pesquisa deve incluir:
  - análise técnica curta
  - datasheet, apenas se for fácil e oficial
  - NCM provável, quando aplicável
  - certificações possíveis como recomendação
  - shortlist com 9 fornecedores sempre que a oferta permitir
- Priorize distribuidores. Revendedores entram apenas para preencher lacunas e no máximo 4.
- Se o fabricante já estiver identificado, não sugerir fabricante alternativo sem pedido explícito do usuário.
- Nunca invente fornecedores, sites, e-mails, telefones ou certificações.
- Nenhum cadastro ou atualização em Notion pode ocorrer sem autorização explícita do usuário.
- Para contatos operacionais, siga a regra `1 e-mail = 1 contato`.
