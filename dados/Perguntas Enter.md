# Perguntas para o Fernando — vaga Senior AI Deployment (Enter)

> Respostas alocadas a partir do áudio do Fernando. **As palavras são dele**, com limpeza apenas de marcador de fala ("tá ligado", "sabe", "enfim") e correção de erro de transcrição, sempre sinalizada entre colchetes.

**Status:** ✅ 11 respondidas · 🟡 13 parciais · ⬜ 10 não respondidas

| Bloco | ✅ | 🟡 | ⬜ |
|---|---|---|---|
| Vendas (1-13) | 2 | 6 | 5 |
| Produto (14-23) | 2 | 6 | 2 |
| Escopo (24-29) | 4 | 0 | 2 |
| Mercado (30-34) | 3 | 1 | 1 |

---

## Vendas

**1. Argumentos de venda (pitch deck)**
⬜ **Não respondida.**

---

**2. Quem são os stakeholders dessa venda (é sempre o time legal? CFO se envolve? Quando entra o time técnico? fazem POC? como fica LGPD no contrato?)**
🟡 **Parcial.**

> "Quem faz a venda é o time de Growth. É um time dedicado aqui que é basicamente responsável por isso e é um time bem institucional. É um time que se conecta com a diretoria e [chega n]a parte jurídica das outras empresas e introduz a coisa. Então é uma venda bem institucional e você precisa ter um lobby muito grande. Normalmente a galera desse time são pessoas bem relacionadas de mercado, que conseguem abrir porta e chegar [em] clientes, então normalmente eles que comandam as negociações."

**Falta:** se o CFO se envolve, quando entra o time técnico, se fazem POC, e como fica a LGPD no contrato.

---

**3. Qual o roadmap médio de integração?**
⬜ **Não respondida.**

---

**4. Enter utiliza apenas as integrações próprias dos LLMs ou integra na licença do cliente (se houver)?**
✅ **Respondida.**

> "A gente integra sim com uns [ERPs] do cliente pra puxar dados e colocar dados, porque o dado sempre nasce lá, tipo processo. Quem tem esse controle é o cliente, então a gente se conecta sim. Mas em relação a LLM, são todas dentro da infraestrutura da Enter, então a gente não tem nenhum modelo próprio, eu acho que não. O modelo próprio que eu falo é self-hosted, acho que a gente não tem. São APIs, tipo OpenAI e Claude. A gente tem algumas redundâncias em relação a [isso]."

---

**5. Para definição de ICP, quais são as principais métricas? Volume de processos? Valor gasto em processos por ano?**
✅ **Respondida.**

> "Eu não sei qual que é o mínimo, mas são apenas grandes clientes que têm um grande volume de processo. Então, sei lá, a partir de mil processos, por exemplo, por mês, aí que são clientes potenciais nossos. Então, de maneira geral, as grandes empresas."

---

**6. Quais as diferenças no pitch para mitigação de processo trabalhista e da esfera civil? Os stakeholders dentro das empresas mudam?**
🟡 **Parcial.**

> "Hoje a gente tá na parte civil. Foi o primeiro produto e agora a gente tá indo pra parte trabalhista também. Alguns clientes a gente tem só no trabalhista, outra [outros] a gente começou no civil, tá puxando trabalhista deles também."

**Falta:** a diferença de pitch entre as duas esferas e se os stakeholders dentro do cliente mudam.

---

**7. Quais os principais canais de aquisição de cliente hoje?**
🟡 **Parcial.**

> "Você precisa ter um lobby muito grande. Normalmente a galera desse time são pessoas bem relacionadas de mercado, que conseguem abrir porta e chegar [em] clientes."

**Falta:** se existe algum canal além de relacionamento e lobby (inbound, evento, indicação de cliente, parceria).

---

**8. Quais são os modelos de cobrança atualmente?**
⬜ **Não respondida.**

---

**9. Vendem solução modular? Qual produto é a porta de entrada? Tem lógica de cross-sell e upsell?**
🟡 **Parcial.**

> "Quando a Enter começou, [o] primeiro produto dela era só contestação, então é montar peças de contestação, que é a defesa. Agora a gente tem esse novo escopo de serviço que a gente chama de enterOS, que [é] a plataforma [em] que você acompanha todo caso."

