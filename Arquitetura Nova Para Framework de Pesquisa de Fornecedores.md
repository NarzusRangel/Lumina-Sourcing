## A. Mapa da arquitetura documental

**Princípio central:** a base-mãe vive em `00_fundacao`, `01_operacao` e `02_qualidade`. `03_chatgpt_web` e `04_codex` não reinventam regra; apenas derivam, simplificam e adaptam.

```text
Base-mãe normativa
→ operação e decisão
→ padrões de qualidade
→ adaptadores por canal
→ artefatos executáveis
→ integrações e memória operacional
→ governança e melhoria contínua
```

| Macrocamada | Papel | Produz | Deriva para |
|---|---|---|---|
| Visão geral do sistema | Define propósito, arquitetura lógica e premissas | narrativa-mãe | GPT instructions, AGENTS.md, onboarding |
| Escopo e limites | Define o que entra, o que não entra e o que exige escalonamento | fronteiras | guardrails, handoff rules |
| Perfis de usuários | Separa necessidades por público, maturidade e autonomia | personas operacionais | Projects, fluxos, respostas |
| Taxonomia de demandas | Classifica tipos de pedidos e rotas de tratamento | classes de demanda | roteamento, skills, templates |
| Fluxos operacionais | Traduz demanda em fases, decisões e saídas | playbooks | comandos, fases, checklists |
| Padrões de resposta | Define formato, densidade, tom, evidência e CTA | response contracts | ChatGPT Web e Codex |
| Critérios de qualidade | Define gate de aceitação | checklist e score | revisão humana, QA de prompt |
| Exemplos e casos reais | Mostra o bom, o ruim e o aceitável | biblioteca exemplificada | treinamento, calibração |
| Base de conhecimento e contexto | Organiza conhecimento estável e contexto volátil | references, context packs | knowledge files, skill context |
| Arquitetura ChatGPT Web | Define instruções simples, Projects e arquivos de apoio | setup Web | Projects, instructions, starters |
| Arquitetura Codex | Define AGENTS.md, SKILL.md, context packs e comandos | setup Codex | skills, phases, automações |
| Arquitetura de integrações e MCP | Define eventos, registros, campos, sync e auditoria | contrato de integração | Notion/database, MCP tools |
| Governança, versionamento e melhoria contínua | Controla dono, revisão, mudança e depreciação | cadência de manutenção | changelog, ADR, revisão trimestral |

**Regra de ouro de derivação**

- Regra comportamental global nasce na base-mãe.
- Conhecimento de referência nasce em `references/`.
- Contexto de execução nasce em `context/`.
- Exemplo nunca substitui regra.
- Memória operacional nunca substitui documento normativo.
- ChatGPT Web recebe a versão mínima viável da regra.
- Codex recebe a versão operacional detalhada da mesma regra.

---

## B. Árvore de pastas e arquivos

