# GG Labs: Sistema Operacional

Sistema operacional do departamento/empresa pra rodar no Claude Code: centraliza todas as informações importantes da GG Labs de forma personalizada em um local só, projetos de clientes, produção de conteúdo, propostas, reuniões e relatórios.

---

## Como instalar

### Opção 1 — Via prompt (mais fácil)

Com o Claude Code aberto em qualquer pasta, copie e cole esse prompt:

```
Instala pra mim o repositório https://github.com/gustavobgayer-dotcom/sistema-operacional-modelo.git na pasta atual, abre ela e roda /setup
```

O Claude faz tudo: clona o repositório, entra na pasta e inicia a configuração.

---

### Opção 2 — Via terminal

**1. Clone o repositório**
```bash
git clone https://github.com/gustavobgayer-dotcom/sistema-operacional-modelo.git
cd sistema-operacional-modelo
```

**2. Abra no VS Code**
```bash
code .
```

**3. Abra o terminal integrado** (Ctrl + ` no Windows / Cmd + ` no Mac) e rode:
```bash
claude
```

**4. Chame o setup**
```
/setup
```

---

O `/setup` analisa o que você descreve, decide se o OS é da empresa inteira (por setor) ou de um departamento específico, e monta a estrutura de pastas sob medida. Em poucos minutos você tem tudo pronto.

---

## O que vem no kit

**Skills prontas pra usar:**
- `/setup` — configura o OS: detecta se é empresa ou departamento e monta as pastas (comece por aqui)
- `/iniciar` — carrega o contexto no começo de cada sessão de trabalho
- `/mapear` — mapeia seus processos e cria skills personalizadas pro seu time
- `/novo-projeto` — cria pasta de projeto novo com CLAUDE.md dedicado (entrevista sobre o projeto)
- `/proposta-comercial` — gera proposta profissional em HTML a partir de um briefing
- `/slide` — cria slide/card visual pra apresentação ou deck
- `/analisar-dados` — analisa um arquivo e gera resumo executivo com insights
- `/email-profissional` — rascunha email profissional a partir de contexto livre
- `/atualizar` — varre o projeto e atualiza os arquivos de contexto que ficaram desatualizados
- `/syncar` — salva o trabalho no GitHub (commit + push, configura na primeira vez)

**Pastas geradas pelo `/setup`:**
- `_contexto/` — contexto da empresa/departamento, preferências e foco atual
- `marca/` — guia de identidade visual
- Pastas de trabalho conforme o escopo: por setor (empresa) ou por fluxo do time (departamento)

**Pasta `dados/`:**
- Drop zone pra arquivos que você quer analisar (CSV, XLSX, TXT, PDF)
- Útil quando você não tem MCP de Google Drive instalado
- Use com `/analisar-dados dados/seu-arquivo.csv`
