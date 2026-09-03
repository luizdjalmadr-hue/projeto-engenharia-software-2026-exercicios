# Projeto integrador: Rota Escolar

**Unidade Curricular:** Projeto e Engenharia de Software — UNIFG 2026/2
**Professor:** Petros Barreto
**Peso:** 65% da média final (55% nos marcos, 10% na apresentação)
**Formato:** equipes de 3 a 5 pessoas, formadas na aula 04

---

## O sistema a ser projetado

Um município de porte médio no interior da Bahia atende cerca de 3.200
estudantes com transporte escolar. A operação envolve 28 veículos, 31
motoristas, 24 monitoras, 19 escolas e 96 rotas — algumas com trechos de estrada
de terra que ficam intrafegáveis no período de chuva.

A gestão atual funciona assim: as rotas estão em uma planilha mantida por uma
servidora há seis anos; a lista de estudantes por veículo está em cadernos que
cada motorista guarda; a frequência é anotada em papel e entregue mensalmente;
a prestação de contas ao Tribunal de Contas é montada à mão a cada trimestre,
consumindo cerca de 80 horas de trabalho.

O município contratou o desenvolvimento de um sistema, o **Rota Escolar**, para
gerir essa operação.

### Por que este domínio

A escolha não é arbitrária. Quatro características tornam o caso adequado ao que
esta unidade curricular precisa ensinar.

**Os interessados têm objetivos incompatíveis.** A secretaria de educação quer
reduzir custo por estudante transportado. O responsável quer o ponto de embarque
mais próximo de casa. O motorista quer uma rota que caiba no tempo disponível.
O Tribunal de Contas quer rastreabilidade completa. Não existe solução que
satisfaça todos, o que obriga a priorizar e a registrar a priorização — que é o
assunto da unidade 3.

**As regras de negócio têm exceções reais.** A elegibilidade depende de distância,
mas medida pelo trajeto percorrível e não em linha reta; e há exceções para
estudantes com deficiência, independentemente da distância. Regras com exceção
forçam decisões de modelagem que regras simples não forçam — o que alimenta a
unidade 4.

**Há um requisito não funcional incontornável.** Vinte e três das 96 rotas não têm
sinal de celular em pelo menos um trecho. O sistema precisa registrar frequência
sem conexão e sincronizar depois. Isso restringe a arquitetura de forma que não
pode ser contornada por escolha de framework, e é o tipo de restrição que a
unidade 5 examina.

**A operação não pode parar.** O transporte roda todo dia letivo enquanto o
sistema é construído. Não existe a opção de desligar o processo antigo para
implantar o novo, o que traz para o projeto as questões de migração e convivência
que a unidade 6 trata.

---

## O que se entrega

O entregável do semestre é um **conjunto de artefatos de engenharia**
acompanhado de uma **fatia vertical implementada**.

Isso merece ser dito com clareza, porque contraria a expectativa comum: **não se
espera um sistema completo**. A ementa desta unidade curricular trata de
projetar, modelar, arquitetar e documentar. A implementação existe para verificar
se o projeto se sustenta quando encontra código — um diagrama de classes que
parece elegante e não se traduz em código funcional é um diagrama defeituoso, e a
única forma de descobrir isso é implementar uma parte.

A fatia vertical é um recorte funcional que atravessa todas as camadas. No Rota
Escolar, uma fatia adequada seria: registrar a frequência de uma turma em uma
rota, desde a interface até a persistência, funcionando sem conexão e
sincronizando quando a rede voltar. É pequena em escopo e completa em
profundidade.

---

## Os oito marcos

Cada marco é entregue como Pull Request no repositório da equipe, com o título
`[Rota Escolar MN] Nome da Equipe`.

### M1 — Iniciação e planejamento · aula 05 · 12%

