# Modelos de payload

## Criar fornecedor
```json
{
  "operacao": "criar fornecedor",
  "base": "Fornecedores",
  "campos": {
    "Nome do fornecedor": "",
    "Tipo de fornecedor": [],
    "País/Região": [],
    "Site": "",
    "Tipos de materiais atendidos": [],
    "Responsável pelo cadastro": [],
    "Status do fornecedor": "",
    "Observações": ""
  }
}
```

## Criar contato
```json
{
  "operacao": "criar contato",
  "base": "Contatos de Fornecedores",
  "campos": {
    "E-mail": "",
    "Nome do contato": "",
    "Cargo": [],
    "Telefone": "",
    "Fornecedores Relacionados": [],
    "Responsável pelo cadastro": [],
    "Status do contato": "",
    "Observações": ""
  }
}
```

## Criar item normalizado
```json
{
  "operacao": "criar item normalizado",
  "base": "Catalogo de Materiais / Componentes",
  "campos": {
    "Nome do item normalizado": "",
    "Fornecedores Relacionados": [],
    "NCM provável": "",
    "Tipos de materiais / família": [],
    "Observações técnicas": "",
    "Responsável": []
  }
}
```

## Atualizar registro
```json
{
  "operacao": "atualizar",
  "base": "",
  "registro_alvo": "",
  "campos_alterados": {}
}
```