```text
/docs
├── 00_fundacao
│   ├── 00_visao-geral-do-sistema.md
│   ├── 01_escopo-e-limites.md
│   ├── 02_perfis-de-usuarios.md
│   ├── 03_taxonomia-de-demandas.md
│   └── 04_modelo-de-derivacao-documental.md
├── 01_operacao
│   ├── 00_fluxo-operacional-por-fases.md
│   ├── 01_matriz-de-triagem.md
│   ├── 02_contexto-operacional-minimo.md
│   └── 03_matriz-canal-por-cenario.md
├── 02_qualidade
│   ├── 00_padrao-de-resposta.md
│   ├── 01_criterios-de-qualidade.md
│   ├── 02_erros-comuns-e-antipadroes.md
│   └── 03_politica-de-exemplos.md
├── 03_chatgpt_web
│   ├── 00_arquitetura-chatgpt-web.md
│   ├── 01_gpt-instructions-source.md
│   ├── 02_knowledge-files-map.md
│   └── 03_projects-organization.md
├── 04_codex
│   ├── 00_arquitetura-codex.md
│   ├── 01_agents-md-source.md
│   ├── 02_skill-catalog-and-pattern.md
│   ├── 03_context-pack-structure.md
│   └── 04_comandos-por-fase.md
├── 05_integracoes
│   ├── 00_arquitetura-integracoes-e-mcp.md
│   ├── 01_modelo-notion-operacional.md
│   ├── 02_eventos-campos-e-mapeamentos.md
│   └── 03_politica-de-sincronizacao-e-auditoria.md
├── 06_templates
│   ├── template_visao-geral-do-sistema.md
│   ├── template_escopo-e-limites.md
│   ├── template_perfis-de-usuarios.md
│   ├── template_taxonomia-de-demandas.md
│   ├── template_fluxo-operacional-por-fases.md
│   ├── template_padrao-de-resposta.md
│   ├── template_criterios-de-qualidade.md
│   ├── template_exemplos-bons-e-ruins.md
│   ├── template_arquitetura-chatgpt-web.md
│   ├── template_arquitetura-codex.md
│   ├── template_skill.md
│   ├── template_mcp_notion.md
│   └── template_governanca-e-versionamento.md
├── 07_examples
│   ├── 00_exemplos-bons-e-ruins.md
│   ├── 01_casos-reais-chatgpt-web.md
│   └── 02_casos-reais-codex.md
├── 08_governanca
│   ├── 00_governanca-e-versionamento.md
│   ├── 01_convencoes-de-organizacao.md
│   ├── 02_log-de-decisoes-documentais.md
│   └── 03_ritual-de-revisao-e-melhoria.md
├── references
│   ├── conhecimento-estavel/
│   ├── dominio/
│   ├── negocio/
│   └── compliance/
├── context
│   ├── chatgpt-web/
│   ├── codex/
│   └── operacao/
└── memory
    ├── registros-locais/
    └── export-mcp/
```

---

## C. Catálogo de documentos

### Núcleo normativo

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_visao-geral-do-sistema.md` | alinhar visão | evitar interpretações divergentes | objetivo, proposta, arquitetura lógica, princípios | liderança, arquitetura, curadoria IA | início |
| `01_escopo-e-limites.md` | definir fronteiras | reduzir invenção e sobrecarga | dentro, fora, escalonamento, riscos | todos | antes de detalhar fluxos |
| `02_perfis-de-usuarios.md` | separar públicos | evitar instrução única para todos | segmentos, necessidades, nível de autonomia | dono da operação, enablement | antes dos canais |
| `03_taxonomia-de-demandas.md` | classificar pedidos | garantir roteamento consistente | tipos, subtipos, exemplos, rota | operação, curadoria, futuros MCPs | antes de comandos e skills |
| `04_modelo-de-derivacao-documental.md` | definir como derivar | impedir duplicação inconsistente | fonte, adaptador, artefato, regra de prevalência | mantenedores | antes de implementar Web/Codex |

### Operação

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_fluxo-operacional-por-fases.md` | desenhar o fluxo padrão | padronizar execução | fases, entradas, saídas, handoffs | operação e designers de agente | após taxonomia |
| `01_matriz-de-triagem.md` | decidir rota | reduzir ambiguidade | tipo de demanda x canal x complexidade | triagem, líderes | no recebimento |
| `02_contexto-operacional-minimo.md` | definir contexto mínimo | evitar respostas sem base | insumos obrigatórios, opcionais e faltantes | usuários e agentes | antes da execução |
| `03_matriz-canal-por-cenario.md` | alocar por canal | evitar uso errado de ferramenta | quando usar Web, Codex, humano, MCP | gestão de adoção | rollout |

### Qualidade

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_padrao-de-resposta.md` | padronizar saídas | garantir consistência | forma, profundidade, CTA, evidência | autores de prompt e skill | na construção de respostas |
| `01_criterios-de-qualidade.md` | medir qualidade | permitir revisão objetiva | clareza, utilidade, rastreabilidade, segurança | QA, curadoria | validação |
| `02_erros-comuns-e-antipadroes.md` | capturar falhas | reduzir reincidência | exemplos de má prática | curadoria, treinamento | revisão |
| `03_politica-de-exemplos.md` | governar exemplos | evitar que exemplos virem regra | origem, anonimização, validade | curadoria | publicação |

### ChatGPT Web

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_arquitetura-chatgpt-web.md` | definir a implementação Web | maximizar adoção com simplicidade | instructions, Projects, knowledge files, limites | admins e curadoria | fase Web |
| `01_gpt-instructions-source.md` | ser a fonte do texto-base | evitar editar instrução diretamente na UI | versão curta, regras e tom | curadoria | antes de publicar projeto |
| `02_knowledge-files-map.md` | mapear knowledge files | organizar contexto estável | lista de arquivos, propósito e atualização | curadoria | setup de Projects |
| `03_projects-organization.md` | modelar Projects | organizar por domínio e uso | nomes de projects, objetivo, público | admins | rollout |

