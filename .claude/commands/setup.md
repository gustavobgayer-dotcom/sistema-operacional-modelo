---
name: setup
description: >
  Configura o GG Labs OS pra uma empresa ou departamento. Analisa o que o usuário
  descreve pra decidir o escopo (empresa inteira por setor, ou departamento único),
  captura o contexto do time (pessoas, cargos, KPIs, o que a empresa espera) e gera
  CLAUDE.md, memória, estrutura de pastas sob medida e lista de MCPs.
  Use quando o usuário chamar /setup, quando _contexto/empresa.md estiver vazio
  ou como template, ou quando disser "configurar o sistema", "primeira vez", "setup".
---

# /setup — Configuração do Sistema

## Verificação inicial

Antes de qualquer coisa, verifique se `_contexto/empresa.md` existe e tem conteúdo real (não apenas o template com placeholders entre colchetes).

- Se **está em branco/template**: inicia o fluxo de onboarding abaixo.
- Se **já tem conteúdo real**: informa ao usuário que o setup já foi feito e pergunta se quer refazer ou apenas atualizar alguma parte.

---

## Onboarding (primeira vez)

Comece com uma mensagem curta de boas-vindas:

> "Boa. Vou te fazer algumas perguntas pra configurar o OS pro seu time. Responde com calma — quanto mais específico, melhor o sistema vai trabalhar pra ti."

Faça as perguntas em sequência, uma por vez, em conversa natural. Não liste todas de uma vez. Espere a resposta de cada uma antes de ir pra próxima.

### Pergunta 1 — Escopo

"Esse OS vai ser da empresa inteira ou de um departamento específico?"

*(Ex: "empresa toda" = organiza por setor. "Sou do comercial e quero meu OS" = departamento único.)*

Guardar a resposta como **escopo**: `empresa` ou `departamento`. Se o usuário não deixar claro, seguir perguntando e inferir; confirmar antes de montar a estrutura.

### Pergunta 2 — Identificação

**Se for empresa:** "Qual é o nome da empresa e o que ela faz?"

**Se for departamento:** "Qual é o time/departamento, de qual empresa, e o que ele entrega?"

### Pergunta 3 — Verificação de histórico

"Você já usa o Claude Code há algum tempo, ou é a primeira vez?"

**Se já usa há algum tempo:** perguntar:

> "Quer que eu tente carregar o que você já tem configurado em outros projetos, ou prefere configurar do zero aqui?"

- **Se quiser carregar:** executar o bloco **"Carregamento de contexto existente"** abaixo antes de continuar.
- **Se preferir do zero:** continua normalmente pra Pergunta 4.

**Se for a primeira vez:** perguntar:

> "Você usa outro assistente de IA com frequência — ChatGPT, Claude na web, Gemini? Se sim, consigo pegar o contexto de lá pra não precisar responder tudo do zero."

- **Se não usa outro assistente:** continua normalmente pra Pergunta 4.
- **Se usa:** executar o bloco **"Importação de contexto de outro assistente"** abaixo antes de continuar.

---

#### Bloco: Carregamento de contexto existente (Claude Code anterior)

Tentar ler, nessa ordem:
1. `~/.claude/CLAUDE.md` — CLAUDE.md global (se existir)
2. Arquivos de memória em `~/.claude/projects/` — procurar por arquivos relevantes (empresa, preferências, contexto)

Com o que encontrar, montar um resumo e apresentar ao usuário:

> "Encontrei isso no que você já tem configurado:
>
> - **Empresa / time:** [extraído]
> - **O que faz:** [extraído]
> - **Tom de voz:** [extraído]
> - **Ferramentas:** [extraído]
> - *(... outras informações encontradas)*
>
> Está correto? Quer ajustar alguma coisa ou completar o que faltou?"

Aguardar confirmação ou correções do usuário. Após confirmar, **pular as perguntas já respondidas** e continuar apenas com o que ficou em aberto (pessoas, KPIs, identidade visual, etc.).

Se não encontrar nada relevante, informar:

> "Não encontrei contexto salvo de outros projetos. Vamos configurar do zero — leva poucos minutos."

E continuar normalmente pra Pergunta 4.

---

#### Bloco: Importação de contexto de outro assistente (ChatGPT, Claude web, Gemini, etc.)