| Artefato | Formato |
|---|---|
| Termo de abertura | 1 a 3 páginas, no formato apresentado na aula 01 |
| Declaração de escopo | inclusões, exclusões explícitas e critérios de aceitação do projeto |
| EAP | decomposição por entregas, até pacotes de trabalho de 8 a 80 horas |
| Cronograma | com dependências, marcos e caminho crítico identificado |
| Registro de riscos | mínimo de 10 riscos, com probabilidade, impacto e resposta planejada |
| Plano de comunicação | quem informa o quê, a quem, com que frequência e por qual meio |

O que distingue um M1 bem-feito é a **qualidade das premissas e exclusões**. Uma
declaração de escopo que só lista o que está incluído deixa em aberto tudo o
resto, e transfere para o meio do projeto uma discussão que deveria ter sido
resolvida no início.

### M2 — Definição do processo · aula 11 · 8%

A equipe escolhe o processo de desenvolvimento que vai adotar e justifica a
escolha. A justificativa precisa comparar com **duas alternativas descartadas**,
explicando por que foram descartadas neste contexto específico — e não em
abstrato.

Entregáveis: documento de definição do processo; quadro de trabalho configurado
no GitHub Projects; e, se a escolha for iterativa, o backlog inicial priorizado.

A comparação é a parte avaliada. "Escolhemos Scrum porque é ágil" não é
justificativa. "Escolhemos entregas incrementais de três semanas porque a
disponibilidade da servidora-chave é de 4 horas semanais e o ciclo precisa caber
nessa janela de validação" é.

### M3 — Requisitos · aula 17 · 18%

| Artefato | Conteúdo |
|---|---|
| Requisitos funcionais | mínimo de 25, identificados, com fonte e prioridade |
| Requisitos não funcionais | mínimo de 8, **todos mensuráveis** |
| Histórias de usuário ou casos de uso | para os 10 requisitos de maior prioridade, com critérios de aceitação |
| Registro de levantamento | como cada requisito foi obtido, de quem, quando |
| Matriz de rastreabilidade | requisito → origem → artefato de projeto → critério de aceitação |
| Registro de conflitos | onde interessados discordaram, e como foi decidido |

O requisito não funcional é o ponto em que a maioria das entregas falha. "O
sistema deve ser rápido" não é requisito. "A consulta de lotação de um veículo em
uma data deve responder em menos de 2 segundos, com 3.200 estudantes e 3 anos de
histórico na base" é.

O **registro de conflitos** é obrigatório porque conflito de requisito é normal e
sua ausência no documento indica que ele não foi percebido, e não que não existe.

### M4 — Modelagem e implementação do núcleo · aula 24 · 20%

| Artefato | Conteúdo |
|---|---|
| Diagrama de casos de uso | cobrindo os atores identificados no M3 |
| Diagrama de classes | com atributos, operações, multiplicidades e navegabilidade |
| Diagramas de sequência | 3 cenários, sendo um deles de exceção |
| Diagrama de atividades ou de estados | 1, para o fluxo ou entidade mais complexo |
| Código do núcleo | as classes de domínio implementadas, com testes |
| Justificativa de modelagem | onde e por que herança, composição ou interface foram usadas |

O código deve estar em PlantUML e em linguagem escolhida no M2 (Python 3.13 ou
Java 21). Os diagramas em PlantUML, versionados como texto — a razão está no
`README.md` da disciplina.

A justificativa de modelagem vale tanto quanto os diagramas. Um `Motorista` que
herda de `Pessoa` e um `Motorista` que compõe uma `Pessoa` produzem sistemas
diferentes, com consequências diferentes de manutenção. Qual foi escolhido
importa menos do que a equipe saber dizer por quê.

### M5 — Arquitetura · aula 30 · 18%

| Artefato | Conteúdo |
|---|---|
| Documento de arquitetura | modelo C4: contexto, contêineres, componentes |
| Registros de decisão (ADR) | mínimo de 6, no formato apresentado na aula 30 |
| Análise de atributos de qualidade | como a arquitetura atende cada RNF do M3, e a que custo |
| Fatia vertical | funcionando, com o requisito de operação sem conexão atendido |

