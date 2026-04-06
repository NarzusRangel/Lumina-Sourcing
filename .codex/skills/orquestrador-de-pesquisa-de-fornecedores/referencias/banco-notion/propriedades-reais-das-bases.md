# Propriedades reais das bases

Use apenas estes nomes nos payloads e previews. Nao renomeie propriedades.

## `Fornecedores`
- `Nome do fornecedor`
- `Tipo de fornecedor`
- `País/Região`
- `Site`
- `Observações`
- `Tipos de materiais atendidos`
- `Responsável pelo cadastro`
- `Status do fornecedor`
- `Contatos relacionados`
- `Itens relacionados`

## `Contatos de Fornecedores`
- `E-mail`
- `Nome do contato`
- `Cargo`
- `Telefone`
- `Fornecedores Relacionados`
- `Observações`
- `Responsável pelo cadastro`
- `Status do contato`

## `Catalogo de Materiais / Componentes`
- `Nome do item normalizado`
- `Fornecedores Relacionados`
- `NCM provável`
- `Observações técnicas`
- `Tipos de materiais / família`
- `Responsável`
- `Criado em`
- `Atualizado em`

## Diferencas criticas operacionais
- `Fornecedores` e `Contatos de Fornecedores` usam `Responsavel pelo cadastro`.
- `Catalogo de Materiais / Componentes` usa `Responsavel`.
- `Contatos relacionados`, `Fornecedores Relacionados` e `Itens relacionados` sao relacoes e devem ser tratadas como tal.
- Os vocabularios de familia/material ainda nao sao identicos entre as bases.

## Observacoes de uso
- Em busca, mostre apenas as propriedades relevantes para a pergunta do usuario.
- Em registro e atualizacao, monte preview usando os nomes exatos acima.
- Nao invente propriedades auxiliares fora do preview textual da skill.

