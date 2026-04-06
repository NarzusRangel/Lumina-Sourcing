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

## Logica de papeis comerciais
- `fabricante`, `distribuidor` e `revendedor` sao papeis comerciais de um registro em `Fornecedores`.
- Nem todo fornecedor e o fabricante original do item; confirme esse papel antes de relacionar.
- O contato e sempre centrado no e-mail e pode atender mais de um fornecedor.
- O material normalizado pode ser relacionado ao fabricante original e, se o usuario quiser, tambem a distribuidores ou revendedores relevantes.

## Regra de interpretacao
- Em `buscar`, use os relacionamentos para explicar o estado atual do banco.
- Em `registrar` e `atualizar`, confirme os papeis comerciais antes de montar o payload.
- Nao trate relacao sugerida em pesquisa como relacao aprovada para escrita no Notion.