### Codex

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_arquitetura-codex.md` | definir modelo avançado | separar operação rica do Web | AGENTS.md, skills, context packs, fases | mantenedores técnicos | fase Codex |
| `01_agents-md-source.md` | ser a fonte do AGENTS.md | evitar drift | princípios, guardrails, fluxos, comandos | mantenedores | setup Codex |
| `02_skill-catalog-and-pattern.md` | catalogar skills | impedir skill redundante | skill id, objetivo, entradas, saídas | curadoria técnica | expansão |
| `03_context-pack-structure.md` | organizar contexto carregável | reduzir contexto inútil | packs por fase, domínio e tarefa | usuários avançados | execução |
| `04_comandos-por-fase.md` | definir comandos guiados | tornar o uso repetível | fase, comando, objetivo, saída esperada | usuários Codex | operação diária |

### Integrações

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_arquitetura-integracoes-e-mcp.md` | desenhar a camada externa | preparar evolução sem acoplamento | princípios, fluxos, segurança, eventos | arquitetura e automação | antes do MCP |
| `01_modelo-notion-operacional.md` | definir banco operacional | padronizar registros | databases, entidades, campos | operações e automação | implantação Notion |
| `02_eventos-campos-e-mapeamentos.md` | mapear dados | evitar integração frouxa | evento, origem, payload, destino | devs de integração | implementação |
| `03_politica-de-sincronizacao-e-auditoria.md` | controlar sync | proteger histórico e confiabilidade | frequência, owner, logs, falhas | operação e compliance | go-live |

### Governança e apoio

| Arquivo | Objetivo | Por que existe | Conteúdo | Quem usa | Quando entra |
|---|---|---|---|---|---|
| `00_governanca-e-versionamento.md` | definir governança | manter documentação viva | owner, revisão, aprovação, semver | todos os mantenedores | após fundação |
| `01_convencoes-de-organizacao.md` | padronizar forma | acelerar manutenção | nomes, numeração, front matter, status | todos | desde o primeiro doc |
| `02_log-de-decisoes-documentais.md` | registrar decisões | preservar racional | ADRs documentais | liderança e mantenedores | cada mudança relevante |
| `03_ritual-de-revisao-e-melhoria.md` | definir cadência | garantir evolução contínua | agenda, critérios, backlog | governança | operação contínua |

---

## D. Templates base em Markdown

### 1. Visão geral do sistema

```md
# Visão Geral do Sistema

## Objetivo
Definir o propósito do sistema de agentes, seus resultados esperados e sua arquitetura lógica.

## Instruções de preenchimento
Preencha este documento antes de criar instruções, skills ou integrações.

## Seções internas
### 1. Contexto do negócio
### 2. Problema que o sistema resolve
### 3. Objetivos principais
### 4. Resultados esperados
### 5. Canais suportados
### 6. Princípios arquiteturais
### 7. Restrições relevantes

## Perguntas guiadas
- Que problema operacional este sistema reduz?
- O que precisa ficar mais rápido, mais claro ou mais consistente?
- O que nunca deve depender de memória tácita?

## Como brainstormar este documento
- Pense antes: qual dor real será padronizada?
- Decisões que ele suporta: desenho dos canais, priorização, limites.
- Reflexões: onde a IA ajuda, onde só assiste, onde não deve atuar?
- Exemplo bom: “reduzir variação de resposta entre analistas e acelerar triagem”.
- Armadilha comum: escrever visão genérica sem efeito operacional.
- Bom o suficiente: qualquer novo mantenedor entende propósito, fronteira e direção.

## Checklist final
- [ ] O objetivo está mensurável
- [ ] Há limites explícitos
- [ ] Os canais estão nomeados
- [ ] Os princípios são reutilizáveis
```

### 2. Escopo e limites

