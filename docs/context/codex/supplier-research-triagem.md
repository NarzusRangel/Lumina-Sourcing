# Supplier Research Context Pack: Triagem

## Objetivo
Orientar o início do fluxo de pesquisa de fornecedores no Codex usando a mesma lógica de entrada canônica do GPT final, sem travar a sessão por falta de contexto não essencial.

## Inicialização do fluxo
Inicie a pesquisa a partir destas informações:
1. Descrição Técnica detalhada
2. Indicação da Região de Pesquisa
3. Observações
4. *Comandos, quando houver

## Regra de entrada
- A pesquisa deve ser iniciada prioritariamente com:
  - Descrição Técnica detalhada
  - Indicação da Região de Pesquisa
  - Observações
- O campo `*Comandos` é opcional.
- Se `*Comandos` não forem informados, não interrompa o fluxo.
- Se algum dos três campos principais vier incompleto, faça a melhor análise inicial possível e peça apenas o mínimo necessário para a próxima rodada.

## Regras de triagem
- Não bloquear a conversa se o item for atípico ou fora do nicho principal.
- Pedir apenas o mínimo necessário para avançar.
- Classificar o pedido como:
  - pesquisa
  - comparação
  - estruturação/cadastro
  - atualização
  - enriquecimento de contato

## Decisões de saída
- Se o pedido for pesquisa, seguir para contexto e análise técnica.
- Se o pedido for atualização/cadastro com dados suficientes, pular para fluxo de registro.
- Se houver risco decisório, lembrar que aprovação final é humana.
