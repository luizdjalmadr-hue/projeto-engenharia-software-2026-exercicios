# Lista 01 — Projeto de software: definição, fracasso e iniciação

**Unidade Curricular:** Projeto e Engenharia de Software — UNIFG 2026/2
**Unidade de Aprendizagem 1:** Gerenciamento de Projetos de Software
**Entrega:** até a véspera da aula 02 · pull request `[Aula 01] Seu Nome Completo`

Esta lista trabalha os conceitos da aula 01 e produz o rascunho de um artefato
que será reaproveitado no M1 do projeto integrador. A Parte E é individual mesmo
para quem já tem equipe formada.

Em várias questões não existe uma única resposta correta. O que é avaliado, com
peso de 30 pontos, é a justificativa.

---

## Parte A — Projeto e operação (15 pontos)

**A1 (8 pontos).** Classifique cada item como projeto ou operação, indicando qual
dos dois critérios da definição — temporariedade ou unicidade — foi decisivo na
sua classificação.

| | Item |
|---|---|
| a | Manter o site da prefeitura no ar |
| b | Migrar o site da prefeitura para uma nova plataforma |
| c | Atender os chamados de suporte da secretaria de educação |
| d | Implantar um sistema de chamados na secretaria |
| e | Emitir mensalmente a folha de pagamento dos servidores |
| f | Substituir o sistema que emite a folha de pagamento |
| g | Digitalizar as 3.200 fichas de endereço dos estudantes |
| h | Conferir trimestralmente a prestação de contas do transporte escolar |

**A2 (7 pontos).** Os itens **g** e **h** são interessantes porque a
classificação depende de informação que o enunciado não fornece.

Para cada um deles, descreva a informação que faltaria para decidir com
segurança, e mostre como a classificação mudaria em cada caso. Um dos dois
poderia ser projeto ou operação conforme a resposta; identifique qual.

---

## Parte B — As causas do fracasso (20 pontos)

**B1 (12 pontos).** Escolha **quatro** das oito causas recorrentes de fracasso
apresentadas na aula. Para cada uma, descreva uma contramedida concreta aplicável
ao projeto Rota Escolar.

Contramedida concreta significa uma prática, um artefato ou um mecanismo
específico — algo que possa ser verificado. "Melhorar a comunicação" não é
contramedida; "reunião semanal de 30 minutos com a servidora responsável pela
planilha, com ata registrada em issue" é.

Formato de cada resposta:

```markdown
### Causa: <nome da causa>

**Como ela se manifestaria no Rota Escolar:**
...

**Contramedida:**
...

**Como saber se a contramedida está funcionando:**
...
```

A terceira parte é a mais importante e a mais esquecida. Uma contramedida sem
forma de verificar se está funcionando é uma intenção.

**B2 (8 pontos).** A aula afirma que sete das oito causas recorrentes não são
técnicas.

Escreva um texto de 10 a 15 linhas respondendo: se isso é verdade, qual o sentido
de um curso de engenharia de software dedicar unidades inteiras a UML,
arquitetura e padrões de projeto?

A resposta precisa apresentar um argumento, e não apenas conciliar as duas
afirmações. Uma direção possível — que você não é obrigado a seguir — é
distinguir o que faz um projeto **falhar** do que faz um sistema **apodrecer**.

---

## Parte C — Requisitos mensuráveis (20 pontos)

**C1 (12 pontos).** Reescreva cada resultado esperado abaixo de forma
mensurável, isto é, de forma que permita verificar objetivamente, no fim do
projeto, se foi alcançado.

| | Formulação original |
|---|---|
| a | O sistema deve ser fácil de usar pelas servidoras da secretaria |
| b | Os relatórios devem ser gerados rapidamente |
| c | O sistema deve ser confiável |
| d | O sistema deve funcionar bem na zona rural |

Para cada um, indique também **de quem** viria a informação necessária para
definir o número. Essa segunda parte importa: números inventados por quem
desenvolve, sem consultar quem usa, produzem metas que ninguém precisava.

**C2 (8 pontos).** Escolha um dos quatro itens e explique o que aconteceria no
projeto se ele permanecesse na formulação original até o fim.

Descreva a situação concreta: quem afirmaria que o objetivo foi atingido, quem
discordaria, com base em quê, e como a discussão terminaria.

---

## Parte D — Atraso e estimativa (15 pontos)

**D1 (8 pontos).** No terceiro mês do projeto Rota Escolar, a equipe informa que
a etapa de levantamento de requisitos, estimada em seis semanas, levará dez.

Para cada uma das três explicações abaixo, classifique a situação como
"apareceu trabalho novo" ou "a estimativa estava errada", e indique a resposta
apropriada da gestão.

| | Explicação da equipe |
|---|---|
| a | "Descobrimos que os endereços dos estudantes estão em fichas de papel; ninguém sabia disso." |
| b | "As entrevistas estão rendendo menos do que esperávamos; achamos que uma reunião de duas horas resolveria cada escola, mas está levendo duas reuniões." |
| c | "A servidora que conhece as regras entrou em férias por 20 dias e não havia substituta." |