> "O ponto importante é que a gente pega carteira dos clientes. [Pode] ter um cliente que tem [mil] processos por mês, não necessariamente a gente pega os [mil], então a gente pode pegar, por exemplo, 500 no primeiro momento e ir aumentando. Se chama share of wallet, que é percentual de carteira. Isso é uma métrica bem importante, que é a principal alavanca nossa. Chegar em 100% de share of wallet dos clientes. Então você pode começar com 20, 10 e ir aumentando. A gente tem alguns clientes que são 100% e são baita case da empresa. Mas a maioria não [é] 100% share of wallet, e essa é a principal alavanca de crescimento da empresa."

> "Alguns clientes a gente tem só no trabalhista, outra [outros] a gente começou no civil, tá puxando trabalhista deles também."

**Falta:** se a solução é vendida de forma modular e qual é hoje o produto de porta de entrada.

---

**10. Qual a maior objeção que os times jurídicos levantam, e como vocês contornam?**
🟡 **Parcial.**

> "Tem questão de aceitação. Tipo, a gente é uma empresa de tecnologia [que vai] prestar serviço jurídico, a gente precisa convencer a empresa que isso realmente faça sentido."

**Falta:** qual é a objeção concreta e como eles contornam.

---

**11. O time jurídico e o CFO que são os decisores da contratação?**
🟡 **Parcial.**

> "É um time que se conecta com a diretoria e [chega n]a parte jurídica das outras empresas e introduz a coisa. Então é uma venda bem institucional."

**Falta:** confirmação explícita sobre o CFO.

---

**12. Como o modelo SaaS centralizado sustenta com cliente enterprise sensível a dado jurídico? Isso pode ser um bloqueio comercial?**
⬜ **Não respondida.**

---

**13. O quanto conhecimento na área legal influencia no processo de venda?**
⬜ **Não respondida.**

---

## Produto

**14. Quais são as formas de integração / deployment?**
🟡 **Parcial.**

> "A gente integra sim com uns [ERPs] do cliente pra puxar dados e colocar dados, porque o dado sempre nasce lá."

> "Dado um processo, não é apenas montar a peça de defesa, mas fazer tudo [...] cadastro em vários tipos de plataforma que precisa ser feito, acompanhamento de prazo."

**Falta:** o mapa das formas de integração e deployment (API, arquivo, acesso direto, etc.).

---

**15. Quais são as variáveis de checagem de fraude?**
✅ **Respondida.**

> "O legal da Enter também é que a gente consegue ver muita coisa por conta própria. É essa questão de jurisprudência falsa. A gente consegue, nas nossas ferramentas, ver se o outro advogado não tá citando uma jurisprudência falsa. A gente consegue fazer alguns cruzamentos de dados, advogado ofensor. Às vezes é algum advogado de má fé, que ele tem vários processos para aquele mesmo cliente, protocolo duplicado. Quando o advogado pega e usa o mesmo número de protocolo de outros clientes para justificar uma ação daquele cliente. 'Eu abri dez protocolos com vocês e vocês não me responderam' — esses protocolos são de outros. Esse tipo de coisa a gente consegue ver, a gente tem ferramenta para isso."

---

**16. Eles integram nos demais sistemas internos da empresa? (Sistema de ponto, e-mail para acessar dispensas médicas / atestados, holerite) Como integram?**
🟡 **Parcial.**

> "A gente integra com o [ERP] do cliente. Normalmente a gente chama de subsídio. Dado que um caso existiu, a empresa tem que prover os subsídios daquele caso. Exemplo: banco. O banco está sendo processado [por] uma determinada fraude. Falaram que teve um empréstimo [no] nome de uma pessoa e a pessoa falou que não foi ela, foi uma fraude. O que o banco tem que fazer? Ele tem [que] analisar aquele caso, então ele tem um time interno que vai fazer uma investigação do tipo: 'tá falando que é fraude, mas vamos ver, essa pessoa assinou o contrato? Como é que foi a forma de contratação do empréstimo? Foi presencial? Teve biometria?'. Existe todo um fluxo onde todos os casos precisam passar, e quem faz isso é o próprio time interno do cliente, e passa para gente. É baseado nessas evidências que a gente monta as teses."

