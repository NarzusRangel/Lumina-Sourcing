# Checklist de Reescrita Manual da Skill

Use este documento como roteiro de manutencao manual da skill `orquestrador-de-pesquisa-de-fornecedores`.

Objetivo:
- manter uma ordem clara de reescrita
- evitar retrabalho
- garantir consistencia entre `SKILL.md`, referencias e camada de Notion

## Ordem de execucao

- [ ] `SKILL.md`
- [ ] `instrucao-canonica-de-pesquisa.md`
- [ ] `regras-canonicas.md`
- [ ] `analise-tecnica-e-shortlist.md`
- [ ] `formato-da-resposta.md`
- [ ] `modelo-card-fornecedor.md`
- [ ] `contratos-dos-comandos.md`
- [ ] `triagem-de-pesquisa.md`
- [ ] `fluxos-de-busca.md`
- [ ] `fluxos-de-registro.md`
- [ ] `fluxos-de-atualizacao.md`
- [ ] `perguntas-obrigatorias-por-entidade.md`
- [ ] `entidades-e-relacionamentos.md`
- [ ] `propriedades-reais-das-bases.md`
- [ ] `regras-de-cadastro.md`
- [ ] `registro-notion-operacional.md`
- [ ] `modelos-de-payload.md`
- [ ] `openai.yaml`
- [ ] `0.2.refatoracao-skill-orquestrador-de-pesquisa-de-fornecedores.md`

## Etapa 1: Contrato Central

### `SKILL.md`
- [ ] Reescrever o papel da skill em 1 frase
- [ ] Revisar principios centrais
- [ ] Confirmar comandos publicos
- [ ] Reescrever o roteamento por intencao
- [ ] Reescrever o comportamento padrao
- [ ] Revisar o `safe-write gate`
- [ ] Revisar a ordem de leitura por fluxo

Direcao:
- manter curto e mandatorio
- usar como orquestrador, nao como referencia extensa
- deixar explicito o que a skill faz e o que ela nunca pode fazer

## Etapa 2: Logica de Pesquisa

### `instrucao-canonica-de-pesquisa.md`
- [ ] Revisar entrada minima
- [ ] Revisar regra de destravamento
- [ ] Revisar como agir sem fabricante
- [ ] Revisar como agir sem regiao
- [ ] Revisar quantidade de perguntas por rodada

Direcao:
- nao travar por falta de contexto nao essencial
- pedir so o minimo necessario para avancar

### `regras-canonicas.md`
- [ ] Revisar hierarquia de fontes
- [ ] Revisar regras obrigatorias
- [ ] Revisar regra de verdade
- [ ] Revisar regra de citacao operacional
- [ ] Revisar regra de saida

Direcao:
- definir claramente fato, inferencia e ausencia de dado
- resolver aqui qualquer duvida sobre o que pode ou nao ser afirmado

### `analise-tecnica-e-shortlist.md`
- [ ] Revisar entregavel obrigatorio
- [ ] Revisar composicao da shortlist
- [ ] Revisar ordem recomendada da shortlist
- [ ] Revisar regra de transparencia

Direcao:
- deixar claro quando entra fabricante, distribuidor e revendedor
- impedir shortlist inflada ou artificial

## Etapa 3: Contrato de Saida

### `formato-da-resposta.md`
- [ ] Revisar ordem fixa das secoes
- [ ] Revisar obrigatoriedade de cada secao
- [ ] Revisar frases padrao de fallback
- [ ] Revisar regra de proximo passo

Direcao:
- transformar a resposta em molde fixo
- garantir repetibilidade entre sessoes

### `modelo-card-fornecedor.md`
- [ ] Revisar ordem dos campos
- [ ] Revisar campos minimos
- [ ] Revisar campos opcionais
- [ ] Revisar o que nunca incluir
- [ ] Revisar como marcar dado nao confirmado

Direcao:
- nao preencher por suposicao
- manter o card consistente e enxuto

## Etapa 4: Fluxos dos Comandos

### `contratos-dos-comandos.md`
- [ ] Revisar entrada minima de cada comando
- [ ] Revisar perguntas permitidas
- [ ] Revisar saida esperada
- [ ] Revisar condicao de encerramento

