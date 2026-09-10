# Resumo — Experiência do Usuário (IHC) — Prova

*Baseado nos slides e atividades da disciplina (Prof. Ana Paula Canal). Bibliografia principal: Rocha & Baranauskas (2003), Mandel (1997), Grilo (2019).*

---

## 1. UX vs UI

- **UI (User Interface / Interface do Usuário)**: a parte visual e interativa do produto — botões, cores, layout, tipografia. É o "como parece e como se usa".
- **UX (User Experience / Experiência do Usuário)**: a experiência **completa** do usuário ao interagir com o produto — inclui UI, mas também emoções, eficiência, satisfação, utilidade e acessibilidade. É "como a pessoa se sente usando".
- **Donald Norman** cunhou o termo "User Experience" para ir além da usabilidade e cobrir todos os aspectos da interação da pessoa com a empresa/produto/serviço.
- Regra prática: **UI é um subconjunto de UX**. Um produto pode ter UI bonita e UX ruim (ex.: app bonito mas confuso).

### Exemplos de inovação digital (citados em atividade)
CNH Digital, e-Título, apps bancários — reduzem burocracia e aumentam a autonomia do usuário, mas exigem boa IHC para não excluir usuários menos familiarizados com tecnologia.

### Importância do IHC
Uma interface mal projetada gera erros, frustração, abandono do produto e até riscos (ex.: sistemas críticos). Boa IHC = eficiência + satisfação + menor carga cognitiva.

---

## 2. Evolução Histórica das Interfaces

Tabela evolutiva (hardware / usuários / tipo de interface), por período:

| Período | Hardware | Usuários | Interface |
|---|---|---|---|
| Até 1945 | Mecânico/eletromecânico | Poucos especialistas | Nenhuma interface (operação direta) |
| 1945–1955 | Válvulas | Engenheiros | Painéis, plugues, chaves |
| 1955–1965 | Transistores | Especialistas/programadores | Cartões perfurados, linguagem de máquina |
| 1965–1980 | Circuitos integrados | Programadores profissionais | Terminais de texto, linhas de comando |
| 1980–1995 | Microprocessadores | Público mais amplo | Interfaces gráficas (GUI), WIMP (Windows, Icons, Menus, Pointer) |
| 1995– | Redes/Internet | Público em geral | Web, multimídia, depois mobile/touch |

- Tendência: quanto mais o hardware evolui, mais **usuários leigos** passam a usar computadores, exigindo interfaces cada vez mais amigáveis.
- Tópicos atuais citados (Atividade 1): **wearables, realidade virtual (VR), realidade aumentada (AR), metaverso, computação móvel** — continuação dessa evolução rumo a interfaces mais naturais/imersivas.

---

## 3. Áreas envolvidas em IHC

IHC é uma área **multidisciplinar**, envolvendo (entre outras):
- Ciência da Computação (implementação)
- Psicologia (cognição, percepção, comportamento)
- Design (visual, gráfico, de interação)
- Ergonomia
- Sociologia/Antropologia (contexto de uso)
- Linguística/Semiótica (comunicação por signos)

---

## 4. Usabilidade

**Usabilidade = Qualidade da Interação.** Segundo Mandel (1997) e conteúdo da disciplina, os três pilares centrais:

1. **Facilidade de aprendizado** — quão rápido um novo usuário consegue aprender a usar o sistema.
2. **Flexibilidade de interação** — quantidade de formas diferentes que usuário e sistema podem trocar informação (múltiplos caminhos para a mesma tarefa).
3. **Robustez de interação** — nível de suporte ao usuário para atingir seus objetivos, incluindo recuperação de erros.

---

## 5. Metáforas de Interface

- **Metáfora**: usar um conceito familiar do mundo real para representar uma função abstrata do sistema (ex.: "área de trabalho", "lixeira", "pastas").
- Facilita o **modelo mental** do usuário, reduzindo a curva de aprendizado.
- Exemplos do Duolingo (Atividade 2 do próprio aluno): coração = vidas restantes; troféu = conquistas; "foguinho" (streak) = sequência de dias estudando. Todas usam ícones do mundo real para representar conceitos do sistema.
- Reflexão pedida (Atividade 1): pensar em um app difícil de usar e quais metáforas ajudariam a torná-lo mais intuitivo.

