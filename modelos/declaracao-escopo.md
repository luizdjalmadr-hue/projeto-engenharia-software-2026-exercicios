# Modelo — Declaração de Escopo

Usado no M1. Extensão esperada: 2 a 4 páginas.

A declaração de escopo registra o acordo sobre o que o projeto compreende. Sua
utilidade concentra-se em duas seções: as **exclusões** e os **critérios de
aceitação**. As demais tendem a sair bem por si; essas duas exigem trabalho e são
as que evitam conflito.

---

```markdown
# Declaração de Escopo — <nome do projeto>

**Versão:** 1.0
**Data:**
**Aprovada por:**

## Inclusões

| # | Item |
|---|---|
| I1 | |

Cobrir tanto o escopo do produto (funções do sistema) quanto o escopo do projeto
(migração, treinamento, documentação, implantação).

## Exclusões

| # | Item | Observação |
|---|---|---|
| E1 | | |

Cada exclusão tem observação explicando a razão. A observação é o que encerra a
discussão futura — a lista seca não encerra.

Escreva aqui aquilo que alguém provavelmente vai pedir no terceiro mês achando
que sempre estivera previsto.

## Entregas

| # | Entrega |
|---|---|
| D1 | |

Entregas são coisas que **existem** ao final, não atividades.

## Critérios de aceitação do projeto

| # | Critério | Como se verifica |
|---|---|---|
| C1 | | |

A segunda coluna é obrigatória. "O sistema deve ser rápido" sem método de
verificação permite discussão infinita sobre em qual máquina e com qual volume de
dados.

Inclua critérios para as entregas que não são software. Treinamento tem critério
de aceitação próprio.
```

---

## Erros frequentes neste artefato

**Seção de exclusões vazia.** É a seção mais barata de escrever e a que mais
evita conflito.

**Exclusão sem observação.** "Rastreamento em tempo real" na lista comunica a
decisão; "rastreamento em tempo real — exige hardware embarcado não previsto no
orçamento" comunica a razão, e a razão é o que evita a discussão voltar.

**Inclusões apenas de software.** Se a lista não menciona migração, treinamento
nem documentação, o projeto está dimensionado só para o escopo do produto.

**Critério de aceitação sem método de verificação.** Transforma o encerramento do
projeto em disputa de percepção.

**Nenhum critério para o que não é software.** Um sistema perfeito que as pessoas
não sabem usar não atinge o objetivo do termo de abertura.