Direcao:
- tratar este arquivo como contrato publico dos comandos

### `triagem-de-pesquisa.md`
- [ ] Revisar sinais de partida
- [ ] Revisar classificacao do pedido
- [ ] Revisar decisoes de saida
- [ ] Revisar gatilhos de pausa

Direcao:
- decidir rapido o fluxo
- rotear sem repetir o contrato detalhado da pesquisa

### `fluxos-de-busca.md`
- [ ] Revisar `contato`
- [ ] Revisar `fornecedor`
- [ ] Revisar `material`

### `fluxos-de-registro.md`
- [ ] Revisar `fornecedor`
- [ ] Revisar `contato`
- [ ] Revisar `material`

### `fluxos-de-atualizacao.md`
- [ ] Revisar `fornecedor`
- [ ] Revisar `contato`
- [ ] Revisar `material`

### `perguntas-obrigatorias-por-entidade.md`
- [ ] Revisar checklist de `fornecedor`
- [ ] Revisar checklist de `contato`
- [ ] Revisar checklist de `material`

Direcao para todos os arquivos de comandos:
- responder sempre:
- [ ] o que preciso saber
- [ ] o que posso inferir
- [ ] o que preciso confirmar
- [ ] o que entrego ao final

## Etapa 5: Camada de Notion

### `entidades-e-relacionamentos.md`
- [ ] Revisar entidades principais
- [ ] Revisar relacionamentos
- [ ] Revisar leitura operacional
- [ ] Revisar logica de papeis comerciais
- [ ] Revisar regra de interpretacao

Direcao:
- resolver aqui a logica entre material, fornecedor, contato, fabricante, distribuidor e revendedor

### `propriedades-reais-das-bases.md`
- [ ] Revisar propriedades por base
- [ ] Revisar diferencas criticas
- [ ] Revisar observacoes de uso

Direcao:
- usar como fonte de verdade dos nomes dos campos
- evitar qualquer floreio

### `regras-de-cadastro.md`
- [ ] Revisar regras fixas
- [ ] Revisar relacoes obrigatorias
- [ ] Revisar curadoria minima
- [ ] Revisar travas antes de registrar

Direcao:
- consolidar aqui as travas de escrita
- deixar a qualidade do banco protegida

### `registro-notion-operacional.md`
- [ ] Revisar regras de escrita
- [ ] Revisar preview minimo obrigatorio
- [ ] Revisar saida esperada

Direcao:
- padronizar exatamente o que aparece antes de pedir autorizacao

### `modelos-de-payload.md`
- [ ] Revisar preview de criar fornecedor
- [ ] Revisar preview de criar contato
- [ ] Revisar preview de criar item normalizado
- [ ] Revisar preview de atualizar registro

Direcao:
- manter exemplos curtos
- manter exemplos canonicos
- nao inventar campos extras

## Etapa 6: Metadata

### `openai.yaml`
- [ ] Revisar `short_description`
- [ ] Revisar `default_prompt`

Direcao:
- ajustar so depois que o conteudo da skill estiver maduro
- refletir a skill final, nao guiar a escrita dela

## Etapa 7: Fechamento

### `0.2.refatoracao-skill-orquestrador-de-pesquisa-de-fornecedores.md`
- [ ] Atualizar tasks
- [ ] Atualizar dev notes
- [ ] Atualizar testing
- [ ] Atualizar completion notes
- [ ] Atualizar file list

Direcao:
- registrar mudanca de comportamento
- nao registrar apenas mudanca de arquivo

## Regra de Ouro

Em cada arquivo, confirme se ele responde com clareza:

- [ ] o que a skill deve fazer
- [ ] o que ela nao pode fazer
- [ ] o que ela pode inferir
- [ ] o que ela precisa confirmar
- [ ] o que ela deve entregar no final

## Validacao Manual Final

- [ ] A skill faz poucas perguntas e nao trava sem motivo
- [ ] O output de `*pesquisar` sai sempre na mesma estrutura
- [ ] Nenhuma escrita em Notion aparece sem preview e sem autorizacao
- [ ] Nao ha contradicao entre `SKILL.md` e as referencias
- [ ] A terminologia esta consistente em toda a skill