Mostrar ao usuário o seguinte prompt pra copiar e colar no assistente que ele usa:

---

> **Copia esse prompt e cola no seu assistente de IA:**
>
> ```
> Preciso exportar o contexto do meu trabalho das nossas conversas para configurar uma nova ferramenta. Por favor, responda com o que sabe sobre mim nas seguintes categorias — se não souber algo, deixe em branco:
>
> EMPRESA OU DEPARTAMENTO: [nome da empresa e/ou do time]
> O QUE FAZ: [o que a empresa/time entrega, em 1-2 frases]
> PESSOAS E CARGOS: [quem está no time e a função de cada um]
> PRINCIPAIS INDICADORES / KPIs: [o que o time mede/acompanha]
> O QUE A EMPRESA ESPERA DO TIME: [a entrega/resultado principal cobrado]
> PRINCIPAIS ATIVIDADES: [o que você mais produz ou faz no dia a dia]
> FERRAMENTAS: [ferramentas que o time usa com frequência]
> IDENTIDADE VISUAL: [cores, fontes, estilo da marca — se mencionou alguma vez]
> TOM DE VOZ: [como você prefere escrever e se comunicar]
> O QUE EVITAR: [o que te incomoda em textos ou respostas de IA]
> OUTROS DETALHES: [qualquer outro contexto relevante]
> ```

---

Após mostrar o prompt, dizer:

> "Cola isso no [nome do assistente que o usuário mencionou] e traz a resposta aqui."

Aguardar o usuário colar a resposta. Com o que vier:

1. Extrair todas as informações da resposta
2. Montar um resumo e apresentar pro usuário confirmar
3. Aguardar confirmação ou ajustes
4. **Pular as perguntas já respondidas** e continuar apenas com o que ficou em branco

---

### Pergunta 4 — Pessoas e cargos

"Quem faz parte do time e qual o cargo de cada um?"

*(Se for uma pessoa só, tudo bem — anota como time de um. Se for empresa, pode ser os responsáveis por cada setor.)*

### Pergunta 5 — Indicadores / KPIs

"Quais são os principais indicadores que vocês acompanham? O que mede se o trabalho tá indo bem?"

*(Ex: comercial → receita, taxa de conversão, ticket médio; marketing → leads, CAC, alcance; RH → tempo de contratação, turnover; financeiro → margem, fluxo de caixa.)*

### Pergunta 6 — O que a empresa espera do time

"O que a empresa mais espera desse time? Qual é a entrega principal, o resultado que mais cobram de vocês?"

*(Essa resposta é a bússola do OS — orienta quais skills e pastas fazem mais sentido.)*

### Pergunta 7 — Atividades do dia a dia

"O que vocês mais produzem no dia a dia? Pode ser mais de uma coisa."

*(Exemplos: propostas comerciais, relatórios, apresentações, análises, follow-ups, documentos internos, materiais de campanha.)*

### Pergunta 7.5 — Foco atual

"E qual é o principal foco agora? O que vocês tão tentando fazer ou resolver nos próximos meses?"

*(Pode ser bater uma meta, estruturar um processo, reduzir um indicador ruim, organizar a operação — qualquer coisa que esteja na mesa.)*

### Pergunta 8 — Ferramentas

"Quais ferramentas vocês usam hoje no trabalho? Cita as principais."

*(Exemplos: Notion, Google Drive, Gmail, Google Calendar, Excel/Sheets, CRM, Slack, Trello, ClickUp, Meta Ads, Google Ads — qualquer uma que use com frequência.)*

### Pergunta 9 — Identidade visual

"A empresa tem identidade visual? Se sim, como prefere compartilhar?"

Apresentar as opções de forma natural, não como lista formal:

> "Pode me mandar o link do site, jogar alguns prints na pasta `dados/` e me dizer o nome dos arquivos, descrever em texto mesmo (cores, estilo, fontes), ou dizer que ainda não tem definido. Qualquer uma dessas funciona."

**Se compartilhar URL:**
- Buscar o conteúdo do site com WebFetch
- Analisar: cores dominantes, tipografia aparente, estilo geral (clean/bold/corporativo/etc), tom visual
- Apresentar o que foi detectado antes de preencher o design-guide:
  > "Vi no site: fundo [cor], destaque em [cor], tipografia [tipo], estilo [adjetivo]. Bate com a marca de vocês?"
