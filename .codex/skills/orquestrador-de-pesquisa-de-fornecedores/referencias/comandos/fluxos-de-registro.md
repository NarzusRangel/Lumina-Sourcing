# Fluxos de registro

## Regras gerais
- Nunca inferir campos criticos se o usuario puder responder.
- Sempre confirmar relacoes entre registros.
- Respeitar a estrutura visual e os icones ja existentes no Notion.
- Nao alterar views, titulos visuais ou organizacao sem pedido explicito.
- Nao montar payload final sem confirmar relacoes, responsavel e status quando a base exigir.
- Encerrar sempre com preview de payload e frase de dependencia de autorizacao explicita.

## `*registrar` fornecedor
### O que preciso saber
1. Nome do fornecedor.
2. Tipo de fornecedor.
3. Pais/Regiao.
4. Site, se houver.
5. Tipos de materiais atendidos.
6. Responsavel pelo cadastro.
7. Status do fornecedor.
8. Observacoes, se houver.

### O que posso inferir
- O payload alvo e `Fornecedores`.
- Campos opcionais vazios nao devem ser inventados.

### O que preciso confirmar
- Se o fornecedor ja existe no banco com outro nome ou variacao.
- Se o tipo de fornecedor esta correto para a operacao.

### O que entrego ao final
- payload de `Fornecedores`
- lacunas remanescentes
- confirmacao de que a gravacao depende de autorizacao explicita

## `*registrar` contato
### O que preciso saber
1. E-mail.
2. Nome do contato, se houver.
3. Cargo, se houver.
4. Telefone, se houver.
5. Responsavel pelo cadastro.
6. Status do contato.
7. Observacoes, se houver.
8. Quais fornecedores devem ser relacionados.

### O que posso inferir
- O payload alvo e `Contatos de Fornecedores`.
- `1 e-mail = 1 contato` permanece obrigatorio.

### O que preciso confirmar
- O fabricante do item original deve ser relacionado a este contato.
- Algum distribuidor ou revendedor recomendado tambem deve ser relacionado.
- Algum fornecedor relacionado ainda nao existe no banco e precisa ser cadastrado antes.
- O e-mail identifica de fato um novo contato e nao um registro ja existente.

### O que entrego ao final
- payload de `Contatos de Fornecedores`
- relacoes confirmadas
- lacunas remanescentes
- confirmacao de que a gravacao depende de autorizacao explicita

## `*registrar` material
### O que preciso saber
1. Nome do item normalizado.
2. NCM provavel, se houver.
3. Tipos de materiais / familia.
4. Observacoes tecnicas.
5. Responsavel.
6. Quais fornecedores serao relacionados.

### O que posso inferir
- O payload alvo e `Catalogo de Materiais / Componentes`.
- O item deve ser registrado em forma normalizada, nao como texto bruto da pesquisa.

### O que preciso confirmar
- Qual e o fabricante do item original.
- Se esse fabricante ja existe em `Fornecedores`.
- Se distribuidores ou revendedores recomendados tambem devem ser relacionados.
- Se o NCM e apenas uma indicacao inicial.

### O que entrego ao final
- payload de `Catalogo de Materiais / Componentes`
- relacoes confirmadas
- lacunas remanescentes
- confirmacao de que a gravacao depende de autorizacao explicita
