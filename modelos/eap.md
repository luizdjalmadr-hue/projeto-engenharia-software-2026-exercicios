# Modelo — EAP e Dicionário

Usado no M1.

A EAP (Estrutura Analítica do Projeto) decompõe o trabalho hierarquicamente. Seu
propósito não é listar tarefas, e sim garantir que **nada foi esquecido** — porque
só se estima, atribui e acompanha aquilo que está representado.

---

## Regras de construção

| Regra | Enunciado |
|---|---|
| Decomposição por entregas | cada nó é algo que **existe** ao final, não uma atividade |
| Regra dos 100% | a soma dos filhos é exatamente igual ao pai |
| Regra dos 8 a 80 | cada pacote de trabalho representa de 8 a 80 horas |
| Teste da atribuição | é possível nomear **uma** pessoa responsável pelo pacote |
| Teste da conclusão | é possível verificar, olhando algo concreto, se terminou |

---

## Estrutura, em PlantUML

```
@startwbs
* 1. <Nome do projeto>
** 1.1 Gerência do projeto
*** 1.1.1 Plano de projeto [24h]
*** 1.1.2 Relatórios de acompanhamento [40h]
** 1.2 <Entrega>
*** 1.2.1 <Pacote> [__h]
@endwbs
```

A gerência do projeto deve ser a primeira entrega. Omiti-la subestima o esforço
total do projeto em 10% a 15%, de forma sistemática.

Ao menos duas entregas devem ser de trabalho que **não** é software: migração de
dados, treinamento, documentação, implantação, acompanhamento.

---

## Dicionário da EAP

Uma entrada por pacote de trabalho.

```markdown
### <código> — <nome do pacote>

| Campo | Conteúdo |
|---|---|
| Descrição | o que este pacote produz |
| Entrega | o artefato ou resultado concreto |
| Responsável | |
| Estimativa | __ horas |
| Predecessor | quais pacotes precisam terminar antes |
| Critério de conclusão | como se verifica que terminou |
| Premissas | o que se assume verdadeiro |
| **Exclui** | o que este pacote NÃO faz |
```

O campo **exclui** é o mais importante e o mais esquecido. Ele evita a lacuna
entre pacotes vizinhos, em que cada lado supõe que o outro faz a parte do meio.

---

## Erros frequentes neste artefato

**Decomposição por fases.** Nós chamados Análise, Projeto, Implementação e Testes
formam um ciclo de vida disfarçado de EAP. Nenhum deles pode ser aceito ou
rejeitado.

**Gerência do projeto ausente.** Gerenciar consome horas e precisa estar
representado.

**Somente software.** Migração e treinamento são escopo do projeto.

**Pacotes de 200 horas.** Escondem progresso: durante semanas o relatório dirá
"em andamento", sem que se saiba se está perto do fim.

**Pacotes de 2 horas.** Produzem uma EAP de 300 folhas que ninguém acompanha.

**Dicionário ausente.** A EAP sozinha parece suficiente até o momento em que duas
pessoas discordam sobre o que um pacote inclui.
