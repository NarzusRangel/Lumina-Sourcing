---
title: "Blueprint de Execução Notion MCP"
doc_id: "PFW-05-004"
version: "0.2.0"
status: "in_review"
owner: "A definir (Lumina Group)"
reviewed_at: "2026-03-30"
next_review: "2026-06-30"
derived_from:
  - "docs/05_integracoes/01_modelo-notion-operacional.md"
  - "docs/05_integracoes/02_eventos-campos-e-mapeamentos.md"
---

# Blueprint de Execução Notion MCP

## Objetivo
Definir o schema técnico da v1 do banco operacional da Lumina Group no Notion, pronto para criação via MCP quando o workspace correto estiver conectado e a página-pai for informada.

## Escopo da v1
A v1 terá 3 bases relacionais:
- `Fornecedores`
- `Contatos de Fornecedores`
- `Catalogo de Materiais/Componentes`

## Regras estruturais da v1
- O banco é analítico e colaborativo, não CRM.
- `Fornecedores` é a entidade central.
- Um mesmo e-mail pode aparecer em mais de um registro de contato quando estiver relacionado a fornecedores diferentes.
- `Catalogo de Materiais/Componentes` armazena item normalizado, não resultado bruto de pesquisa.
- Escrita no Notion só pode ocorrer com autorização explícita do usuário.
- Novos contatos encontrados em pesquisas futuras devem ser adicionados, nunca substituir contatos antigos.
- Atualizações em registros existentes sobrescrevem o valor atual, preservando `Atualizado em`, `Responsável` e `Observações`.

## Base 1: Fornecedores

### Papel
Entidade principal do banco. Representa empresas únicas por nome comercial, mesmo quando acumulam mais de um papel no ecossistema.

### Propriedades
| Propriedade | Tipo Notion | Regra |
|---|---|---|
| `Nome do fornecedor` | `TITLE` | obrigatório; 1 registro por nome comercial único |
| `Tipo de fornecedor` | `MULTI_SELECT('Fabricante':blue, 'Distribuidor':green, 'Revendedor':orange, 'Comprador':red)` | permite múltiplos papéis |
| `País/Região` | `MULTI_SELECT` | valores livres e expansíveis pela equipe |
| `Site` | `URL` | opcional |
| `Tipos de materiais atendidos` | `MULTI_SELECT` | deve compartilhar o mesmo vocabulário-base usado nas demais bases |
| `Observações` | `RICH_TEXT` | notas operacionais e contexto |
| `Status do fornecedor` | `SELECT('Ativo':green, 'Revisar':yellow, 'Inativo':gray)` | estado operacional |
| `Responsável` | `MULTI_SELECT` | nomes livres e expansíveis; não usar `PEOPLE` na v1 |
| `Última evidência revisada` | `DATE` | data da última checagem relevante |
| `Contatos relacionados` | `RELATION('CONTATOS_DS_ID', DUAL 'Fornecedores Relacionados')` | preenchido após criação da base de contatos |
| `Itens relacionados` | `RELATION('CATALOGO_DS_ID', DUAL 'Fornecedores Relacionados')` | preenchido após criação da base de catálogo |
| `Criado em` | `CREATED_TIME` | auditoria mínima |
| `Atualizado em` | `LAST_EDITED_TIME` | auditoria mínima |

## Base 2: Contatos de Fornecedores

### Papel
Armazenar contatos operacionais centrados no e-mail, com foco em uso prático pelos colaboradores.