- Ajustar conforme feedback e preencher `marca/design-guide.md`

**Se compartilhar imagens (logo, prints):**
- Pedir pro usuário colocar os arquivos na pasta `dados/` e informar os nomes
- Ler os arquivos como imagem, analisar cores, estilo, padrões
- Apresentar o que foi detectado antes de preencher, igual ao fluxo de URL

**Se descrever em texto:**
- Usar a descrição diretamente pra preencher `marca/design-guide.md`

**Se ainda não tiver definido:**
- Preencher o `marca/design-guide.md` com campos em branco e orientações pra preencher depois
- Mencionar brevemente: "Sem problema — você preenche quando tiver. O Claude vai usar um visual neutro até lá."

**Logo (perguntar em todos os casos acima):**

> "Tem o logo em PNG ou SVG? Se tiver, joga na pasta `marca/` e me diz o nome do arquivo. Se tiver versão pra fundo escuro e outra pra fundo claro, manda as duas."

- Se fornecer: preencher a seção **Logo** do `marca/design-guide.md` com o caminho e a variação
- Se não tiver: deixar a seção Logo em branco

### Pergunta 10 — Preferências de escrita

"Como vocês preferem que o Claude escreva? O que mais incomoda em textos gerados por IA?"

*(Exemplos: "direto, sem enrolação" / "mais institucional pra comunicação externa" / "odeio travessão e jargão corporativo".)*

---

## Processamento das respostas

Com todas as respostas, confirme o **escopo** e monte o perfil:

- **`empresa`** — organização com vários setores (marketing, comercial, financeiro, RH, operações). Estrutura por setor.
- **`departamento`** — um time só. Estrutura pelas pastas do fluxo daquele time.

O contexto capturado (pessoas, cargos, KPIs, o que a empresa espera, atividades) é a base pra decidir quais pastas e skills fazem sentido.

---

## O que gerar

### 1. Atualizar `CLAUDE.md` na raiz

Substitua os placeholders pelo conteúdo real:

```markdown
# [Nome da empresa ou do time] — Sistema Operacional

## O que é esse workspace
[uma ou duas frases descrevendo o que essa pasta representa — OS da empresa X organizado por setor, ou OS do time Y]

**Estrutura de pastas:**
[lista das pastas criadas conforme o escopo]
- `templates/skills/` — templates de skills prontos pra personalizar com /mapear
- `templates/ferramentas/catalogo.md` — APIs e ferramentas disponíveis pra usar em skills

## Sobre o negócio
[empresa/departamento, o que faz, pessoas e cargos, KPIs, o que a empresa espera do time]

## O que mais fazemos aqui
[lista das principais atividades/entregas]

## Tom de voz
[como escrever, o que evitar]

## Ferramentas conectadas
[lista das ferramentas — atualizar conforme MCPs forem instalados]

---

## Contexto do negócio
[manter as seções operacionais do template original: leitura de _contexto/ no início, fluxo de trabalho, regras do sistema, aprender com correções]
```

### 2. Preencher `_contexto/empresa.md`

```markdown
# Contexto da Empresa / Departamento

**Escopo:** [empresa inteira / departamento — nome]
**Nome:** [nome da empresa ou do time]
**O que faz:** [descrição]

## Pessoas e cargos
- [nome — cargo]

## Indicadores / KPIs
- [KPI principal]

## O que a empresa espera desse time
[a entrega/resultado principal]

## Setores ou processos
[setores, se empresa; processos, se departamento]

## Principais entregas
[o que mais produz]

## Ferramentas
[lista]

## Contexto adicional
[o que mais surgiu nas respostas]
```

### 3. Preencher `_contexto/estrategia.md`

Preencher fase, prioridade principal, o que pode esperar e contexto com prazo, a partir da Pergunta 7.5.

### 4. Preencher `_contexto/preferencias.md`

Preencher tom de voz, o que evitar e estilo geral, a partir da Pergunta 10.

### 5. Pré-preencher `marca/design-guide.md`

Se o usuário descreveu cores e estilo, preencha. Se não, deixe os campos em branco com o aviso do topo do arquivo.

### 6. Desenhar e criar a estrutura de pastas

