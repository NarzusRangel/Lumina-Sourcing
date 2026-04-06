# Entidades e relacionamentos

## Pagina raiz
`Lumina Group | MRO, Oil & Gas | Comercial`

## Entidades principais
### `Fornecedores`
Entidade central do banco.

### `Contatos de Fornecedores`
Entidade operacional centrada no e-mail.

### `Catalogo de Materiais / Componentes`
Entidade de item normalizado.

## Relacionamentos
- `Fornecedores` se relaciona com `Contatos relacionados`.
- `Fornecedores` se relaciona com `Itens relacionados`.
- `Contatos de Fornecedores` se relaciona com `Fornecedores Relacionados`.
- `Catalogo de Materiais / Componentes` se relaciona com `Fornecedores Relacionados`.

## Leitura operacional
- O fornecedor e o centro do ecossistema.
- O contato pode se ligar a mais de um fornecedor.
- O item normalizado pode se ligar ao fabricante e tambem a distribuidores ou revendedores, se o usuario quiser registrar isso.