### Propriedades
| Propriedade | Tipo Notion | Regra |
|---|---|---|
| `E-mail` | `TITLE` | chave operacional da linha |
| `Nome do contato` | `RICH_TEXT` | opcional; pode ser descoberto depois |
| `Cargo` | `RICH_TEXT` | opcional |
| `Telefone` | `PHONE_NUMBER` | opcional |
| `Fornecedores Relacionados` | `RELATION('FORNECEDORES_DS_ID', DUAL 'Contatos relacionados')` | um contato pode se ligar a múltiplos fornecedores |
| `Tipos de materiais relacionados` | `MULTI_SELECT` | mesmo vocabulário-base das outras bases |
| `Status do contato` | `SELECT('Novo':blue, 'Validado':green, 'Sem resposta':orange, 'Revisar':yellow, 'Inativo':gray)` | estado operacional |
| `Dados confirmados manualmente` | `CHECKBOX` | confirmação humana |
| `Observações` | `RICH_TEXT` | notas de curadoria |
| `Responsável` | `MULTI_SELECT` | nomes livres e expansíveis |
| `Criado em` | `CREATED_TIME` | auditoria mínima |
| `Atualizado em` | `LAST_EDITED_TIME` | auditoria mínima |

### Regra operacional crítica
Se uma nova sessão trouxer novos e-mails para um fornecedor já existente, o fluxo deve criar novos registros em `Contatos de Fornecedores`. Não excluir nem substituir registros antigos automaticamente.

## Base 3: Catalogo de Materiais/Componentes

### Papel
Armazenar itens normalizados, ligados a segmentos e fornecedores capazes de atendê-los.

### Propriedades
| Propriedade | Tipo Notion | Regra |
|---|---|---|
| `Nome do item normalizado` | `TITLE` | item consolidado e limpo |
| `Fornecedores Relacionados` | `RELATION('FORNECEDORES_DS_ID', DUAL 'Itens relacionados')` | inclui fabricantes, distribuidores e revendedores relacionados ao item |
| `Segmento` | `RICH_TEXT` | texto congelado derivado de NCM/nicho |
| `NCM provável` | `RICH_TEXT` | classificação sugerida, não normativa |
| `Tipos de materiais / família` | `MULTI_SELECT` | vocabulário-base compartilhado |
| `Observações técnicas` | `RICH_TEXT` | detalhes úteis de normalização e curadoria |
| `Responsável` | `MULTI_SELECT` | nomes livres e expansíveis |
| `Criado em` | `CREATED_TIME` | auditoria mínima |
| `Atualizado em` | `LAST_EDITED_TIME` | auditoria mínima |

## Vocabulários compartilhados

### Campos que devem reaproveitar o mesmo vocabulário
- `Tipos de materiais atendidos`
- `Tipos de materiais relacionados`
- `Tipos de materiais / família`
- `Responsável`
- `País/Região`

### Regra
O MCP pode criar os campos como `MULTI_SELECT`, mas a curadoria da lista de valores seguirá evolutiva. A equipe poderá adicionar novas opções conforme adoção e crescimento do banco.

## Ordem de criação via MCP

### Etapa 1
Criar `Fornecedores` sem relações externas.

### Etapa 2
Criar `Contatos de Fornecedores` com relação dual para `Fornecedores`.

### Etapa 3
Atualizar `Fornecedores` para consolidar a relação dual com `Contatos de Fornecedores`, se necessário.

### Etapa 4
Criar `Catalogo de Materiais/Componentes` com relação dual para `Fornecedores`.

### Etapa 5
Atualizar `Fornecedores` para consolidar a relação dual com `Catalogo de Materiais/Componentes`, se necessário.

## Estratégia técnica recomendada
- Criar `Fornecedores` primeiro.
- Capturar o `data_source_id` retornado.
- Criar `Contatos de Fornecedores` referenciando o `data_source_id` de `Fornecedores`.
- Criar `Catalogo de Materiais/Componentes` referenciando o mesmo `data_source_id`.
- Fazer `fetch` após cada criação para confirmar schema e IDs reais.
- Só depois criar views auxiliares.

## Schema DDL de referência para MCP