### Modelos Mentais (três modelos)
- **Modelo do Usuário**: como o usuário imagina que o sistema funciona (construído pela experiência de uso).
- **Modelo do Programador** (ou do sistema): como o sistema **de fato** funciona internamente.
- **Modelo do Projetista/Designer**: a intenção do designer sobre como o usuário deveria entender o sistema.
- Meta do design: aproximar ao máximo o **modelo do usuário** do **modelo do projetista**, escondendo a complexidade do modelo do programador.

---

## 6. MPIH — Modelo do Processador Humano de Informação

**Fonte:** Card, Moran & Newell (1983), via Rocha & Baranauskas (2003, cap. 3). Modela o ser humano como um sistema de processamento de informação com três subsistemas interligados, cada um com **memórias** e **processadores** próprios, caracterizados por 4 tipos de parâmetros:

- **u** = capacidade de armazenamento da memória (unidades: itens, letras, chunks)
- **d** = tempo de decaimento (quanto tempo a informação permanece antes de se perder)
- **k** = tipo de código de armazenamento (físico, acústico, visual, semântico...)
- **t** = tempo de ciclo do processador (tempo para processar uma unidade de informação)

Ciclo geral: **Sistema Perceptual → Sistema Cognitivo → Sistema Motor** ("reconhece–age").

### 6.1 Sistema Perceptual (SP)

- **Processador Perceptual (PP)**: converte estímulos físicos (luz, som) em representações mentais.
  - `tp = 100ms [50–200ms]` — tempo de ciclo do processador perceptual.
- **MIV (Memória de Imagem Visual)**: retém estímulos visuais brevemente.
  - `dmiv = 200ms [90–1000ms]`
  - `umiv = 17 letras [7–17]`
- **MIA (Memória de Imagem Auditiva)**: retém estímulos auditivos brevemente.
  - `dmia = 1500ms [900–3500ms]`
  - `umia = 5 letras [4,4–6,2]`
- **Perceptum**: unidade básica de percepção; a percepção não é uma cópia fiel da realidade, mas uma interpretação.
- **Lei de Bloch**: relação entre intensidade e duração de um estímulo luminoso para que seja percebido — quanto mais breve o estímulo, maior deve ser sua intensidade para ser percebido (I × t = constante, para durações curtas).
- **Fóvea**: região central da retina com maior acuidade visual; os olhos se movem por **sacadas** (movimentos rápidos) para focar diferentes pontos.
- **Pattern/template matching**: reconhecimento de padrões visuais comparando com "moldes" armazenados na memória.
- **Ilusões de ótica** (exemplos vistos): figuras ambíguas (ex.: taça/dois rostos), efeito de imagem residual (afterimage), paralaxe de movimento, grade de Hermann — mostram que a percepção pode ser "enganada", evidenciando que o sistema perceptual interpreta ativamente, não apenas registra.

### 6.2 Sistema Cognitivo (SC)

- **Processador Cognitivo (PC)**: processa/decide com base nas informações das memórias.
  - `tc = 70ms [25–170ms]`
- **MCD/MT (Memória de Curta Duração / Memória de Trabalho)**:
  - `dmcd = 7s [5–226s]`
  - `umcd = 3 chunks [2,5–4,1]` isolados, podendo chegar a **7 chunks [5–9]** quando auxiliada pela MLD (relação com a MLD aumenta a capacidade efetiva).
- **MLD (Memória de Longa Duração)**:
  - `dmld = infinito` (não decai)
  - Capacidade também considerada ilimitada.
- **Chunk**: unidade significativa de informação agrupada (ex.: a sigla "IHC" é 1 chunk de 3 letras, mas só se o usuário já souber o que significa; para quem não sabe, são 3 chunks separados). Exemplo citado: "WIMP" como chunk para quem conhece IHC.
- Reconhecimento é **paralelo**, mas a ação/resposta é **serial** (só se executa uma ação de cada vez, mesmo que várias informações sejam reconhecidas ao mesmo tempo).