```md
# Escopo e Limites

## Objetivo
Definir o que o sistema cobre, o que não cobre e quando escalar para humano.

## Instruções de preenchimento
Escreva em formato decisório, não em narrativa vaga.

## Seções internas
### 1. Dentro do escopo
### 2. Fora do escopo
### 3. Casos limítrofes
### 4. Regras de escalonamento
### 5. Riscos de extrapolação

## Perguntas guiadas
- Quais tarefas são permitidas?
- O que exige validação humana?
- Em que cenário a IA deve recusar ou redirecionar?

## Como brainstormar este documento
- Pense antes: onde a equipe costuma pedir “só mais uma coisa”?
- Decisões que ele suporta: recusa, handoff, guardrail.
- Reflexões: o que parece próximo, mas não deveria entrar?
- Exemplo bom: “resumir, classificar, estruturar e recomendar; não aprovar contrato”.
- Armadilha comum: deixar “análise estratégica” amplo demais.
- Bom o suficiente: dois revisores independentes chegariam à mesma decisão.

## Checklist final
- [ ] Escopo positivo definido
- [ ] Fora de escopo explícito
- [ ] Handoff humano claro
- [ ] Casos ambíguos tratados
```

### 3. Perfis de usuários

```md
# Perfis de Usuários

## Objetivo
Segmentar públicos para definir experiência, linguagem, profundidade e autonomia.

## Instruções de preenchimento
Crie perfis operacionais, não personas de marketing.

## Seções internas
### 1. Perfil
### 2. Objetivo principal
### 3. Nível de familiaridade com IA
### 4. Dores e riscos
### 5. Canal recomendado
### 6. Tipo de suporte necessário

## Perguntas guiadas
- Quem usa o sistema no dia a dia?
- Quem só consulta?
- Quem cria e mantém o sistema?

## Como brainstormar este documento
- Pense antes: quais diferenças mudam a operação?
- Decisões que ele suporta: simplificação, permissões, treinamento.
- Reflexões: que perfil precisa de caminho guiado e qual precisa de liberdade?
- Exemplo bom: colaborador geral, operador avançado, curador, mantenedor técnico.
- Armadilha comum: perfis demais sem consequência prática.
- Bom o suficiente: cada perfil gera uma regra de uso diferente.

## Checklist final
- [ ] Perfis são acionáveis
- [ ] Cada perfil tem canal recomendado
- [ ] Há distinção de autonomia
- [ ] Há risco principal por perfil
```

### 4. Taxonomia de demandas

```md
# Taxonomia de Demandas

## Objetivo
Classificar pedidos para roteamento, padronização e medição.

## Instruções de preenchimento
Use categorias mutuamente úteis, não perfeitas.

## Seções internas
### 1. Categoria
### 2. Subcategoria
### 3. Sinais de identificação
### 4. Entrada mínima
### 5. Saída esperada
### 6. Canal ideal
### 7. Exemplo real

## Perguntas guiadas
- Quais pedidos se repetem?
- O que diferencia uma análise de uma execução?
- O que requer contexto estável versus contexto de caso?

## Como brainstormar este documento
- Pense antes: quais classes mudam o fluxo?
- Decisões que ele suporta: triagem, templates, skills.
- Reflexões: categorias estão úteis para operação ou só bonitas?
- Exemplo bom: consulta, síntese, estruturação, comparação, decisão assistida, execução guiada.
- Armadilha comum: taxonomia por assunto em vez de por tipo de trabalho.
- Bom o suficiente: 80% dos pedidos entram com pouca dúvida.

## Checklist final
- [ ] Categorias cobrem a maioria dos casos
- [ ] Cada categoria muda a forma de operar
- [ ] Há exemplos reais
- [ ] Há vínculo com canal e saída
```

### 5. Fluxo operacional por fases

