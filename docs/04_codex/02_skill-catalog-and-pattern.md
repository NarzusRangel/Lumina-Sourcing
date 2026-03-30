---
title: "Skill Catalog and Pattern"
doc_id: "PFW-04-003"
version: "0.1.0"
status: "draft"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from:
  - "docs/00_fundacao/03_taxonomia-de-demandas.md"
---

# Skill Catalog and Pattern

## Critérios para criar uma skill
- Resolver uma tarefa recorrente e bem delimitada.
- Ter gatilho claro de uso.
- Produzir saída verificável.
- Não duplicar a função de outra skill existente.

## Skill inicial prevista
- `supplier-research-orchestrator`
  - Objetivo: conduzir pesquisa de fornecedores por fases, com análise técnica inicial, pesquisa profunda, síntese operacional e preparação de cadastro/atualização no Notion.
  - Entradas mínimas: descrição técnica mínima, região foco e observações opcionais.
  - Saídas: análise técnica curta, datasheet opcional, NCM provável, certificações possíveis, shortlist com 9 fornecedores e payload de registro/atualização quando autorizado.

## Desenho da skill principal

### Nome e ID
- Nome: Supplier Research Orchestrator
- ID: `supplier-research-orchestrator`

### Problema que resolve
- Padroniza a pesquisa profunda de fornecedores para a operação comercial da Lumina Group.
- Evita perda de qualidade entre usuários iniciantes e avançados.
- Permite reaproveitar a pesquisa em fluxos de cadastro e atualização no Notion.

### Quando usar
- Pesquisa de fornecedores de materiais, produtos, componentes ou serviços.
- Casos que exigem análise técnica inicial antes da busca de mercado.
- Casos em que o usuário quer transformar pesquisa em cadastro ou atualização operacional.

### Quando não usar
- Aprovação final de fornecedor.
- Negociação, homologação ou decisão contratual.
- Cadastro no Notion sem autorização explícita do usuário.

### Entradas mínimas
- Descrição técnica mínima do item ou serviço.
- Região ou regiões de interesse.
- Observações livres, quando houver.

### Entradas opcionais de alto valor
- Fabricante conhecido.
- Part number.
- Comandos internos por setor, como família ou gatilhos especializados.
- Lista de e-mails já capturados manualmente pelo usuário para cadastro/atualização.

### Saídas obrigatórias do fluxo de pesquisa
- Análise técnica inicial curta.
- Link de datasheet apenas se for fácil, oficial e de baixo custo de pesquisa.
- NCM provável, quando aplicável.
- Lista de possíveis certificações recomendadas.
- Shortlist final com 9 fornecedores sempre que a oferta permitir.

### Regras da shortlist
- Se houver fabricante identificável, ele entra na lista como referência principal.
- As demais recomendações priorizam distribuidores.
- Revendedores só entram para completar lacunas e no máximo 4.
- Se o usuário informou fabricante, não sugerir outro fabricante sem pedido explícito.
- Se não houver fabricante identificável, a skill pode sugerir fabricantes alternativos.

### Regras de verdade
- Não inventar empresas, sites, contatos ou certificações.
- Só registrar contatos públicos ou dados fornecidos explicitamente pelo usuário.
- Sempre diferenciar evidência confirmada, inferência e recomendação.

### Regras de escrita
- Nenhum cadastro ou atualização no Notion ocorre sem comando explícito do usuário.
- Um usuário pode entrar direto na fase de cadastro/atualização se já tiver os dados necessários.

### Dependências de contexto
- Taxonomia de demandas.
- Fluxo operacional por fases.
- Critérios de qualidade.
- Contrato do Notion para contatos, fornecedores e resultados de pesquisa.

## Padrão de catálogo
| Skill ID | Problema que resolve | Quando usar | Quando não usar | Entradas | Saídas |
|---|---|---|---|---|---|
| supplier-research-orchestrator | pesquisa, síntese e registro operacional | pesquisa de fornecedores com fases e pós-processamento operacional | aprovação, negociação ou gravação sem autorização | descrição técnica, região, observações, dados de contato opcionais | análise técnica, shortlist, payload de registro |