### 1. Fornecedores
```sql
CREATE TABLE (
  "Nome do fornecedor" TITLE,
  "Tipo de fornecedor" MULTI_SELECT('Fabricante':blue, 'Distribuidor':green, 'Revendedor':orange, 'Comprador':red),
  "País/Região" MULTI_SELECT('Brasil':green, 'Global':blue),
  "Site" URL,
  "Tipos de materiais atendidos" MULTI_SELECT('Instrumentação':blue, 'Elétrica':yellow, 'Automação':purple),
  "Observações" RICH_TEXT,
  "Status do fornecedor" SELECT('Ativo':green, 'Revisar':yellow, 'Inativo':gray),
  "Responsável" MULTI_SELECT('A definir':default),
  "Última evidência revisada" DATE,
  "Criado em" CREATED_TIME,
  "Atualizado em" LAST_EDITED_TIME
)
```

### 2. Contatos de Fornecedores
Substituir `FORNECEDORES_DS_ID` pelo `data_source_id` real retornado após criar `Fornecedores`.

```sql
CREATE TABLE (
  "E-mail" TITLE,
  "Nome do contato" RICH_TEXT,
  "Cargo" RICH_TEXT,
  "Telefone" PHONE_NUMBER,
  "Fornecedores Relacionados" RELATION('FORNECEDORES_DS_ID', DUAL 'Contatos relacionados'),
  "Tipos de materiais relacionados" MULTI_SELECT('Instrumentação':blue, 'Elétrica':yellow, 'Automação':purple),
  "Status do contato" SELECT('Novo':blue, 'Validado':green, 'Sem resposta':orange, 'Revisar':yellow, 'Inativo':gray),
  "Dados confirmados manualmente" CHECKBOX,
  "Observações" RICH_TEXT,
  "Responsável" MULTI_SELECT('A definir':default),
  "Criado em" CREATED_TIME,
  "Atualizado em" LAST_EDITED_TIME
)
```

### 3. Catalogo de Materiais/Componentes
Substituir `FORNECEDORES_DS_ID` pelo `data_source_id` real retornado após criar `Fornecedores`.

```sql
CREATE TABLE (
  "Nome do item normalizado" TITLE,
  "Fornecedores Relacionados" RELATION('FORNECEDORES_DS_ID', DUAL 'Itens relacionados'),
  "Segmento" RICH_TEXT,
  "NCM provável" RICH_TEXT,
  "Tipos de materiais / família" MULTI_SELECT('Instrumentação':blue, 'Elétrica':yellow, 'Automação':purple),
  "Observações técnicas" RICH_TEXT,
  "Responsável" MULTI_SELECT('A definir':default),
  "Criado em" CREATED_TIME,
  "Atualizado em" LAST_EDITED_TIME
)
```

## Views recomendadas para a v1

### Fornecedores
- `Todos os fornecedores`
- `Fabricantes`
- `Distribuidores`
- `Revisar evidência`

### Contatos de Fornecedores
- `Todos os contatos`
- `Contatos validados`
- `Novos contatos`
- `Sem resposta`

### Catalogo de Materiais/Componentes
- `Todos os itens`
- `Por segmento`
- `Por fornecedor`
- `Sem revisão recente`

## Pré-requisitos para execução real
Antes da criação real via MCP, será necessário:
1. Conectar/autenticar o Notion correto nesta sessão.
2. Informar a URL ou ID da página-pai onde as 3 bases serão criadas.
3. Confirmar se os vocabulários iniciais de `MULTI_SELECT` podem nascer enxutos e crescer depois.
4. Autorizar explicitamente a criação das bases.

## Próxima ação operacional
Quando o Notion correto estiver conectado, este blueprint pode ser convertido em chamadas MCP na ordem:
1. `_notion_create_database` para `Fornecedores`
2. `fetch` do resultado para capturar `data_source_id`
3. `_notion_create_database` para `Contatos de Fornecedores`
4. `_notion_create_database` para `Catalogo de Materiais/Componentes`
5. `fetch` de validação
6. `_notion_create_view` para as views iniciais

## Estado de consolidação
- A v1 foi criada no Notion e validada manualmente como base operacional assistida.
- A próxima revisão deve melhorar a etapa de perguntas finais antes de qualquer cadastro ou atualização, para garantir curadoria mínima dos requisitos obrigatórios.