```md
# Fluxo Operacional por Fases

## Objetivo
Transformar demanda em uma sequência repetível de decisão e entrega.

## Instruções de preenchimento
Descreva fases com entrada, ação, decisão e saída.

## Seções internas
### 1. Fase
### 2. Objetivo da fase
### 3. Entrada mínima
### 4. Ação do agente
### 5. Critério de decisão
### 6. Saída
### 7. Próxima fase

## Perguntas guiadas
- Como começa um atendimento?
- Onde validar contexto insuficiente?
- Em que momento registrar memória operacional?

## Como brainstormar este documento
- Pense antes: onde hoje há retrabalho?
- Decisões que ele suporta: comandos, handoffs, automação.
- Reflexões: qual etapa evita erro cedo?
- Exemplo bom: triagem → enquadramento → execução → revisão → registro.
- Armadilha comum: confundir fase com ferramenta.
- Bom o suficiente: qualquer operador novo consegue seguir o fluxo.

## Checklist final
- [ ] Toda fase tem entrada e saída
- [ ] Há ponto de revisão
- [ ] Há critério de escalonamento
- [ ] Há registro final
```

### 6. Padrão de resposta

```md
# Padrão de Resposta

## Objetivo
Definir formato, densidade, tom e estrutura mínima das respostas.

## Instruções de preenchimento
Especifique o contrato da resposta por tipo de demanda.

## Seções internas
### 1. Princípios de resposta
### 2. Estrutura padrão
### 3. Variações por demanda
### 4. Nível de detalhe
### 5. Regras de clareza
### 6. CTA ou próximo passo

## Perguntas guiadas
- O que a resposta precisa permitir fazer em seguida?
- Quando usar síntese versus detalhamento?
- Como evitar excesso de texto?

## Como brainstormar este documento
- Pense antes: que respostas hoje parecem corretas mas inúteis?
- Decisões que ele suporta: UX textual, consistência, adoção.
- Reflexões: qual é a menor resposta ainda útil?
- Exemplo bom: começo direto, estrutura estável, próximos passos claros.
- Armadilha comum: responder como aula em vez de como entrega.
- Bom o suficiente: a resposta é executável sem retrabalho.

## Checklist final
- [ ] Há formato padrão
- [ ] Há regra para profundidade
- [ ] Há variação por tipo de demanda
- [ ] Há próximo passo claro
```

### 7. Critérios de qualidade

```md
# Critérios de Qualidade

## Objetivo
Definir como avaliar se um artefato de IA está pronto para uso.

## Instruções de preenchimento
Use critérios observáveis e revisáveis.

## Seções internas
### 1. Critério
### 2. Definição
### 3. Evidência esperada
### 4. Nível mínimo aceitável
### 5. Falhas típicas

## Perguntas guiadas
- O que torna uma resposta útil, segura e confiável?
- O que é bloqueante?
- O que é apenas melhoria?

## Como brainstormar este documento
- Pense antes: o que já gerou erro ou constrangimento?
- Decisões que ele suporta: revisão, publicação, retrabalho.
- Reflexões: quais critérios são realmente auditáveis?
- Exemplo bom: clareza, aderência ao escopo, rastreabilidade, completude, ação.
- Armadilha comum: critério bonito sem forma de verificar.
- Bom o suficiente: dois revisores chegam a parecer semelhante.

## Checklist final
- [ ] Critérios são auditáveis
- [ ] Há severidade por falha
- [ ] Há evidência esperada
- [ ] Há mínimo aceitável
```

### 8. Exemplos bons e ruins

```md
# Exemplos Bons e Ruins

## Objetivo
Calibrar comportamento por contraste entre saída desejada e indesejada.

## Instruções de preenchimento
Use exemplos curtos, contextualizados e anotados.

## Seções internas
### 1. Cenário
### 2. Exemplo bom
### 3. Por que é bom
### 4. Exemplo ruim
### 5. Por que é ruim
### 6. Lição operacional

## Perguntas guiadas
- O que um bom operador reconhece imediatamente?
- Que erro parece convincente, mas falha no uso real?
- Que exemplos ajudam treinamento?

## Como brainstormar este documento
- Pense antes: onde as pessoas elogiam respostas que não servem?
- Decisões que ele suporta: treinamento, QA, melhoria.
- Reflexões: o exemplo ruim falha por quê?
- Exemplo bom: resposta curta, contextual, orientada a ação.
- Armadilha comum: exemplo artificial demais.
- Bom o suficiente: o contraste ensina algo operacional.

## Checklist final
- [ ] Há contraste claro
- [ ] O cenário é realista
- [ ] A lição está explícita
- [ ] O exemplo ruim não é caricato
```