Os ADRs são o artefato mais valioso deste marco. Um registro de decisão de
arquitetura documenta o **contexto** em que a decisão foi tomada, as
**alternativas** consideradas, a decisão e suas **consequências** — incluindo as
negativas. Uma decisão sem consequência negativa declarada não foi analisada.

### M6 — Manutenção e evolução · aula 34 · 8%

| Artefato | Conteúdo |
|---|---|
| Plano de manutenção | como os quatro tipos de manutenção serão atendidos |
| Análise de dívida técnica | do **próprio código** da equipe, com evidência |
| Estratégia de evolução | como o sistema conviverá com a planilha atual durante a transição |

A análise de dívida técnica é sobre o código que a própria equipe escreveu. Isso
é deliberado: reconhecer compromisso assumido no próprio trabalho é mais difícil
e mais útil que apontar problema em código de terceiros.

### M7 — Gerência de configuração · aula 37 · 8%

Este marco avalia o **histórico** do repositório, e não um documento novo. O que
se examina:

| Item | O que se espera |
|---|---|
| Estratégia de ramificação | documentada e efetivamente seguida no histórico |
| Pull requests | com revisão de outra pessoa da equipe, e comentários substantivos |
| Mensagens de commit | descrevendo o porquê, não apenas o quê |
| Versionamento | semântico, com tags e um `CHANGELOG.md` |
| Distribuição do trabalho | contribuição de todas as pessoas da equipe, visível no histórico |
| Rastreabilidade | commits associados a issues, issues associadas a requisitos |

Um repositório com 40 commits de uma pessoa e 3 de cada uma das outras quatro
indica um problema de trabalho em equipe, que é uma das competências avaliadas na
unidade curricular. O histórico do Git é o registro mais honesto disso que existe.

### M8 — Documentação e apresentação · aula 40 · 8% + 10%

| Artefato | Conteúdo |
|---|---|
| Documentação consolidada | os artefatos dos marcos anteriores, revisados e coerentes entre si |
| README do projeto | como instalar, executar e testar, a partir de máquina limpa |
| Apresentação | 20 minutos |

A coerência entre artefatos é avaliada. Um diagrama de classes que menciona uma
entidade ausente do documento de requisitos indica que os documentos evoluíram
separadamente — que é o problema de documentação mais comum na prática, e o
assunto da aula 38.

Estrutura sugerida da apresentação: 3 minutos sobre o problema e os interessados;
5 sobre as decisões de requisito e as que foram deixadas de fora; 5 sobre a
arquitetura e os compromissos assumidos; 4 de demonstração da fatia vertical,
incluindo o funcionamento sem conexão; 3 de perguntas.

---

## A atividade cruzada da aula 38

Na aula 38, cada equipe recebe a documentação produzida por outra equipe e tenta
colocar o sistema em funcionamento usando apenas o que está escrito, sem fazer
perguntas.

Duas notas saem dessa atividade. A equipe que **documentou** é avaliada pelo
sucesso da outra. A equipe que **executou** é avaliada pela qualidade do relato:
o que faltava, o que estava ambíguo, o que estava errado, e o que teria bastado
para resolver.

A atividade existe porque "documente bem" é uma recomendação sem consequência até
que alguém dependa da documentação. Aqui alguém depende.

---

## Papéis rotativos

Cada marco tem uma pessoa responsável pela coordenação, e **essa pessoa não pode
coordenar dois marcos consecutivos**. Com oito marcos e equipes de 3 a 5 pessoas,
todas coordenam ao menos uma vez.

A coordenação envolve: organizar as reuniões da equipe, consolidar a entrega,
abrir o pull request e responder pela comunicação com o professor naquele marco.
Não envolve fazer o trabalho das outras pessoas.

O registro de quem coordenou cada marco vai no `README.md` do projeto e é
verificado contra o histórico do Git.

---

## Níveis de escopo

A equipe escolhe o nível no M2 e o declara no `README.md`.

