# Lista 02 — Escopo, EAP e controle de mudanças

**Unidade Curricular:** Projeto e Engenharia de Software — UNIFG 2026/2
**Unidade de Aprendizagem 1:** Gerenciamento de Projetos de Software
**Entrega:** até a véspera da aula 03 · pull request `[Aula 02] Seu Nome Completo`

Esta lista continua o caso escolhido na Parte E da lista 01 — biblioteca do campus
ou aplicativo dos agentes comunitários de saúde. Use o mesmo caso, para que os
artefatos se acumulem.

O termo de abertura da lista 01 é insumo desta lista. Se ele mudou depois da
correção, use a versão corrigida.

---

## Parte A — Escopo do produto e escopo do projeto (15 pontos)

**A1 (10 pontos).** Classifique cada item como escopo do **produto**, escopo do
**projeto**, ou item que deveria ser **exclusão**. Justifique em uma linha cada.

| | Item (caso da biblioteca) |
|---|---|
| a | Tela de registro de empréstimo |
| b | Migração dos 12.000 títulos do sistema antigo |
| c | Compra de leitores de código de barras |
| d | Treinamento das 3 servidoras |
| e | Relatório de obras em atraso |
| f | Manutenção do sistema no ano seguinte à entrega |
| g | Etiquetagem física dos 12.000 exemplares |
| h | Cálculo de multa por atraso |
| i | Contratação de uma quarta servidora |
| j | Backup automatizado da base |

Se o seu caso é o dos agentes de saúde, traduza cada item para o domínio
equivalente antes de classificar, e informe a tradução usada.

**A2 (5 pontos).** Dois itens da lista dependem de uma decisão que ainda não foi
tomada. Identifique quais, diga qual é a decisão pendente em cada caso e de quem
é a decisão.

---

## Parte B — Declaração de escopo (25 pontos)

**B1 (20 pontos).** Escreva a declaração de escopo completa do seu caso, no
formato da seção 2.1 da aula, com as quatro partes:

| Parte | Mínimo exigido |
|---|---|
| Inclusões | 8 itens identificados (I1, I2, …) |
| Exclusões | 5 itens, **cada um com observação** explicando a razão |
| Entregas | 6 entregas identificadas (D1, D2, …) |
| Critérios de aceitação | 4 critérios, **cada um com a coluna "como se verifica"** |

Distribuição dos pontos:

| Aspecto | Pontos |
|---|---|
| Inclusões cobrem o escopo do produto **e** do projeto | 5 |
| Exclusões são plausíveis e têm observação útil | 6 |
| Ao menos uma exclusão decorre de premissa da lista 01 que se revelou frágil | 3 |
| Critérios de aceitação são verificáveis, com método declarado | 6 |

O terceiro item merece atenção. Na aula 02, a premissa "os endereços estão
digitalizados" virou a exclusão E6, com a responsabilidade atribuída à
secretaria. Faça o mesmo movimento com uma das premissas do seu termo de abertura.

**B2 (5 pontos).** Escolha **uma** das suas exclusões e escreva o diálogo de
quatro a seis linhas que aconteceria no terceiro mês do projeto se ela **não**
estivesse registrada. Depois escreva o mesmo diálogo com ela registrada.

O objetivo é demonstrar a diferença entre disputa e decisão, e não produzir
literatura.

---

## Parte C — EAP e dicionário (30 pontos)

**C1 (16 pontos).** Construa a EAP completa do seu caso, decomposta **por
entregas**, com três níveis.

Requisitos:

- mínimo de 7 entregas no segundo nível;
- a gerência do projeto deve estar presente;
- ao menos duas entregas que **não** são software;
- todo pacote de trabalho com estimativa em horas, entre 8 e 80;
- a regra dos 100% respeitada em todos os nós.

Entregue em dois formatos. O `eap.md` com a estrutura e as estimativas em tabela,
e o `eap.puml` com o diagrama.

```
@startwbs
* 1. Biblioteca do Campus
** 1.1 Gerência do projeto
*** 1.1.1 Plano de projeto [24h]
** 1.2 Requisitos
*** 1.2.1 Entrevistas com as servidoras [16h]
@endwbs
```

O `.puml` será compilado pela verificação automática do pull request.

**C2 (10 pontos).** Escreva o dicionário de **quatro** pacotes de trabalho, com
os oito campos do exemplo da seção 4.1 da aula: descrição, entrega, responsável,
estimativa, predecessor, critério de conclusão, premissas e **exclui**.

Escolha os quatro pacotes assim: o de maior estimativa, o de menor, um que não é
software, e um que você considera o mais arriscado. Informe o critério de escolha
de cada um.

**C3 (4 pontos).** Verifique sua própria EAP contra os dois testes da seção 4 da
aula, e relate o resultado:

- para cada pacote, é possível nomear **uma** pessoa responsável?
- para cada pacote, é possível verificar, olhando algo concreto, se terminou?

Se algum pacote falhar em um dos testes, corrija a EAP e explique o que mudou.

---

## Parte D — Escopo crescente (15 pontos)

O histórico abaixo é de um projeto real de sistema de biblioteca, com prazo
original de seis meses.