**Falta:** se integram em sistema de ponto, e-mail, holerite (os exemplos da pergunta) e como é feita a integração tecnicamente.

---

**17. Quais os bureaus que eles estão integrados pelo lado da Enter? (Ex: para mapear fraude eles consultam se o autor tem histórico de processos similares em algum lugar - Jusbrasil, etc)**
🟡 **Parcial.**

> "Tem uns casos legais da Latam, por exemplo. Quem toca Latam é o Fraga, inclusive. A gente conecta com uma API de tempo. Se não me engano, ela foi desenvolvida pela galera da Agulhas Negras, ITA, não sei, algum órgão assim, uma equipe federal. E você consegue ver: teve um cancelamento de voo e a Latam foi processada. Só que se for por motivo de [força] maior, ela não pode ser processada. Então se for um mau tempo, ela ganha o caso. A gente conseguiu conectar diretamente nessa API para puxar esse tipo de dado. Isso é uma inteligência a mais que a gente consegue [ter]. Mas é muito caso a caso. De maneira geral, a gente consegue sim dar inteligência nessa análise."

**Falta:** nenhum bureau nomeado (Jusbrasil ou equivalente). O exemplo dado é uma API de dados meteorológicos, não um bureau.

---

**18. Existe algum score de jurisprudência? A Enter faz uma análise preditiva de sucesso da defesa? (Fala de Jurimetria no site deles)**
🟡 **Parcial.**

> "A gente consegue, nas nossas ferramentas, ver se o outro advogado não tá citando uma jurisprudência falsa."

**Falta:** se existe score de jurisprudência e se há análise preditiva de sucesso da defesa. Ele falou de checagem de jurisprudência falsa, que não é a mesma coisa.

---

**19. Como é feito o acompanhamento se houve mitigação ou não do processo? (Qual a janela de prazo do tracking - se o autor não processar em x anos?)**
⬜ **Não respondida.**

---

**20. Como eles medem sucesso do saving financeiro da plataforma?**
🟡 **Parcial.**

> "O outro KPI que a gente acompanha é o ticket médio. Porque, beleza, ela não tem condição de ganhar o caso [em] que ela tá errada, mas a gente pode ir pra um acordo, e com esse acordo a gente consegue um valor melhor."

**Falta:** como o saving é calculado e comprovado em número (baseline, comparação contra o quê).

---

**21. Como eles comprovam track record, dado que a empresa é recente e o ciclo judicial em média é longo?**
⬜ **Não respondida.**

---

**22. Acordo bilateral entre empresa e autor é considerado sucesso? Quais os critérios?**
✅ **Respondida.**

> "Tem caso que a empresa tá errada e não tem o que fazer, realmente foi um caso que a empresa agiu errado, por conta de qualquer motivo, seja um processo errado que ela executou, seja [porque] o funcionário agiu de má fé. Isso daí pode acontecer. Então o outro KPI que a gente acompanha é o ticket médio, porque, beleza, ela não tem condição de ganhar o caso [em] que ela tá errada, mas a gente pode ir pra um acordo, e com esse acordo a gente consegue um valor melhor."

---

**23. Qual grau de personalização da ferramenta para atender diferentes necessidades de negócio?**
🟡 **Parcial.**

> "A coisa que a gente faz normalmente nessa parte de parametrização, ela é bem extensiva, porque tem muita coisa que a gente tem que fazer meio que na mão."

> "Na Claro, que é um cliente novo, precisa tudo ser implementado do zero, tanto a parte da contestação, que tem um tempo de execução grande de parametrizar ferramenta, quanto também a questão de estruturar a operação deles."

**Falta:** até onde vai a personalização e o que é fixo no produto.

---

## Escopo

**24. Como é dividido o tempo do AI deployment entre execução do projeto, contato com cliente e melhoria de produto interno?**
✅ **Respondida.**

> "O AI deployment tem tanto papel ali de execução quanto o papel de tocar o projeto. Quando a Enter começou, [o] primeiro produto dela era só contestação, então é montar peças de contestação, que é a defesa. Era 100% execução, porque você simplesmente parametrizava a solução, dava para o cliente e ele usava. Agora que a gente tem esse novo escopo de serviço que a gente chama de enterOS, [a] plataforma [em] que você acompanha todo caso, então virou muito mais um projeto. Dado um processo, não é apenas montar a peça de defesa, mas fazer tudo. [Tem a] questão de excelência operacional, de cadastro em vários tipos de plataforma que precisa ser feito, acompanhamento de prazo. Então tem uma parte forte do projeto."

