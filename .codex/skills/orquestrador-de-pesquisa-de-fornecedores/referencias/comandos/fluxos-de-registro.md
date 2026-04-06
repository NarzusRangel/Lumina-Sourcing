# Fluxos de registro

## Regras gerais
- Nunca inferir campos criticos se o usuario puder responder.
- Sempre confirmar relacoes entre registros.
- Respeitar a estrutura visual e os icones ja existentes no Notion.
- Nao alterar views, titulos visuais ou organizacao sem pedido explicito.

## `*registrar` fornecedor
Perguntar:
1. Nome do fornecedor.
2. Tipo de fornecedor.
3. Pais/Regiao.
4. Site, se houver.
5. Tipos de materiais atendidos.
6. Responsavel pelo cadastro.
7. Status do fornecedor.
8. Observacoes, se houver.

Montar payload para `Fornecedores`.

## `*registrar` contato
Perguntar:
1. E-mail.
2. Nome do contato, se houver.
3. Cargo, se houver.
4. Telefone, se houver.
5. Responsavel pelo cadastro.
6. Status do contato.
7. Observacoes, se houver.
8. Quais fornecedores devem ser relacionados.

Confirmacoes obrigatorias:
- O fabricante do item original deve ser relacionado a este contato?
- Algum distribuidor ou revendedor recomendado tambem deve ser relacionado?
- Algum fornecedor relacionado ainda nao existe no banco e precisa ser cadastrado antes?

Montar payload para `Contatos de Fornecedores`.

## `*registrar` material
Perguntar:
1. Nome do item normalizado.
2. NCM provavel, se houver.
3. Tipos de materiais / familia.
4. Observacoes tecnicas.
5. Responsavel.
6. Quais fornecedores serao relacionados.

Confirmacoes obrigatorias:
- Qual e o fabricante do item original?
- Esse fabricante ja existe em `Fornecedores`?
- Distribuidores ou revendedores recomendados tambem devem ser relacionados?

Montar payload para `Catalogo de Materiais / Componentes`.