### 9. Arquitetura ChatGPT Web

```md
# Arquitetura ChatGPT Web

## Objetivo
Definir como a base-mãe vira uma experiência simples e consistente no ChatGPT Web.

## Instruções de preenchimento
Documente a camada Web como adaptador, não como origem de regra.

## Seções internas
### 1. Objetivo do canal
### 2. Público-alvo
### 3. GPT instructions base
### 4. Projects e knowledge files
### 5. Limites do canal
### 6. Casos de uso
### 7. Regras de manutenção

## Perguntas guiadas
- O que deve ficar invisível para simplificar?
- O que deve estar sempre disponível no Project?
- O que deve ser remetido ao Codex?

## Como brainstormar este documento
- Pense antes: qual é a experiência mínima elegante?
- Decisões que ele suporta: Projects, knowledge, guardrails.
- Reflexões: o usuário comum precisa ver taxonomia ou só sentir consistência?
- Exemplo bom: instruções curtas, knowledge estável, comandos opcionais.
- Armadilha comum: levar complexidade do Codex para o Web.
- Bom o suficiente: um colaborador comum consegue usar sem treinamento longo.

## Checklist final
- [ ] O canal está simplificado
- [ ] Os limites estão claros
- [ ] Há mapa de knowledge files
- [ ] Há regra de encaminhamento ao Codex
```

### 10. Arquitetura Codex

```md
# Arquitetura Codex

## Objetivo
Definir a operação avançada no Codex com AGENTS.md, skills, contexto e fases.

## Instruções de preenchimento
Descreva os componentes operacionais e a relação entre eles.

## Seções internas
### 1. Objetivo do canal
### 2. Tipos de artefato
### 3. AGENTS.md derivado
### 4. Skills e critérios de criação
### 5. Context packs
### 6. Comandos por fase
### 7. Registros e handoffs

## Perguntas guiadas
- O que o Codex faz que o Web não deve fazer?
- Que conhecimento deve virar skill?
- Que contexto deve ser carregado sob demanda?

## Como brainstormar este documento
- Pense antes: onde a operação exige granularidade e memória de trabalho?
- Decisões que ele suporta: skill design, contexto, automação.
- Reflexões: o que é regra global e o que é habilidade local?
- Exemplo bom: AGENTS enxuto, skills focadas, contexto modular.
- Armadilha comum: transformar skill em depósito de conhecimento.
- Bom o suficiente: um mantenedor sabe criar ou revisar uma skill sem inventar padrão.

## Checklist final
- [ ] Papéis dos artefatos estão distintos
- [ ] Há critérios de criação de skill
- [ ] Há estratégia de contexto
- [ ] Há fases operacionais
```

### 11. Desenho de skill

```md
# Desenho de Skill

## Objetivo
Especificar uma skill reutilizável, com gatilho, escopo, entradas, saídas e limites.

## Instruções de preenchimento
Preencha uma skill por documento.

## Seções internas
### 1. Nome e ID
### 2. Problema que resolve
### 3. Quando usar
### 4. Quando não usar
### 5. Entradas mínimas
### 6. Saídas esperadas
### 7. Dependências de contexto
### 8. Checklist de qualidade

## Perguntas guiadas
- Esta skill resolve uma tarefa recorrente?
- O uso é claro o suficiente para não gerar sobreposição?
- O output é verificável?

## Como brainstormar este documento
- Pense antes: essa skill merece existir?
- Decisões que ele suporta: criação, fusão ou descarte.
- Reflexões: é melhor skill, template ou reference?
- Exemplo bom: escopo estreito, gatilho claro, saída repetível.
- Armadilha comum: skill ampla demais.
- Bom o suficiente: qualquer mantenedor identifica quando chamar ou não.

## Checklist final
- [ ] Há gatilho claro
- [ ] Há limite explícito
- [ ] Há entrada mínima
- [ ] Há output verificável
```

### 12. Desenho de MCP/Notion