> "Vai depender. Por exemplo, na Claro, que é um cliente novo, precisa tudo ser implementado do zero, tanto a parte da contestação, que tem um tempo de execução grande de parametrizar ferramenta, quanto também a questão de estruturar a operação deles. Então quase 50%. E no projeto da Claro, por exemplo, tá fazendo um outro menino, então ele tá mais focado na parte de parametrizar, eu tô mais focado na parte do projeto. Mas aí vai depender muito do tipo de cliente: se o projeto já aconteceu, se já tá andando, ou se é um projeto novo."

---

**25. O que você ainda faz manualmente para cada cliente que você gostaria que já fosse um playbook/workframe?**
✅ **Respondida.**

> "A coisa que a gente faz normalmente nessa parte de parametrização, ela é bem extensiva, porque tem muita coisa que a gente tem que fazer meio que na mão. Muito acompanhamento de dados também: a gente monta dash, a gente bate no banco pra tá fazendo esse tipo de acompanhamento. Então tem muita coisa que o produto tá evoluindo pra deixar as coisas mais produtizadas, com mais padrão. Enquanto o produto tá evoluindo, a gente precisa fazer muita coisa [por] fora ainda, mas a ideia é que fique tudo cada vez mais centralizado dentro do produto."

---

**26. Quanto tempo leva do kickoff até o cliente ver valor na Enter?**
⬜ **Não respondida.**

---

**27. Quais as métricas de sucesso para um processo end-to-end de implementação?**
✅ **Respondida.**

> "Métrica de sucesso é principalmente questão de êxito. Êxito é quantos casos você ganha. Então êxito e ticket médio. Porque tem caso que a empresa tá errada e não tem o que fazer. Então o outro KPI que a gente acompanha é o ticket médio, porque, beleza, ela não tem condição de ganhar o caso [em] que ela tá errada, mas a gente pode ir pra um acordo, e com esse acordo a gente consegue um valor melhor. Então êxito e ticket médio são os dois principais. De maneira geral, tem questão de prazo também, que acompanhar prazo jurídico envolve uma série de complexidades, então não perder prazo, por exemplo, é muito importante também. Mas de maneira geral são esses dois que são os mais importantes."

---

**28. Qual é a maior dor da área de AI Deployment hoje?**
✅ **Respondida.**

> "Eu acho que a maior dor da área de AI deployment hoje é que o produto ainda tem bastante... é um produto muito novo e ainda tem bastante espaço pra amadurecer. Então muita coisa precisa ser feita manual, o AI deployment ainda faz muita coisa manual por conta disso. Talvez essa seja a principal dor."

---

**29. Se um cliente não tem bandwidth para integração, qual é a solução que a Enter oferece?**
⬜ **Não respondida.**

---

## Mercado

**30. Quem são os principais concorrentes?**
✅ **Respondida.**

> "Principais concorrentes: a gente tá tomando mercado de clientes de escritórios que já fazem o que a gente faz. Então tem essa concorrência direta em termos de mercado, que a gente rouba literalmente fatia deles."

> "Tem algumas outras empresas que também são da área, tipo a [Harvey], que é bem grande nos Estados Unidos, é maior que a Enter até, só que ataca uma outra fatia de mercado. [A gente ataca] especificamente contencioso de massa de grandes empresas. Se pegar [Harvey], por exemplo, eles atacam um middle market, que é uma coisa que a gente não vai, pelo menos não agora, e não tem muita pretensão. Então é um ponto legal: Enter significa Enter de enterprise, então o foco é de fato oferecer soluções para essas grandes empresas. Nessa área jurídica não existe nenhum concorrente direto em termos de solução tecnológica que tá fazendo isso hoje."

---

**31. Um LLM mainstream de mercado como o Claude pode ameaçar o business da Enter de alguma forma? Quais principais diferenciais além do contexto?**
✅ **Respondida.**

