---
name: orquestrador-de-pesquisa-de-fornecedores
description: Pesquisa de fornecedores com resposta comercial estruturada, shortlist em cards, fluxo seguro de busca/registro/atualizacao guiado no Notion e geracao de RFQ ou follow-up. Use quando o pedido envolver pesquisa de item ou servico, consulta de materiais/fornecedores/contatos, preparacao assistida de cadastro ou atualizacao no Notion, criacao de RFQ, follow-up de RFQ ou templates reutilizaveis desses emails.
---

# Orquestrador de Pesquisa de Fornecedores

Use esta skill para pesquisar, qualificar fornecedores, orientar fluxos seguros no Notion e gerar RFQs ou follow-ups comerciais da Lumina Group.

## Principios centrais
- Nenhuma escrita no Notion ocorre sem autorizacao explicita do usuario.
- Trate `1 e-mail = 1 contato` como regra operacional obrigatoria.
- Nao invente fornecedores, contatos, certificacoes, representacoes, estoque, homologacao ou relacoes.
- Preserve o design atual do Notion: nao alterar icones, nomes visuais, views ou organizacao sem pedido explicito.
- Priorize distribuidores na shortlist; use revendedores apenas para preencher lacunas e no maximo 4.
- Use sempre os nomes reais das propriedades existentes nas bases do Notion.

## Comandos publicos
- `*pesquisar`
- `*registrar`
- `*buscar`
- `*atualizar`
- `*gerarRFQ`
- `*followupRFQ`
- `*criartemplateRFQ`
- `*criartemplatefollowUP`

## Roteamento por intencao
- Use `*pesquisar` quando o usuario quer encontrar fornecedores, comparar oferta, validar um item ou iniciar a jornada sem indicar outro comando.
- Use `*buscar` quando o usuario quer consultar o Notion para localizar `material`, `fornecedor` ou `contato` existentes.
- Use `*registrar` quando o usuario quer preparar um novo cadastro no Notion com payload e relacoes confirmadas.
- Use `*atualizar` quando o usuario quer alterar um registro ja existente, preservando o restante dos dados.
- Use `*gerarRFQ` quando o usuario quer um e-mail de cotacao completo para o caso atual.
- Use `*followupRFQ` quando o usuario quer cobrar retorno de uma RFQ ja enviada.
- Use `*criartemplateRFQ` quando o usuario quer um modelo reutilizavel de RFQ por classe de demanda.
- Use `*criartemplatefollowUP` quando o usuario quer um modelo reutilizavel de follow-up por classe de demanda.

## Comportamento padrao
- Se o usuario nao indicar comando, comece por `*pesquisar`.
- Se faltarem descricao tecnica ou objetivo da consulta, faca apenas as perguntas minimas para destravar a proxima rodada.
- Se o fabricante nao vier informado, nao bloqueie a pesquisa; siga com a melhor interpretacao tecnica e deixe explicito quando houver inferencia.
- Se a regiao nao vier informada, pergunte uma vez. Se ela nao for respondida, siga com pesquisa ampla e sinalize que a shortlist inicial esta sem recorte regional firme.
- Se o contexto estiver insuficiente para escrita no Notion, pause no preview de lacunas e nao improvise valores criticos.

## Ordem de leitura por fluxo
- Para `*pesquisar`, leia nesta ordem:
  - `referencias/comandos/triagem-de-pesquisa.md`
  - `referencias/pesquisa/instrucao-canonica-de-pesquisa.md`
  - `referencias/pesquisa/regras-canonicas.md`
  - `referencias/pesquisa/analise-tecnica-e-shortlist.md`
  - `referencias/pesquisa/formato-da-resposta.md`
  - `referencias/pesquisa/modelo-card-fornecedor.md`
- Para `*buscar`, `*registrar` e `*atualizar`, leia nesta ordem:
  - `referencias/banco-notion/entidades-e-relacionamentos.md`
  - `referencias/banco-notion/propriedades-reais-das-bases.md`
  - `referencias/banco-notion/regras-de-cadastro.md`
  - `referencias/banco-notion/registro-notion-operacional.md`
  - `referencias/banco-notion/modelos-de-payload.md`
  - `referencias/comandos/contratos-dos-comandos.md`
  - o fluxo especifico correspondente em `referencias/comandos/`
- Para `*gerarRFQ` e `*followupRFQ`, leia o arquivo correspondente em `referencias/emails/`.
- Para templates reutilizaveis, leia `referencias/emails/criar-template-rfq.md` ou `referencias/emails/criar-template-followup.md`.

## Fluxo base de pesquisa
1. Interpretar tecnicamente o item e identificar o objetivo do usuario.
2. Aplicar a triagem inicial em `referencias/comandos/triagem-de-pesquisa.md`.
3. Aplicar as regras canonicas de busca, verdade e hierarquia de fontes.
4. Montar a shortlist conforme `referencias/pesquisa/analise-tecnica-e-shortlist.md`.
5. Responder no formato fixo definido em `referencias/pesquisa/formato-da-resposta.md`.
6. Usar cards por fornecedor conforme `referencias/pesquisa/modelo-card-fornecedor.md`.
7. Encerrar com um proximo passo claro.

## Safe-write gate
Antes de qualquer escrita ou confirmacao de escrita no Notion:
1. Localize a entidade e a base alvo.
2. Levante lacunas e campos criticos ainda nao confirmados.
3. Confirme relacoes entre item, fabricante, distribuidor, revendedor, fornecedor e contato.
4. Monte o payload com os nomes reais das propriedades.
5. Mostre preview claro da operacao, da base, do registro alvo e dos campos.
6. Declare explicitamente: `A gravacao no Notion depende de autorizacao explicita do usuario.`

## Conducao operacional
- Faça de 2 a 4 perguntas curtas por rodada.
- Consulte primeiro o Notion em `*buscar`, `*registrar` e `*atualizar`.
- Nao trate inferencia como fato; sinalize a diferenca no texto final.
- Quando um detalhe couber melhor nas referencias, siga o contrato da referencia em vez de expandir o `SKILL.md`.

## Arquivos internos essenciais
- `referencias/pesquisa/instrucao-canonica-de-pesquisa.md`
- `referencias/pesquisa/regras-canonicas.md`
- `referencias/comandos/triagem-de-pesquisa.md`
- `referencias/pesquisa/analise-tecnica-e-shortlist.md`
- `referencias/pesquisa/formato-da-resposta.md`
- `referencias/pesquisa/modelo-card-fornecedor.md`
- `referencias/comandos/contratos-dos-comandos.md`
- `referencias/banco-notion/registro-notion-operacional.md`