```md
# Desenho de MCP/Notion

## Objetivo
Definir como eventos operacionais serão registrados e sincronizados com Notion via MCP.

## Instruções de preenchimento
Documente contrato de dados e governança, não só ferramentas.

## Seções internas
### 1. Objetivo da integração
### 2. Entidades registradas
### 3. Eventos gerados
### 4. Campos obrigatórios
### 5. Fluxo de sincronização
### 6. Auditoria e falhas
### 7. Segurança e permissões

## Perguntas guiadas
- O que vale registrar?
- Quem consome esses registros?
- Qual evento cria, atualiza ou encerra um item?

## Como brainstormar este documento
- Pense antes: que memória operacional hoje se perde?
- Decisões que ele suporta: schema, MCP, ownership.
- Reflexões: registro é para histórico, métrica ou execução?
- Exemplo bom: banco de solicitações, banco de entregas, banco de melhorias.
- Armadilha comum: registrar tudo sem propósito.
- Bom o suficiente: um dev consegue implementar o contrato sem adivinhar campo.

## Checklist final
- [ ] Entidades definidas
- [ ] Eventos mapeados
- [ ] Campos obrigatórios claros
- [ ] Política de auditoria definida
```

### 13. Governança e versionamento

```md
# Governança e Versionamento

## Objetivo
Definir como a documentação evolui, quem aprova e como mudanças são controladas.

## Instruções de preenchimento
Trate este documento como contrato operacional.

## Seções internas
### 1. Papéis e responsáveis
### 2. Status documentais
### 3. Política de revisão
### 4. Semver documental
### 5. Critérios de aprovação
### 6. Depreciação e substituição
### 7. Registro de mudanças

## Perguntas guiadas
- Quem pode propor, revisar e aprovar?
- O que exige revisão trimestral?
- Como evitar documentos órfãos?

## Como brainstormar este documento
- Pense antes: quem já cuida disso na prática?
- Decisões que ele suporta: ownership, cadência, manutenção.
- Reflexões: o que acontece se ninguém revisar?
- Exemplo bom: owner nominal, data de revisão, status, changelog.
- Armadilha comum: governança sem rito.
- Bom o suficiente: qualquer documento tem dono e próxima revisão.

## Checklist final
- [ ] Há owner por documento
- [ ] Há status padronizado
- [ ] Há cadência de revisão
- [ ] Há regra de depreciação
```

---

## E. Roadmap de construção

| Fase | Objetivo | Documentos a criar | Dependências futuras | Risco de pular | Sinal de maturidade |
|---|---|---|---|---|---|
| Fase 1: fundação | fixar a verdade base | visão geral, escopo, perfis, taxonomia, modelo de derivação | todas | divergência estrutural desde o início | há consenso sobre propósito, limites e públicos |
| Fase 2: operação | transformar visão em fluxo | fluxo por fases, triagem, contexto mínimo, matriz canal-cenário | qualidade, Web, Codex | operação inconsistente | casos reais já cabem no fluxo |
| Fase 3: qualidade | definir o que é bom | padrão de resposta, critérios, antipadrões, política de exemplos | publicação e revisão | respostas úteis porém despadronizadas | revisores conseguem reprovar com critério |
| Fase 4: implementação ChatGPT Web | criar a frente simples | arquitetura Web, instructions source, knowledge map, projects | adoção ampla | Web nasce confuso ou verboso | usuário comum usa sem depender de especialista |
| Fase 5: implementação Codex | criar a frente avançada | arquitetura Codex, AGENTS source, skill catalog, context packs, comandos | skills e futura automação | Codex vira repositório caótico | skill nova segue padrão único |
| Fase 6: integrações/MCP | preparar memória e registro | arquitetura MCP, modelo Notion, mapeamentos, auditoria | dashboards e automações | integração nasce sem contrato | campos e eventos já estão definidos |
| Fase 7: governança contínua | manter vivo e confiável | governança, convenções, ADR documental, ritual de revisão | evolução contínua | obsolescência e drift | toda mudança tem owner, status e revisão |

---

## F. Regras de organização e governança

