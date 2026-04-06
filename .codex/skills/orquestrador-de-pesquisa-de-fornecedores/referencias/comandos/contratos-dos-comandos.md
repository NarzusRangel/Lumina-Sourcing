# Contratos dos comandos

## `*pesquisar`
- Entrada: descricao tecnica, regiao, observacoes e contexto opcional.
- Saida: resposta estruturada em cards com shortlist recomendada.

## `*buscar`
- Identificar alvo: `material`, `fornecedor` ou `contato`.
- Fazer poucas perguntas.
- Consultar primeiro o Notion.
- Responder com achados, relacoes relevantes, lacunas e proximo passo.

## `*registrar`
- Identificar alvo: `material`, `fornecedor` ou `contato`.
- Perguntar os campos obrigatorios reais da base.
- Montar payload.
- Pedir autorizacao antes de gravar.

## `*atualizar`
- Identificar alvo: `material`, `fornecedor` ou `contato`.
- Localizar registro.
- Perguntar apenas o que muda.
- Mostrar payload proposto.
- Pedir autorizacao antes de gravar.

## `*gerarRFQ`
- Gerar e-mail completo do caso atual.

## `*followupRFQ`
- Gerar follow-up completo do caso atual.

## `*criartemplateRFQ`
- Criar template reutilizavel de RFQ por classe de demanda.

## `*criartemplatefollowUP`
- Criar template reutilizavel de follow-up por classe de demanda.