### 6.3 Sistema Motor (SM)

- **Processador Motor (PM)**: converte decisões cognitivas em ações físicas (comandos musculares).
  - `tm = 70ms [30–100ms]`
- Dados empíricos citados (Card et al., 1983, p.63):
  - Digitação: **novato ≈ 1000ms/tecla**; **especialista ≈ 60ms/tecla**.
  - Tempo médio calculado: ~**140ms por tecla** (exemplo de cálculo apresentado).
  - Diferença de desempenho entre teclado **QWERTY** e teclado **alfabético**: cerca de **8%** (o QWERTY não é necessariamente pior apesar do arranjo "não lógico").

### 6.4 Aplicação prática do MPIH (exemplo do Duolingo — Atividade 2)

Fluxo ao responder uma pergunta no app:
1. **SP**: o usuário lê e ouve o enunciado/áudio da pergunta (percepção visual + auditiva).
2. **SC**: reconhece a palavra/estrutura gramatical (usa MCD e MLD — vocabulário já aprendido), decide a resposta.
3. **SM**: executa a ação física — toca na opção correta ou digita a resposta.
Esse ciclo se repete a cada interação, e a **carga cognitiva** aumenta se o conteúdo é difícil ou a interface é confusa (mais chunks para processar na MCD).

---

## 7. Semiótica e Comunicação em Interfaces

**Fonte:** Charles Sanders Peirce; Grilo (2019).

- **Semiótica**: estudo dos signos e de como eles produzem significado.
- **Tríade de Peirce**: todo signo envolve três elementos:
  1. **Signo** (ou Representamen) — aquilo que representa algo (ex.: o ícone).
  2. **Objeto** — aquilo que é representado (o referente real).
  3. **Interpretante** — o efeito/sentido que o signo produz na mente de quem interpreta.
- **Sentido x Significado**: sentido é a interpretação subjetiva/contextual; significado é mais fixo/convencional (dicionário).
- **Três dimensões do signo** (segundo Grilo, 2019):
  1. **Sintática** — relação entre os signos entre si (estrutura, forma).
  2. **Semântica** — relação entre o signo e o que ele representa (significado).
  3. **Pragmática** — relação entre o signo e o usuário/contexto de uso (efeito prático, uso real).

### Arquétipos de Marca (Mark & Pearson, 2003 — citado por Grilo, 2019, p.109)
Aplicação de arquétipos de personalidade (ex.: o Herói, o Sábio, o Explorador, o Inocente, o Fora-da-lei, o Mago, o Cara Comum, o Amante, o Bobo da Corte, o Cuidador, o Criador, o Governante) para dar **identidade e coerência semiótica** a produtos digitais — a marca "comunica" um arquétipo através de cores, tom de voz, ícones etc.

---

## 8. Psicologia da UX — Percepção e Cognição

**Fonte:** Grilo (2019) — árvore de conceitos psicológicos aplicados à UX.

### Percepção
Como o usuário capta e interpreta estímulos da interface (cores, contraste, hierarquia visual, som) — base para a leitura e compreensão dos elementos de tela.

### Cognição
Desdobra-se em quatro grandes áreas:

1. **Atenção**
   - **Sustentada** — manter o foco em uma tarefa por um período prolongado.
   - **Seletiva** — focar em um estímulo relevante ignorando distrações.
   - **Dividida** — atenção repartida entre múltiplas tarefas/estímulos simultâneos (multitasking).

2. **Memória**
   - **Sensorial** — retenção breve dos estímulos captados pelos sentidos (equivale à MIV/MIA do MPIH).
   - **Curta duração** — retém informação por segundos, capacidade limitada (equivale à MCD do MPIH).
   - **Longa duração** — dividida em:
     - **Declarativa** (consciente, "saber que"): subdividida em **episódica** (eventos vividos) e **semântica** (fatos e conceitos gerais).
     - **Não-declarativa** (implícita, "saber como"): habilidades, hábitos, procedimentos automáticos.