| Semana | Pedido | Aprovado? | Esforço |
|---|---|---|---|
| 3 | Campo de observação no cadastro de exemplar | sim, na hora | 3 h |
| 5 | Exportar a lista de empréstimos em Excel | sim, na hora | 10 h |
| 7 | Filtro por área do conhecimento na busca | sim, na hora | 14 h |
| 9 | Etiqueta de lombada com o logo da instituição | sim, na hora | 8 h |
| 11 | Histórico de empréstimos anteriores do usuário | sim, na hora | 22 h |
| 13 | Aviso por e-mail três dias antes do vencimento | sim, na hora | 26 h |
| 16 | Relatório de obras mais emprestadas por semestre | sim, na hora | 12 h |

Na semana 18, a coordenação questionou o atraso do projeto.

**D1 (6 pontos).** Calcule o total de horas de trabalho não previsto e converta
em semanas de uma pessoa, considerando 30 horas úteis semanais de trabalho
efetivo em desenvolvimento. Apresente o cálculo.

**D2 (5 pontos).** Nenhum dos sete pedidos era absurdo, e nenhum isoladamente
justificaria renegociar o prazo. Explique, em 8 a 12 linhas, por que a soma
produziu um problema que nenhuma parcela produzia.

**D3 (4 pontos).** Escreva o registro de mudanças que a equipe deveria ter
mantido — uma tabela com as sete linhas — e descreva como a conversa da semana 18
teria sido diferente com esse documento na mesa.

---

## Parte E — Solicitação de mudança (15 pontos)

**E1 (12 pontos).** Preencha uma solicitação de mudança completa, no formato da
seção 8.1 da aula, para o pedido abaixo, adaptado ao seu caso.

**Caso da biblioteca:** a coordenação de pós-graduação pede que o sistema
controle também o empréstimo entre bibliotecas de outras instituições, com prazo
e regras próprias.

**Caso dos agentes de saúde:** a secretaria pede que o aplicativo também registre
a aferição de pressão arterial e glicemia durante a visita, com histórico por
domicílio.

O formulário precisa conter: data, solicitante, descrição, justificativa, item de
escopo afetado, e a análise de impacto com as seis dimensões — esforço, prazo,
custo, outros itens, riscos introduzidos e requisitos afetados.

Termine com a recomendação da equipe.

**E2 (3 pontos).** Indique **quem** deve decidir essa solicitação, justificando
com a tabela de autoridade da seção 8 da aula. Se a sua análise indicar que a
decisão exige reavaliar o termo de abertura, explique por quê.

---

## Parte F — Investigação (sem pontos, obrigatória)

A ausência desta parte reduz a nota da lista em 10 pontos.

Procure uma **EAP real** de um projeto público brasileiro. Editais de licitação de
sistemas, termos de referência e planos de trabalho de contratos de TI
frequentemente contêm uma, sob o nome de "estrutura analítica", "plano de
trabalho" ou "cronograma físico-financeiro". Portais de transparência municipais
e estaduais são boas fontes.

Escreva de 8 a 12 linhas informando:

- de que projeto se trata e onde o documento foi encontrado, com link;
- a decomposição é por entregas ou por fases?
- há itens que não são software — treinamento, migração, documentação?
- a gerência do projeto aparece?
- qual o maior problema que você identifica nessa EAP?

Se não encontrar nenhuma, relate o que procurou e onde. A dificuldade de
encontrar já é um achado.

---

## Formato da entrega

```
exercicios/aula02/
├── RESPOSTAS.md              Partes A, B2, C3, D, E e F
├── declaracao-escopo.md      Parte B1
├── eap.md                    Parte C1 (estrutura e estimativas) e C2 (dicionário)
└── eap.puml                  Parte C1 (diagrama)
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

**Parte A.** Os itens **c**, **g** e **i** são os interessantes. Comprar
equipamento, etiquetar 12.000 exemplares e contratar pessoal não são software —
mas isso não decide automaticamente se estão dentro ou fora. Depende do que foi
contratado, e é aí que a exclusão explícita entra.

**Parte C1.** A tentação é montar a EAP com sete nós chamados Levantamento,
Análise, Projeto, Implementação, Testes, Documentação e Implantação. Isso é um
ciclo de vida, não uma EAP por entregas, e perde os pontos de corretude. O teste
é simples: se o nó não pode ser aceito nem rejeitado, ele é uma atividade.

**Parte C2.** O campo **exclui** é o que mais custa a preencher e o que mais vale.
Ele existe para evitar a lacuna entre dois pacotes vizinhos, em que cada lado
supõe que o outro faz a parte do meio.

**Parte D2.** A resposta esperada não é "porque somaram muitas horas". Isso é o
cálculo de D1. A pergunta é por que a **estrutura** de aprovar pequenas mudanças
na hora produz um resultado que nenhuma das decisões individuais produziria — o
que envolve a ausência de registro e a impossibilidade de perceber a tendência.

**Parte E.** A dimensão mais esquecida da análise de impacto é "riscos
introduzidos". No caso dos agentes de saúde, registrar pressão arterial e glicemia
significa passar a tratar dado de saúde, o que muda o enquadramento na LGPD. Uma
análise que não percebe isso está incompleta.