**Não crave uma estrutura fixa.** Monte a partir do escopo + do que o time faz + dos KPIs, e **mostre a proposta antes de criar**.

Ler `templates/perfis/` pra ter os pontos de partida (`claude-md-empresa.md` e `claude-md-departamento.md`).

**Se escopo = empresa:** propor a estrutura por setor:

```
_contexto/  marca/
marketing/     comercial/ (propostas/)   financeiro/ (relatorios/)
rh/            operacoes/                 projetos/
dados/         tarefas.md
```

Ajustar os setores à realidade (adicionar/remover conforme o que existe na empresa).

**Se escopo = departamento:** propor pastas conforme o fluxo daquele time. Exemplos por área (usar como referência, não como regra):

- **Comercial:** `propostas/`, `clientes/` (ou `pipeline/`), `relatorios/`, `reunioes/`
- **Marketing:** `campanhas/`, `conteudo/`, `calendario/`, `relatorios/`
- **RH:** `vagas/`, `onboarding/`, `pessoas/`, `documentos/`
- **Financeiro:** `relatorios/`, `orcamentos/`, `fluxo-de-caixa/`
- **Operações:** `processos/` (SOPs), `fornecedores/`, `projetos/`

Todas terminam com `_contexto/`, `marca/`, `dados/` e `tarefas.md`.

Apresentar assim:

> "Com base no que você me contou, sugiro essa estrutura pro OS do [time/empresa]:
>
> ```
> [estrutura proposta]
> ```
>
> Quer usar essa, ajustar (adicionar/remover pasta), ou montar do seu jeito?"

- **Se aceitar:** criar as pastas.
- **Se quiser ajustar:** aplicar os ajustes e confirmar antes de criar.
- **Se quiser personalizar:** perguntar quais pastas fazem sentido e criar conforme ele descrever.

### 7. Recomendar MCPs e ferramentas

Ler `templates/ferramentas/catalogo.md` e cruzar com as ferramentas que o usuário citou na Pergunta 8.

Para cada ferramenta que o usuário usa e que tem um MCP ou conector disponível no catálogo:
- Mostrar o que o conector faz
- Mostrar o comando de instalação
- Perguntar se quer instalar agora

Exemplo:

> "Vi que vocês usam Notion. Tem um conector que deixa o Claude acessar suas páginas e bases direto. Quer que eu instale?"

Se aceitar, rodar o comando. Se preferir depois, anotar em `tarefas.md`:

```
## MCPs pra instalar depois
- [ ] Notion — `claude mcp add notion -- npx -y @notionhq/notion-mcp-server`
```

Se o usuário mencionar uma ferramenta que não está no catálogo, informar:

> "Não tenho um conector pronto pra [ferramenta], mas você pode pesquisar se existe um MCP pra ela em mcp.so. Se encontrar, me passa que eu instalo."

---

## Mensagem final

Após gerar todos os arquivos, envie uma mensagem de encerramento:

> "[Nome], o OS do [time/empresa] tá configurado.
>
> Aqui está o que foi criado:
> - CLAUDE.md — o Claude agora sabe quem é o time, o que a empresa espera de vocês e onde fica cada coisa
> - _contexto/ — negócio, pessoas, KPIs, preferências e foco atual salvos
> - marca/design-guide.md — identidade visual [preenchida / pronta pra preencher]
> - Estrutura de pastas [por setor / do time]
> - [N] MCPs instalados / [N] anotados pra instalar depois
>
> **Duas coisas importantes antes de continuar:**
>
> 1. Se você tiver chaves de API, guarde sempre num arquivo chamado `.env` — ele já está protegido e nunca vai ser enviado pro GitHub por engano.
>
> 2. Pra não perder o trabalho, conecte esse workspace ao GitHub rodando `/syncar`.
>
> **Próximo passo:** rode `/mapear` pra eu entender os processos do dia a dia do time e criar skills personalizadas."

---

## Regras

- Tom direto e humano, sem excesso de entusiasmo
- Não use listas com bullet points nas perguntas — faça em conversa
- Se o usuário der respostas vagas, faz uma pergunta de acompanhamento antes de continuar
- Gera os arquivos todos de uma vez no final, não um a um durante as perguntas
- Sempre mostrar a estrutura de pastas antes de criar
- Após gerar, mostra a mensagem final resumida — não lista cada linha de cada arquivo
