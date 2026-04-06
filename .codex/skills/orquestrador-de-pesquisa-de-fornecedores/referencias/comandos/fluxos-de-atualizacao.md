# Fluxos de atualizacao

## Regra geral
- Identificar a entidade primeiro.
- Localizar o registro antes de perguntar o novo valor.
- Perguntar apenas propriedades que mudam.
- Preservar o restante do registro.
- Mostrar payload proposto antes da escrita.
- Nao atualizar relacoes sem confirmar se devem ser mantidas, removidas ou ampliadas.
- Encerrar com frase de dependencia de autorizacao explicita.

## `*atualizar` fornecedor
### O que preciso saber
1. Qual fornecedor deve ser atualizado.
2. Quais propriedades mudam.
3. Novo valor de cada propriedade.
4. Se alguma relacao com contatos ou itens tambem muda.

### O que posso inferir
- O restante do registro deve ser preservado.
- O payload deve listar apenas campos alterados.

### O que preciso confirmar
- Se o registro encontrado e o correto.
- Se as relacoes associadas devem ser mantidas, removidas ou ampliadas.

### O que entrego ao final
- resumo do registro encontrado
- campos alterados
- relacoes impactadas
- payload estruturado

## `*atualizar` contato
### O que preciso saber
1. Qual e-mail ou contato deve ser atualizado.
2. Quais propriedades mudam.
3. Se os fornecedores relacionados devem ser mantidos, removidos ou ampliados.

### O que posso inferir
- O alvo primario e um registro em `Contatos de Fornecedores`.
- A atualizacao nao substitui automaticamente contatos antigos.

### O que preciso confirmar
- Se o e-mail ou o contato encontrado e o correto.
- Se o conjunto de fornecedores relacionados continua valido.

### O que entrego ao final
- resumo do registro encontrado
- campos alterados
- relacoes impactadas
- payload estruturado

## `*atualizar` material
### O que preciso saber
1. Qual item normalizado deve ser atualizado.
2. Quais propriedades mudam.
3. Se os fornecedores relacionados devem ser mantidos, removidos ou ampliados.

### O que posso inferir
- O alvo primario e um registro em `Catalogo de Materiais / Componentes`.
- A atualizacao parcial deve preservar o restante do cadastro.

### O que preciso confirmar
- Se o item normalizado localizado e o correto.
- Se fabricante, distribuidores e revendedores relacionados continuam corretos.

### O que entrego ao final
- resumo do registro encontrado
- campos alterados
- relacoes impactadas
- payload estruturado

## Saida obrigatoria
- resumo do registro encontrado
- payload estruturado
- lista de relacoes impactadas
- confirmacao de que a escrita depende de autorizacao explicita