3. **Linguagem**
   - Base teórica: **Vygotsky** — a linguagem é fundamental para o pensamento e para a mediação social/cultural da cognição. Em UX, a linguagem/microcopy da interface (textos, rótulos, mensagens de erro) afeta diretamente a compreensão do usuário.

4. **Modelo Mental**
   - Representação interna que o usuário constrói sobre como o sistema funciona, construída a partir de experiências prévias e da interação com a interface (liga-se diretamente ao conceito de Modelo do Usuário visto na seção de Metáforas).

### Exemplos de interface de e-commerce (aplicação prática)
- **Etapas de progresso no checkout** (ex.: carrinho → endereço → pagamento → confirmação) — reduzem carga cognitiva mostrando onde o usuário está no processo (usa memória de trabalho de forma eficiente, menos chunks a reter).
- **Rastreamento de pedidos** (linha do tempo de status) — comunica informação complexa de forma visual e sequencial, facilitando o modelo mental do usuário sobre "onde está meu pedido".

---

## 9. Ergonomia do Software

Citada no contexto do trabalho PA1 Parte 2: aplica princípios ergonômicos (adequação da interface às capacidades e limitações humanas) na análise de um produto digital, normalmente em conjunto com os conceitos do MPIH — ou seja, avalia-se se a interface respeita os limites de percepção, memória e tempos de resposta do usuário.

---

## 10. Dark Patterns

Citado na Atividade 1 (pesquisa pedida, conteúdo pode cair na prova como conceito):
- **Dark Patterns** são padrões de design **intencionalmente enganosos**, criados para induzir o usuário a tomar ações que não tomaria conscientemente (ex.: dificultar cancelamento de assinatura, pré-selecionar opções pagas, criar falso senso de urgência/escassez, esconder custos até o fim do checkout).
- Vão contra os princípios de usabilidade e ética em UX — o oposto de um design centrado no usuário.
- Vale ter 1–2 exemplos concretos na cabeça (ex.: botão de "cancelar assinatura" escondido; contagem regressiva falsa de "oferta"; opt-out pré-marcado para newsletter/dados).

---

## 11. Respostas ao PA1 — Parte 2 (Produto de Aprendizagem 1)

**Produto Digital escolhido: Duolingo** (mesmo exemplo usado na Atividade 2, para manter consistência com o que já foi estudado em aula).

### Pergunta 1 — Houve estudo de UX/IHC no desenvolvimento do produto? Em que aspectos?

Sim, é possível perceber claramente um estudo aprofundado de Experiência do Usuário e IHC no desenvolvimento do Duolingo. Isso fica evidente em aspectos como:

- **Onboarding guiado**: o app não joga o usuário direto no conteúdo — há um fluxo inicial de perguntas (nível, objetivo, tempo diário) que ajusta a experiência ao perfil do usuário, reduzindo a carga cognitiva inicial.
- **Uso de metáforas e gamificação**: elementos como o coração (vidas), o troféu (conquistas) e o "foguinho" (streak/sequência de dias) traduzem conceitos abstratos do sistema em símbolos familiares e emocionalmente engajadores — exatamente o papel das metáforas de interface discutido em aula.
- **Feedback imediato**: cada resposta (certa ou errada) gera retorno visual e sonoro instantâneo, o que respeita os tempos de ciclo do MPIH e evita que o usuário fique "no escuro" quanto ao resultado de sua ação.
- **Consistência visual**: cores, ícones e posicionamento dos botões se mantêm padronizados em todas as telas, o que reduz o esforço de aprendizado a cada nova tela (facilidade de aprendizado — um dos pilares da usabilidade).

### Pergunta 2 — Análise via MPIH

**a) Sinalização de eventos importantes / como é chamada a atenção do usuário**

