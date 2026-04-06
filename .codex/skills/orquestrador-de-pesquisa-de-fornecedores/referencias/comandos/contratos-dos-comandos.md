# Contratos dos comandos

## Regra transversal
- Fazer de 2 a 4 perguntas curtas por rodada.
- Nao duplicar perguntas ja respondidas.
- Nao encerrar sem proximo passo claro.
- Em fluxos de escrita, mostrar preview de payload e lembrar que a gravacao depende de autorizacao explicita do usuario.

## `*pesquisar`
- Entrada minima: descricao tecnica ou nome do item, objetivo da busca e contexto minimo disponivel.
- Perguntas permitidas: apenas o necessario para destravar item, fabricante, regiao ou restricao critica.
- Saida esperada: resposta estruturada na ordem fixa de `formato-da-resposta.md`, com shortlist em cards.
- Condicao de encerramento: entregar a shortlist e sugerir um unico proximo passo principal.

## `*buscar`
- Entrada minima: alvo (`material`, `fornecedor` ou `contato`) e identificador inicial do registro.
- Perguntas permitidas: apenas para desambiguar alvo, fornecedor principal, objetivo da consulta ou contexto minimo.
- Saida esperada: registro encontrado, relacoes relevantes, lacunas e proximo passo curto.
- Condicao de encerramento: o usuario entende o que foi encontrado e o que falta para seguir.

## `*registrar`
- Entrada minima: alvo (`material`, `fornecedor` ou `contato`) e intencao de cadastro.
- Perguntas permitidas: apenas campos obrigatorios reais, relacionamentos, responsavel, status e observacoes relevantes.
- Saida esperada: payload pronto para gravacao, lacunas remanescentes e confirmacao textual de dependencia de autorizacao.
- Condicao de encerramento: preview completo montado e usuario apto a autorizar ou corrigir.

## `*atualizar`
- Entrada minima: alvo (`material`, `fornecedor` ou `contato`) e identificador do registro.
- Perguntas permitidas: apenas o necessario para localizar o registro e confirmar os campos que mudam.
- Saida esperada: resumo do registro encontrado, campos alterados, relacoes impactadas e payload de atualizacao.
- Condicao de encerramento: alteracoes parciais definidas sem sobrescrever o restante do registro.

## `*gerarRFQ`
- Entrada minima: item, contexto comercial e destinatario ou perfil de destinatario.
- Perguntas permitidas: apenas para fechar prazo, volume, prazo de resposta, anexos ou pontos obrigatorios do pedido.
- Saida esperada: e-mail completo de RFQ, pronto para uso.
- Condicao de encerramento: mensagem final pronta, sem lacunas criticas abertas.

## `*followupRFQ`
- Entrada minima: contexto da RFQ anterior e objetivo do follow-up.
- Perguntas permitidas: apenas para fechar prazo, urgencia, referencia da RFQ ou destinatario.
- Saida esperada: e-mail completo de follow-up, pronto para uso.
- Condicao de encerramento: mensagem final pronta, curta e acionavel.

## `*criartemplateRFQ`
- Entrada minima: classe de demanda e contexto de uso.
- Perguntas permitidas: apenas para definir variaveis reutilizaveis e tom desejado.
- Saida esperada: template reutilizavel com placeholders claros.
- Condicao de encerramento: modelo reutilizavel pronto para adaptar.

## `*criartemplatefollowUP`
- Entrada minima: classe de demanda e contexto de uso.
- Perguntas permitidas: apenas para definir variaveis reutilizaveis e gatilho do follow-up.
- Saida esperada: template reutilizavel com placeholders claros.
- Condicao de encerramento: modelo reutilizavel pronto para adaptar.
