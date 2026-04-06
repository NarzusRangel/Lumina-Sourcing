# Fluxos de atualizacao

## Regra geral
- Identificar a entidade primeiro.
- Localizar o registro antes de perguntar o novo valor.
- Perguntar apenas propriedades que mudam.
- Preservar o restante do registro.
- Mostrar payload proposto antes da escrita.

## `*atualizar` fornecedor
Perguntar:
1. Qual fornecedor deve ser atualizado.
2. Quais propriedades mudam.
3. Novo valor de cada propriedade.
4. Se alguma relacao com contatos ou itens tambem muda.

## `*atualizar` contato
Perguntar:
1. Qual e-mail ou contato deve ser atualizado.
2. Quais propriedades mudam.
3. Se os fornecedores relacionados devem ser mantidos, removidos ou ampliados.

## `*atualizar` material
Perguntar:
1. Qual item normalizado deve ser atualizado.
2. Quais propriedades mudam.
3. Se os fornecedores relacionados devem ser mantidos, removidos ou ampliados.

## Saida obrigatoria
- resumo do registro encontrado
- payload estruturado
- lista de relacoes impactadas
- confirmacao de que a escrita depende de autorizacao explicita
