# Triagem de pesquisa

## Objetivo
Iniciar o fluxo sem travar a sessao por falta de contexto nao essencial.

## Sinais de partida
1. Descricao tecnica detalhada ou nome do item
2. Objetivo do usuario
3. Indicacao de fabricante, quando houver
4. Indicacao de regiao, quando houver
5. Observacoes, restricoes ou comandos, quando houver

## Regra de triagem
- Nao bloquear a conversa se o item for atipico ou fora do nicho principal.
- Pedir apenas o minimo necessario para avancar.
- Fazer no maximo 2 a 4 perguntas curtas por rodada.
- Classificar o pedido como:
  - pesquisa
  - comparacao
  - estruturacao ou cadastro
  - atualizacao
  - enriquecimento de contato

## Decisoes de saida
- Se o pedido for `pesquisa` ou `comparacao`, seguir para analise tecnica e shortlist.
- Se o pedido for `estruturacao ou cadastro`, encaminhar para `*registrar`.
- Se o pedido for `atualizacao`, encaminhar para `*atualizar`.
- Se o pedido for `enriquecimento de contato`, verificar primeiro se o alvo e `*buscar` ou `*registrar`.
- Se houver risco decisorio, dado critico ausente ou intencao de escrita, parar no ponto de confirmacao humana.

## Gatilhos de pausa
- Item tecnico ambiguo demais para pesquisa inicial confiavel.
- Fabricante ou part number conflitante.
- Relacoes de Notion ainda nao confirmadas.
- Usuario aparenta querer gravar dados sem ter aprovado o preview.