| Nível | Escopo adicional | Nota máxima |
|---|---|---|
| **1 — Essencial** | os oito marcos com o conteúdo mínimo descrito acima | 8,5 |
| **2 — Completo** | fatia vertical com sincronização real de dados offline; testes automatizados nas classes de domínio; diagramas de implantação | 10,0 |
| **3 — Avançado** | cálculo de elegibilidade por trajeto usando dados reais do OpenStreetMap; análise de desempenho da consulta de lotação com base de 3 anos; documentação publicada como site | 10,0 + bônus |

Bônus adicionais, até 1,5 ponto no total:

- Entrevista com uma pessoa que trabalhe de fato com transporte escolar, registrada e usada no M3
- Protótipo navegável validado com alguém externo à turma
- Análise comparativa da mesma modelagem em Python e em Java, com as diferenças de expressividade discutidas
- Automação da geração dos diagramas a partir do código, ou do código a partir dos diagramas

---

## Critérios de avaliação

Aplicados a todos os marcos:

| Critério | Pontos |
|---|---|
| Corretude técnica dos artefatos | 35 |
| Justificativa das decisões de projeto | 30 |
| Qualidade e coerência dos artefatos entre si | 25 |
| Clareza da comunicação escrita | 10 |

A justificativa pesa 30 pontos porque engenharia de software consiste, em grande
parte, em escolher entre alternativas aceitáveis sob restrição. Em quase nenhum
dos artefatos deste projeto existe uma única resposta correta. Existe resposta
adequada ao contexto e defensável, e resposta que não se sustenta quando alguém
pergunta por quê.

### O que reduz a nota de forma significativa

Artefato copiado de exemplo sem adaptação ao contexto do projeto. Documento
gerado sem que a equipe consiga explicar suas decisões. Requisito não funcional
sem número. Decisão de arquitetura sem consequência negativa declarada. Histórico
de Git que mostra trabalho concentrado em uma pessoa.

### Sobre uso de assistentes de IA

É permitido, e deve ser declarado no `README.md` do projeto, indicando em quais
artefatos e de que forma. O critério é o mesmo aplicado a qualquer outra fonte:
a equipe precisa entender e conseguir defender cada decisão registrada. Em uma
disciplina em que 30% da nota está na justificativa, texto que a equipe não
consegue sustentar em uma pergunta perde valor de qualquer maneira.

---

## Estrutura do repositório

```
rota-escolar/
├── README.md                    visão geral, nível escolhido, coordenação por marco
├── docs/
│   ├── 01-termo-abertura.md
│   ├── 02-escopo.md · 03-eap.md · 04-cronograma.md
│   ├── 05-riscos.md · 06-comunicacao.md
│   ├── 07-processo.md
│   ├── 08-requisitos.md · 09-rastreabilidade.md · 10-conflitos.md
│   ├── 11-arquitetura.md
│   ├── 12-manutencao.md
│   ├── adr/
│   │   └── 0001-persistencia-local.md ...
│   └── diagramas/
│       ├── casos-de-uso.puml
│       ├── classes.puml
│       ├── sequencia-*.puml
│       └── c4-*.puml
├── src/
├── tests/
└── CHANGELOG.md
```

---

## Cronograma dos marcos

| Marco | Aula | Unidade de aprendizagem correspondente |
|---|---|---|
| M1 | 05 | UA 1 — Gerenciamento de Projetos |
| M2 | 11 | UA 2 — Modelos e Metodologias |
| M3 | 17 | UA 3 — Requisitos |
| M4 | 24 | UA 4 — Modelagem e Orientação a Objetos |
| M5 | 30 | UA 5 — Projeto e Arquitetura |
| M6 | 34 | UA 6 — Ciclo de Vida e Manutenção |
| M7 | 37 | UA 7 — Gerência de Configuração |
| M8 | 40 | UA 8 — Documentação e Colaboração |

Cada marco é entregue na aula que encerra a unidade correspondente, de modo que o
conteúdo é aplicado imediatamente depois de estudado.

---

Dúvidas sobre o projeto podem ser registradas como *issue* no repositório de
exercícios.