O Duolingo utiliza principalmente **estímulos visuais e sonoros combinados** para sinalizar eventos importantes, explorando o Sistema Perceptual (MIV e MIA): cores fortes (verde para acerto, vermelho para erro), sons característicos (efeito sonoro de acerto/erro), pequenas animações (o mascote reagindo) e notificações push (lembrete diário, "sua sequência está em risco"). Esses estímulos são projetados para serem captados rapidamente pelo Processador Perceptual (tp ≈ 100ms) e chamam a **atenção seletiva** do usuário para a informação mais relevante no momento (ex.: destacar em vermelho a palavra errada), evitando que ele precise varrer a tela inteira em busca do que mudou.

**b) Carga cognitiva / quantidade de elementos nas telas / processamento da informação**

As telas do Duolingo são **enxutas**, normalmente com apenas um exercício, uma instrução curta e poucos botões de ação por vez. Essa escolha de design está diretamente alinhada aos limites do MPIH: a Memória de Curta Duração (MCD) comporta apenas cerca de **3 a 7 chunks** simultaneamente, então telas poluídas gerariam sobrecarga cognitiva. Ao apresentar uma única tarefa por tela, o app garante que o **Sistema Cognitivo (SC)** processe a informação sem ultrapassar essa capacidade. Não há, portanto, sobrecarga na maior parte da experiência — a única exceção é quando o exercício envolve uma frase longa ou uma explicação gramatical nova, momento em que a quantidade de "chunks" a reter aumenta (o usuário ainda não tem esses itens consolidados na Memória de Longa Duração/MLD, então cada palavra nova conta como um chunk isolado, em vez de agrupada). O processamento segue o ciclo clássico do MPIH: **percepção do enunciado (SP) → reconhecimento/decisão usando MCD e MLD (SC) → resposta física (SM)**.

**c) Subsistema Motor — habilidades necessárias**

A interação com o Duolingo exige habilidades motoras relativamente simples, típicas de interfaces touch: **toques (taps)** em opções de múltipla escolha, **arrastar e soltar (drag-and-drop)** para ordenar palavras, e **digitação** em exercícios de escrita livre. Como são ações curtas e repetitivas, o tempo do Processador Motor (tm ≈ 70ms, dentro da faixa de 30–100ms) é suficiente para a maioria das interações, e usuários mais experientes com o app desenvolvem uma "automatização" motora parecida com a diferença entre digitador novato (~1000ms/tecla) e especialista (~60ms/tecla) vista no Sistema Motor — quanto mais uso, mais rápida e precisa fica a resposta física do usuário aos exercícios.

### Pergunta 3 — Ergonomia do Software

**Pesquisa breve**: a Ergonomia do Software é a aplicação de princípios ergonômicos ao desenvolvimento de interfaces, buscando adequá-las às capacidades cognitivas, perceptivas e físicas do ser humano. Um dos referenciais mais usados na área são os **critérios ergonômicos de Bastien & Scapin (1993)**, que incluem: condução, carga de trabalho, controle explícito, adaptabilidade, gestão de erros, consistência, significado dos códigos e compatibilidade.

Dois critérios aplicados ao Duolingo:

- **Condução (guidance)** — *em conformidade*. Este critério avalia se o sistema orienta, informa e conduz o usuário adequadamente. O Duolingo cumpre bem esse critério: setas e destaques indicam a próxima lição disponível na trilha, instruções curtas aparecem no topo de cada exercício, e o app sempre deixa claro qual é a ação esperada (ex.: "toque na tradução correta"). Isso reduz a ambiguidade e guia o usuário passo a passo, mesmo sem tutorial extenso.

- **Gestão de erros (error management)** — *parcialmente em conformidade*. Este critério avalia como o sistema previne, sinaliza e ajuda o usuário a se recuperar de erros. O Duolingo sinaliza bem os erros (feedback visual/sonoro imediato) e oferece a explicação da resposta correta logo depois, o que ajuda na recuperação e no aprendizado. Porém, ele **não é totalmente robusto** nesse critério: em alguns exercícios de digitação, pequenos erros de digitação (typos) são tratados como erro de conteúdo, gerando frustração — uma prevenção de erro mais tolerante (ex.: ignorar diferenças mínimas de digitação) tornaria o sistema mais robusto e mais alinhado a esse critério ergonômico.
