# Registro Notion operacional

## Objetivo
Orientar cadastro e atualizacao de fornecedores, contatos e materiais no Notion com autorizacao explicita do usuario.

## Regras de escrita
- Nenhuma gravacao ocorre sem comando explicito do usuario.
- `1 e-mail = 1 contato`
- O mesmo e-mail pode aparecer em mais de um registro quando estiver ligado a fornecedores diferentes.
- Novos contatos devem ser adicionados, nao substituir contatos antigos automaticamente.
- O item gravado no catalogo deve ser normalizado, nao copiado como texto bruto da pesquisa.

## Bases operacionais
- `Fornecedores`
- `Contatos de Fornecedores`
- `Catalogo de Materiais / Componentes`

## Saida esperada
- payload de cadastro ou atualizacao pronto para gravacao
- indicacao clara da operacao alvo
- lista de lacunas, quando houver
- confirmacao textual de que a gravacao depende de autorizacao do usuario
