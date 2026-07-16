# GG Labs: Sistema Operacional

## O que é esse workspace
Sistema operacional de trabalho feito pra centralizar num só lugar tudo que importa de uma empresa ou de um departamento: processos, entregas, documentos, propostas, relatórios e acompanhamento.

Esse OS funciona em dois recortes, definidos no `/setup`:
- **Empresa inteira** — organizado por setor (marketing, comercial, financeiro, RH, operações).
- **Departamento único** — a pasta é o OS de um time só, com as pastas e o fluxo daquele departamento.

O `/setup` analisa o que você descreve, decide entre empresa ou departamento e monta a estrutura de pastas sob medida. Antes de configurar, a estrutura abaixo é só uma referência.

**Estrutura de pastas (referência, o `/setup` ajusta):**
- `_contexto/` — memória do sistema (não apagar)
- `marca/` — identidade visual e logos
- `dados/` — drop zone pra arquivos analisar (CSV, XLSX, TXT, PDF)
- `templates/skills/` — templates de skills prontos pra personalizar com /mapear
- `templates/ferramentas/catalogo.md` — APIs e ferramentas disponíveis pra usar em skills
- `tarefas.md` — lista de tarefas corrente
- *(pastas de trabalho criadas pelo `/setup`: por setor, se for empresa; por fluxo do time, se for departamento)*

## Sobre o negócio
*(Preenchido pelo `/setup` em `_contexto/empresa.md`: qual é a empresa ou o departamento, o que faz, quem são as pessoas e cargos, principais indicadores/KPIs e o que a empresa mais espera desse time.)*

## O que mais fazemos aqui
*(Preenchido pelo `/setup` com as principais entregas do time ou da empresa.)*

## Escopo e contexto
Esse OS pode servir uma empresa inteira ou um departamento específico. O contexto detalhado (setores, processos, pessoas, KPIs) fica em `_contexto/empresa.md`.

## Tom de voz
*(Definido em `_contexto/preferencias.md`. Por padrão: informal e direto, como quem fala. Evitar travessão (—), frases-fragmento curtas em série, e dicotomias do tipo "não é isso, é aquilo".)*

## Ferramentas conectadas
- [ ] Notion
- [ ] Gmail
- [ ] Google Calendar
- [ ] Google Drive

*(Marcar conforme for instalando os MCPs)*

---

## Contexto do negócio

No início de toda conversa, ler os seguintes arquivos (se existirem e estiverem configurados):

1. `_contexto/empresa.md` — qual é a empresa ou o departamento, o que faz, pessoas, KPIs, o que a empresa espera do time
2. `_contexto/preferencias.md` — tom de voz, estilo de escrita, o que evitar
3. `_contexto/estrategia.md` — foco atual, prioridades, o que pode esperar

Usar essas informações como base pra qualquer resposta ou decisão. Ao sugerir prioridades, formatos ou abordagens, considerar o foco atual descrito em `estrategia.md` e os indicadores do time descritos em `empresa.md`.

Para qualquer tarefa visual (proposta, slide, apresentação), consultar `marca/design-guide.md` como referência de estilo.

Não é necessário listar o que foi lido nem confirmar a leitura. Apenas usar o contexto naturalmente.

---

## Fluxo de trabalho

Antes de executar qualquer tarefa, verificar se existe uma skill relevante em `.claude/skills/` ou `.claude/commands/`.
Se encontrar, seguir as instruções da skill.
Se não encontrar, executar a tarefa normalmente.

Ao concluir uma tarefa que não tinha skill mas parece repetível, perguntar se o usuário quer transformar em skill. Não perguntar pra tarefas pontuais.

---

## Regras do sistema

- A estrutura de pastas de trabalho é a que o `/setup` montou pro escopo (empresa por setor ou departamento por fluxo).
- Salvar cada entregável na pasta correspondente ao fluxo/setor a que pertence.
- Propostas comerciais vão na pasta de propostas do comercial (ex.: `comercial/propostas/` ou `propostas/`).
- Relatórios e análises vão na pasta de relatórios do time (ex.: `financeiro/relatorios/` ou `relatorios/`).
- Manter o `tarefas.md` como lista corrente de tarefas do OS.

---

## Aprender com correções

Quando o usuário corrigir algo ou der uma instrução que parece permanente ("na verdade é assim", "não faça mais isso", "prefiro assim", "sempre que...", "evita..."), perguntar se quer salvar. Se sim:

- **Sobre a empresa/departamento** → `_contexto/empresa.md`
- **Preferências e estilo** → `_contexto/preferencias.md`
- **Prioridades e foco atual** → `_contexto/estrategia.md`
- **Regra de comportamento nessa pasta** → este `CLAUDE.md`
- **Mudança visual** → `marca/design-guide.md`

Salvar só a linha nova, sem reformatar o arquivo inteiro.
