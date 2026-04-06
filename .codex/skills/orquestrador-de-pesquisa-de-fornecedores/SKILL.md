---
name: orquestrador-de-pesquisa-de-fornecedores
description: Pesquisa de fornecedores com resposta comercial estruturada, shortlist em cards, busca/registro/atualizacao guiados no Notion e geracao de RFQ ou follow-up. Use quando o pedido envolver pesquisa de item ou servico, consulta de materiais/fornecedores/contatos, cadastro ou atualizacao assistida no Notion, criacao de RFQ, follow-up de RFQ ou templates reutilizaveis desses emails.
---

# Orquestrador de Pesquisa de Fornecedores

Use esta skill como camada operacional da Lumina Group para pesquisa, qualificacao comercial e preparacao assistida de cadastros no Notion.

## Principios fixos
- Use `*pesquisar` como fluxo padrao quando o usuario nao indicar comando.
- Preserve o comportamento canonico consolidado em `referencias/pesquisa/instrucao-canonica-de-pesquisa.md`.
- Preserve o design existente do Notion: nao alterar icones, nomes visuais, views ou organizacao sem pedido explicito do usuario.
- Use sempre os nomes reais das propriedades ja existentes nas bases do Notion.
- Nao grave nada no Notion sem autorizacao explicita do usuario.
- Trate `1 e-mail = 1 contato` como regra operacional obrigatoria.
- Nao invente fornecedores, contatos, certificacoes, representacoes, estoque ou homologacao.

## Comandos publicos
- `*pesquisar`
- `*registrar`
- `*buscar`
- `*atualizar`
- `*gerarRFQ`
- `*followupRFQ`
- `*criartemplateRFQ`
- `*criartemplatefollowUP`

## Roteamento rapido
- `*pesquisar`: entregar analise tecnica, NCM, certificacoes e shortlist em cards.
- `*buscar`: identificar `material`, `fornecedor` ou `contato`, fazer poucas perguntas e consultar primeiro o Notion.
- `*registrar`: identificar a entidade, perguntar os campos obrigatorios reais da base e montar payload antes de qualquer gravacao.
- `*atualizar`: localizar o registro, perguntar apenas o que muda e mostrar o payload proposto antes da escrita.
- `*gerarRFQ`: gerar e-mail completo para o caso atual.
- `*followupRFQ`: gerar follow-up completo para o caso atual.
- `*criartemplateRFQ`: criar modelo reutilizavel de RFQ por tipo de demanda.
- `*criartemplatefollowUP`: criar modelo reutilizavel de follow-up por tipo de demanda.

## Fluxo de pesquisa
1. Interpretar tecnicamente o item.
2. Aplicar a triagem inicial definida em `referencias/comandos/triagem-de-pesquisa.md`.
3. Aplicar as regras canonicas de busca e verdade.
4. Aplicar o contrato de analise e shortlist em `referencias/pesquisa/analise-tecnica-e-shortlist.md`.
5. Montar a resposta no formato padrao definido em `referencias/pesquisa/formato-da-resposta.md`.
6. Usar cards por fornecedor conforme `referencias/pesquisa/modelo-card-fornecedor.md`.
7. Sugerir proximo passo claro.

## Fluxos guiados do Notion
Antes de usar `*buscar`, `*registrar` ou `*atualizar`:
- Ler `referencias/banco-notion/entidades-e-relacionamentos.md`.
- Ler `referencias/banco-notion/propriedades-reais-das-bases.md`.
- Ler `referencias/banco-notion/regras-de-cadastro.md`.
- Ler `referencias/banco-notion/registro-notion-operacional.md`.
- Ler o fluxo especifico em `referencias/comandos/`.

Regras de conducao:
- Fazer 2 a 4 perguntas curtas por rodada.
- Confirmar relacoes entre item, fabricante, distribuidor, revendedor e contato.
- Perguntar o responsavel do cadastro quando a base exigir esse campo.
- Ao registrar contato, confirmar quais fornecedores serao relacionados.
- Ao registrar material, confirmar qual fabricante do item deve ser relacionado e se distribuidores ou revendedores tambem entram.

## Fluxos de e-mail
Antes de gerar ou estruturar e-mails:
- Ler `referencias/emails/gerar-rfq.md` ou `referencias/emails/followup-rfq.md`.
- Para templates reutilizaveis, ler `referencias/emails/criar-template-rfq.md` ou `referencias/emails/criar-template-followup.md`.

## Arquivos internos essenciais
- `referencias/pesquisa/instrucao-canonica-de-pesquisa.md`
- `referencias/comandos/triagem-de-pesquisa.md`
- `referencias/pesquisa/analise-tecnica-e-shortlist.md`
- `referencias/banco-notion/registro-notion-operacional.md`
