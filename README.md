# Exercícios — Projeto e Engenharia de Software

**UNIFG 2026/2** · Prof. Petros Barreto · 160 horas em 40 aulas de 4h
**Nível do segmento:** Fundamental · **Área:** Computação e TIC

Este é o repositório público da unidade curricular. Contém as listas de
exercícios, a especificação do projeto integrador **Rota Escolar** e os modelos
de artefato usados ao longo do semestre.

Os slides ficam em repositório separado, cujo endereço é distribuído em sala e no
ambiente virtual.

---

## Preparação do ambiente

Feita uma vez, no início do semestre.

```bash
# 1. Faça fork deste repositório

# 2. Clone o seu fork
git clone https://github.com/SEU-USUARIO/projeto-engenharia-software-2026-exercicios.git
cd projeto-engenharia-software-2026-exercicios

# 3. Aponte para o repositório original, para receber as listas novas
git remote add upstream https://github.com/petrosbarreto/projeto-engenharia-software-2026-exercicios.git
```

Para gerar as imagens dos diagramas localmente, é necessário PlantUML. Existem
três formas de usá-lo:

```bash
# opção A — extensão do VS Code (mais simples)
#   instale "PlantUML" e use Alt+D para pré-visualizar

# opção B — Java local
brew install plantuml          # macOS
sudo apt install plantuml      # Debian/Ubuntu
plantuml docs/diagramas/classes.puml

# opção C — servidor público, sem instalar nada
#   http://www.plantuml.com/plantuml/uml/
```

Para as listas com código, a partir da UA 4:

```bash
# se a equipe escolher Python
uv init && uv python pin 3.13 && uv add --dev pytest

# se escolher Java
# JDK 21 + Maven ou Gradle
```

### Antes de cada lista nova

```bash
git switch main && git pull upstream main && git push origin main
```

---

## Entrega de uma lista

```bash
git switch -c aula07
# resolva em exercicios/aula07/
git add exercicios/aula07
git commit -m "Aula 07: comparação entre modelo espiral e incremental"
git push -u origin aula07
```

Em seguida, abra um pull request com o título no formato
`[Aula NN] Seu Nome Completo`.

Pull request com título fora do padrão não é corrigido. Para as entregas do
projeto, o formato é `[Rota Escolar MN] Nome da Equipe`.

### Verificação automática

Ao abrir o pull request, uma automação verifica quatro coisas e comenta o
resultado:

| Verificação | Comportamento |
|---|---|
| Presença de `RESPOSTAS.md` na pasta alterada | falha se ausente |
| Sintaxe dos arquivos `.puml` alterados | falha se algum diagrama não compila |
| Título do pull request no padrão | aviso |
| Testes, quando houver código | falha se algum teste quebrar |

A verificação de sintaxe dos diagramas existe por uma razão prática: um `.puml`
que não compila indica diagrama que nunca foi visualizado, e diagrama nunca
visualizado costuma estar errado.

---

## Formato de cada entrega

```
exercicios/aulaNN/
├── RESPOSTAS.md          respostas, análises e justificativas
├── diagramas/            arquivos .puml, quando a lista pedir
├── src/                  código, a partir da UA 4
└── evidencias/           capturas e saídas de comando, quando pertinente
```

Três regras se aplicam a todas as listas.

**As seções do `RESPOSTAS.md` seguem a numeração do enunciado.** Se o enunciado
tem `## Parte A` e `### A1`, a resposta tem as mesmas divisões. Isso existe para
tornar a correção verificável e não é preferência estética.

**Diagramas são entregues em PlantUML, como texto.** A imagem exportada pode ser
incluída, mas o `.puml` é obrigatório. A razão é que texto entra no controle de
versão e aparece no *diff*; um `.png` não permite ver o que mudou entre duas
versões.

**Toda decisão de projeto vem acompanhada da justificativa.** Um diagrama de
classes que usa herança sem explicar por que não usou composição está incompleto
como artefato de engenharia, mesmo estando sintaticamente correto.

---

## Critérios de correção

| Critério | Pontos | O que se avalia |
|---|---|---|
| Corretude técnica | 35 | as respostas e os artefatos estão tecnicamente certos |
| Justificativa das decisões | 30 | as escolhas foram explicadas e se sustentam |
| Qualidade dos artefatos | 25 | completos, legíveis, coerentes entre si |
| Clareza da comunicação escrita | 10 | organização e redação |

A justificativa pesa 30 pontos porque, em quase nenhum problema desta unidade
curricular, existe uma única resposta correta. Existe resposta adequada ao
contexto e defensável, e resposta que não se sustenta quando alguém pergunta por
quê. Uma resposta diferente da esperada, bem fundamentada, vale mais do que a
resposta esperada sem fundamento.

### Prazos

| | |
|---|---|
| Entrega | até a véspera da aula seguinte, 23h59 |
| Atraso de até 7 dias | desconto de 20 pontos |
| Atraso acima de 7 dias | não corrigido; conta como uma das descartadas |

A nota de exercícios é a média das 40 listas, descartando as duas piores.

---

## Composição da nota final

| Instrumento | Peso |
|---|---|
| Marcos do projeto Rota Escolar (M1 a M8) | 55% |
| Listas de exercícios (40) | 25% |
| Participação em revisões e atividades entre equipes | 10% |
| Apresentação final | 10% |