Note que o item **c** é ambíguo de propósito. Explique de que depende a
classificação nesse caso.

**D2 (7 pontos).** Um projeto contratado por R$ 180.000 com prazo de dez meses
está no sexto mês. A equipe informa que precisará de quatro meses adicionais. A
gestão autoriza a contratação de mais três pessoas para recuperar o atraso.

Explique por que essa decisão pode piorar a situação. A resposta deve incluir
pelo menos dois mecanismos concretos pelos quais o resultado pode ser pior que o
de não contratar ninguém.

A referência clássica é o capítulo 2 de *O Mítico Homem-Mês*, de Frederick
Brooks. Não é necessário lê-lo para responder, mas ajuda.

---

## Parte E — Termo de abertura (30 pontos)

Esta parte é individual, e o resultado será reaproveitado — revisado em equipe —
no M1 do projeto integrador.

**E1 (25 pontos).** Escreva um termo de abertura completo para **um** dos dois
projetos abaixo. Escolha o que preferir.

**Opção 1.** Sistema de gestão do acervo e dos empréstimos da biblioteca de um
campus universitário com 4.000 estudantes, 12.000 títulos e 3 servidoras. Hoje o
controle é feito em um sistema desktop de 2009 que roda em uma única máquina, sem
backup automatizado, e cujo fornecedor encerrou as atividades.

**Opção 2.** Aplicativo de registro de atendimentos para uma equipe de 14 agentes
comunitários de saúde de um município. Os agentes visitam cerca de 1.100
domicílios por mês, registram os dados em fichas de papel e entregam na unidade
de saúde, onde uma pessoa digita tudo no sistema do Ministério da Saúde.

O documento deve conter as nove seções do exemplo da aula 01: justificativa,
objetivo, resultados esperados mensuráveis, escopo preliminar com exclusões
explícitas, marcos previstos, restrições, premissas, riscos iniciais e
interessados.

O que será avaliado:

| Aspecto | Peso |
|---|---|
| Resultados esperados são de fato mensuráveis | 6 |
| As exclusões de escopo são explícitas e plausíveis | 5 |
| Premissas estão separadas de restrições, e são premissas de verdade | 5 |
| Riscos são previsíveis a partir do contexto, não genéricos | 5 |
| Os interessados incluem alguém que a maioria esqueceria | 4 |

O último item merece explicação. Todo levantamento de interessados encontra os
óbvios. A qualidade do artefato aparece nos que passam despercebidos: no caso da
biblioteca, quem responde pelo patrimônio da instituição; no caso dos agentes de
saúde, o Ministério da Saúde como destinatário final dos dados.

**E2 (5 pontos).** Faça a leitura crítica do **seu próprio** termo de abertura,
no formato da seção 7.1 da aula. Aponte:

- qual das suas premissas, se falsa, causaria o maior impacto, e por quê;
- qual seção você teve mais dificuldade de escrever, e o que isso indica sobre o
  que você ainda não sabe do domínio;
- uma pergunta que você faria ao patrocinador se tivesse acesso a ele.

---

## Parte F — Investigação (sem pontos, obrigatória)

A ausência desta parte reduz a nota da lista em 10 pontos. Ela não tem resposta
no material da aula.

Procure um caso brasileiro documentado de projeto de software público que
fracassou ou foi cancelado. Fontes possíveis: relatórios de tribunais de contas
estaduais ou do TCU, reportagens de veículos que cobrem tecnologia, acórdãos
disponíveis publicamente.

Escreva de 8 a 12 linhas informando:

- de que projeto se trata, e qual era o valor e o prazo previstos;
- qual foi o desfecho;
- quais das oito causas recorrentes da aula aparecem no caso;
- a fonte, com link.

Não é necessário que o caso seja grande. Um sistema municipal que custou
R$ 200.000 e nunca entrou em uso é um caso tão instrutivo quanto um de bilhões.

---

## Formato da entrega

```
exercicios/aula01/
├── RESPOSTAS.md              Partes A, B, C, D, E2 e F
└── termo-de-abertura.md      Parte E1
```

## Distribuição dos pontos

| Critério | Pontos |
|---|---|
| Corretude técnica | 35 |
| Justificativa das decisões | 30 |
| Qualidade dos artefatos | 25 |
| Clareza da comunicação escrita | 10 |
| Ausência da Parte F | −10 |

---

## Observações sobre algumas questões

**Parte A, itens g e h.** A dificuldade é intencional. Boa parte do trabalho de
classificar esforços em uma organização real tem essa característica: a resposta
depende de como o trabalho está organizado, e não de uma propriedade intrínseca
da atividade.

**Parte C.** Tornar um objetivo mensurável é mais difícil do que parece, e a
tentação é produzir números arbitrários. Um número arbitrário é pior que a
formulação vaga original, porque cria a aparência de rigor. Se você não sabe qual
número usar, diga de quem viria a informação — isso é uma resposta legítima.

**Parte E.** O termo de abertura será revisado em equipe no M1. Escrevê-lo
individualmente agora tem uma razão: a comparação entre as versões de cada pessoa
da equipe, na aula 05, revela onde o entendimento do problema divergia sem que
ninguém tivesse notado.
