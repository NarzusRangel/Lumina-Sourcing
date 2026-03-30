# Supplier Research Context Pack: Registro Notion

## Objetivo
Orientar cadastro e atualização de fornecedores e contatos no Notion com autorização explícita do usuário.

## Regras de escrita
- Nenhuma gravação ocorre sem comando explícito do usuário.
- `1 e-mail = 1 contato`
- O mesmo e-mail pode aparecer em mais de um registro quando estiver ligado a fornecedores diferentes.
- Novos contatos devem ser adicionados, não substituir contatos antigos automaticamente.
- O item gravado no catálogo deve ser normalizado, não copiado como texto bruto da pesquisa.

## Bases operacionais
- `Fornecedores`
- `Contatos de Fornecedores`
- `Catalogo de Materiais/Componentes`

## Campos mínimos para contato
- E-mail
- Nome do contato, se houver
- Telefone, se houver
- Fornecedor relacionado
- Marcas/Fabricantes relacionados
- Origem do contato

## Saída esperada
- Payload de cadastro/atualização pronto para gravação
- Indicação clara da operação alvo (`criar` ou `atualizar`)
- Lista de lacunas, se houver campos insuficientes
- Confirmação textual de que a gravação depende de autorização do usuário

## Saída esperada para catálogo
- Nome do item normalizado
- Segmento
- NCM provável
- Fornecedores Relacionados
- Observações técnicas