---

## Projeto integrador: Rota Escolar

Equipes de 3 a 5 pessoas, formadas na aula 04, conduzem o projeto de um sistema
de gestão de transporte escolar municipal, do termo de abertura à documentação
final.

O entregável é um conjunto de artefatos de engenharia acompanhado de uma fatia
vertical implementada — e não um sistema completo. A ementa desta unidade
curricular trata de projetar, modelar, arquitetar e documentar; a implementação
serve para verificar se o projeto se sustenta quando encontra código.

| Marco | Aula | Entrega | Peso |
|---|---|---|---|
| M1 | 05 | Termo de abertura, escopo, EAP, cronograma, riscos, comunicação | 12% |
| M2 | 11 | Processo de desenvolvimento escolhido, com justificativa | 8% |
| M3 | 17 | Documento de requisitos com rastreabilidade | 18% |
| M4 | 24 | Modelos UML e núcleo orientado a objetos implementado | 20% |
| M5 | 30 | Documento de arquitetura (C4), ADRs e fatia vertical | 18% |
| M6 | 34 | Plano de manutenção e análise de dívida técnica | 8% |
| M7 | 37 | Repositório com histórico real de colaboração | 8% |
| M8 | 40 | Documentação consolidada e apresentação | 8% |

A coordenação de cada marco é rotativa: quem coordena um marco não pode
coordenar o seguinte. Com oito marcos, todas as pessoas da equipe coordenam ao
menos uma vez.

Especificação completa em [`projeto/README.md`](projeto/README.md).

---

## Modelos de artefato

A pasta [`modelos/`](modelos/) contém os formatos usados nas entregas do projeto.
Cada modelo tem as seções esperadas e um exemplo preenchido referente ao Rota
Escolar, para que fique claro o nível de detalhe pretendido.

| Modelo | Usado em |
|---|---|
| [`termo-abertura.md`](modelos/termo-abertura.md) | M1 |
| [`declaracao-escopo.md`](modelos/declaracao-escopo.md) | M1 |
| [`eap.md`](modelos/eap.md) | M1 |
| `registro-riscos.md` | M1 |
| `documento-requisitos.md` | M3 |
| `matriz-rastreabilidade.md` | M3 |
| `adr.md` | M5 |
| `documento-arquitetura-c4.md` | M5 |
| `plano-manutencao.md` | M6 |

Os modelos são ponto de partida, não formulário a preencher. Uma equipe pode
acrescentar seções, e frequentemente deve.

---

## Índice das listas

| UA | Aulas | Tema |
|---|---|---|
| **1** | [01](exercicios/aula01) · [02](exercicios/aula02) · 03 · 04 · 05 | Gerenciamento de projetos |
| **2** | 06 · 07 · 08 · 09 · 10 · 11 | Modelos e metodologias |
| **3** | 12 · 13 · 14 · 15 · 16 · 17 | Requisitos |
| **4** | 18 · 19 · 20 · 21 · 22 · 23 · 24 | Modelagem UML e orientação a objetos |
| **5** | 25 · 26 · 27 · 28 · 29 · 30 | Projeto e arquitetura |
| **6** | 31 · 32 · 33 · 34 | Ciclo de vida e manutenção |
| **7** | 35 · 36 · 37 | Gerência de configuração e versões |
| **8** | 38 · 39 · 40 | Documentação e colaboração |

As listas são publicadas na semana da aula correspondente.

---

## Bibliografia

**Básica**
- PRESSMAN, R.; MAXIM, B. *Engenharia de Software: uma abordagem profissional*. 9ª ed.
- SOMMERVILLE, I. *Engenharia de Software*. 10ª ed.
- LARMAN, C. *Utilizando UML e Padrões*. 3ª ed.

**Complementar**
- PROJECT MANAGEMENT INSTITUTE. *Guia PMBOK*. 7ª ed.
- SCHWABER, K.; SUTHERLAND, J. *Guia do Scrum* — <https://scrumguides.org>
- FOWLER, M. *Refatoração*. 2ª ed.
- MARTIN, R. C. *Arquitetura Limpa*.
- BROWN, S. *The C4 Model* — <https://c4model.com>
- CHACON, S.; STRAUB, B. *Pro Git*, 2ª ed., gratuito em <https://git-scm.com/book/pt-br>
- BROOKS, F. *O Mítico Homem-Mês*.

---

## Colaboração e integridade

É permitido discutir ideias com colegas, consultar livros, normas e material
disponível na internet, e usar assistentes de IA. O uso de IA deve ser declarado
no `RESPOSTAS.md` ou no `README.md` do projeto, indicando em quais partes e de
que forma.

O critério é o mesmo aplicado a qualquer fonte: é preciso entender e conseguir
defender cada decisão registrada. Em uma unidade curricular em que 30% da nota
está na justificativa, texto que não se sustenta em uma pergunta perde valor de
qualquer maneira.

Não é permitido apresentar como próprio o artefato produzido por outra equipe, nem
entregar documento cujas decisões a equipe não consiga explicar.

---

Dúvidas podem ser registradas como [issue](../../issues) neste repositório.