> "Pensando em termos de empresas novas, de tecnologia: quando você pega grandes empresas como [Anthropic], como OpenAI, Google etc., eles não vão atacar um problema tão específico assim. São bem mais soluções generalistas, onde a pessoa, usando a ferramenta, tenta [endereçar] as nossas dores. A gente aqui vai muito mais deep nas coisas, pra entrar dentro da operação da pessoa, e precisa de uma expertise muito grande."

---

**32. Qual barreira de entrada pra esse mercado?**
✅ **Respondida.**

> "[A Enter] tem uma força muito grande do modelo tradicional, que hoje é o mercado forte. Então vai ter sempre algumas barreiras no sentido de: os outros escritórios também têm poder, são escritórios grandes que não querem perder mercado, então tem toda uma pressão política. Tem questão de aceitação: a gente é uma empresa de tecnologia [que vai] prestar serviço jurídico, a gente precisa convencer a empresa que isso realmente faça sentido. Então tem uma série de coisas aí que são desafios da empresa."

---

**33. Qual o esforço para uma empresa desenvolver isso internamente?**
🟡 **Parcial.**

> "Até mesmo consultoria não é tão trivial, porque você precisa de fato fazer um produto, não seria tipo um projeto."

**Falta:** o esforço para a própria empresa cliente desenvolver internamente. Ele respondeu do ângulo da consultoria, não do cliente.

---

**34. Como eles veem a questão de quem possui o dado afetar o futuro da empresa? Ex: com IA as empresas estão entrando em uma guerra de quem possui o dado/ informações, além de todos os inputs do modelo hoje serem dados extremamente sensíveis e estratégicos da empresa. Existe já um movimento de empresas construirem sua própria licença de AI ou comprarem de players que fazem o deployment no ambiente da empresa (ou até opensource). Isso é um risco ou oportunidade pra Enter?**
⬜ **Não respondida.**

---

## Observações

Coisas que o Fernando falou e que não respondem a nenhuma das 34 perguntas.

**Sobre o nível de profundidade que ele considera necessário**

> "Vou te mandar um áudio aqui por tópico. Eu vou passar um contexto mais geral. Muito sinceramente, eu [não] vou entrar em todas as perguntas. Então, se você quiser realmente saber um pouco mais a fundo, pode perguntar, claro. Mas, cara, eu diria que não é tão necessário você saber isso tudo a esse nível de profundidade. Algumas coisas nem eu sei tão de bate-pronto assim. É mais o contexto geral mesmo. Qualquer coisa que você quiser mais especificada, você [pode] me [perguntar] também."

**Fonte que ele recomendou**

> "Sobre mercado, o episódio do [Mateus] com o [?], um episódio que é gravado lá na Sequoia, ele entra relativamente bastante sobre isso. Inclusive ele faz comparação com qualquer outra empresa de LLM, tipo [Anthropic], OpenAI, [sobre] se eles não são concorrentes, e até mesmo consultorias, tipo o que impede a Accenture de fazer o que a gente faz. Acho que ele explica muito bem sobre essas questões."

**Nomes e clientes citados**

- **Claro** — cliente novo, implementação do zero, dividido entre ele (projeto) e outra pessoa (parametrização).
- **Latam** — cliente, tocado pelo **Fraga**.
- **enterOS** — nome do novo escopo de serviço / plataforma de acompanhamento de casos.
- **Share of wallet** — percentual da carteira de processos do cliente. Principal alavanca de crescimento da empresa.
- **Subsídio** — nome interno para as evidências que o cliente precisa prover sobre cada caso.

---

## Notas de transcrição

Correções feitas sobre erros evidentes do áudio, todas sinalizadas com colchetes no texto:

| Transcrição | Lido como |
|---|---|
| "RPs do cliente" | ERPs |
| "Mantropik" | Anthropic |
| "Harvard" | Harvey |
| "carteiro" | carteira |
| "principal aval" | principal alavanca |
| "causa maior" | força maior |
| "essência operacional" | excelência operacional |
| "Inter" / "Entra" | Enter |
| "que a gente chama de interesse" | enterOS |
| "Matheus" | Mateus |

**Pontos que continuam ilegíveis:** com quem é o episódio gravado na Sequoia ("o episódio do Mateus com o Lá"). O trecho "eu vou entrar em todas as perguntas" foi lido como "eu **não** vou entrar em todas as perguntas", pelo contexto da frase seguinte.