| Tema | Regra |
|---|---|
| Nome de arquivo | `NN_nome-em-kebab-case.md` |
| Nome de pasta | `NN_categoria` para ordem fixa; `references`, `context`, `memory` sem numeração |
| Idioma | português para operação; inglês só em artefatos exigidos pela ferramenta |
| Front matter | `title`, `doc_id`, `version`, `status`, `owner`, `reviewed_at`, `next_review`, `derived_from` |
| Status | `draft`, `in_review`, `approved`, `deprecated`, `archived` |
| Versionamento | semver documental por arquivo: `0.x` enquanto em desenho, `1.0.0` ao aprovar, `minor` para expansão, `patch` para clareza |
| Dono | um owner nominal por documento; nunca “time” apenas |
| Revisão | toda peça aprovada tem `next_review` |
| Rascunho vs aprovado | rascunho usa `status: draft`; aprovado exige reviewer e data |
| Derivação | todo arquivo de canal deve apontar `derived_from` para a base-mãe |
| Mudanças relevantes | registrar em `02_log-de-decisoes-documentais.md` |
| Depreciação | documento depreciado aponta substituto e data-limite |
| Regra anti-drift | nunca editar GPT instruction final ou AGENTS.md sem atualizar primeiro a fonte documental correspondente |

**Front matter sugerido**

```yaml
---
title: "Nome do Documento"
doc_id: "DOC-00-001"
version: "0.1.0"
status: "draft"
owner: "Nome Sobrenome"
reviewed_at: "2026-03-29"
next_review: "2026-06-29"
derived_from: []
---
```

---

## G. Guia de onde cada informação deve morar

| Natureza da informação | Morada canônica | Também pode aparecer em | Não deve morar como fonte primária |
|---|---|---|---|
| Instruções de comportamento | `00_fundacao`, `01_operacao`, `02_qualidade` | GPT instructions, AGENTS.md, SKILL.md | chat solto, Notion operacional |
| Conhecimento de referência | `references/` | knowledge files, context packs | AGENTS.md, chat |
| Contexto operacional | `context/operacao` | Projects, Codex context pack | references estáveis |
| Exemplos | `07_examples` | knowledge files curados, treinamento | regra principal |
| Templates | `06_templates` | playbooks internos | chat, instructions finais |
| Configuração do ambiente | `03_chatgpt_web`, `04_codex` | Projects, AGENTS.md, arquivos locais | examples, references |
| Integração externa | `05_integracoes` | MCP configs, docs técnicas | GPT instructions |
| Memória/registros operacionais | `memory/`, MCP, Notion/database | dashboards e histórico | base normativa |

**Mapa por superfície**

- `GPT instructions`: comportamento resumido, tom, limites, fluxo mínimo.
- `knowledge files`: conhecimento estável e exemplos curados.
- `Projects`: agrupamento por público, caso de uso e knowledge pack.
- `chat`: contexto efêmero do caso atual.
- `AGENTS.md`: regras operacionais do Codex e contexto de execução.
- `SKILL.md`: uma habilidade específica, estreita e reutilizável.
- `references/`: conhecimento estável, durável, de consulta.
- `templates/`: moldes de criação e revisão.
- `examples/`: exemplos anotados e calibrados.
- `MCP`: ponte de execução e leitura/escrita em sistemas externos.
- `Notion/database`: memória operacional estruturada, métricas, backlog, registros.

---

## H. Próximos 10 passos práticos

1. Criar a pasta `docs/` com a árvore acima, sem ainda popular `03_chatgpt_web` e `04_codex`.
2. Preencher primeiro `00_visao-geral-do-sistema.md` em uma sessão única de definição.
3. Fechar `01_escopo-e-limites.md` com foco em recusas, handoffs e casos limítrofes.
4. Mapear `02_perfis-de-usuarios.md` para no máximo 4 perfis operacionais.
5. Construir `03_taxonomia-de-demandas.md` usando 30 a 50 pedidos reais já ocorridos.
6. Desenhar `00_fluxo-operacional-por-fases.md` e validar contra casos reais.
7. Aprovar `00_padrao-de-resposta.md` e `01_criterios-de-qualidade.md` antes de publicar qualquer canal.
8. Só então derivar `01_gpt-instructions-source.md` e `01_agents-md-source.md`.
9. Criar o catálogo inicial de skills apenas depois de fechar taxonomia e fases.
10. Desenhar `01_modelo-notion-operacional.md` apenas para registros que tenham uso claro em operação ou melhoria.

Se quiser, no próximo passo eu transformo isso em um pacote pronto para uso no repositório, criando os arquivos Markdown base em `docs/` já com esses templates preenchíveis.
