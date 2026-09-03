# Declaração de Escopo - Rota Escolar

## 1. Objetivo do projeto
Substituir o controle em planilha do transporte escolar municipal por um sistema que atenda 3.200 estudantes em 96 rotas, com 28 veículos, reduzindo de 80 para 20 horas o esforço de cada prestação de contas trimestral.

## 2. Escopo do produto
O sistema entregará:
- Cadastro de estudantes, responsáveis, escolas, rotas, veículos e condutores
- Verificação de elegibilidade por distância entre residência e escola
- Controle de vagas por veículo
- Registro de frequência diária, inclusive sem conexão de rede
- Relatórios da prestação de contas trimestral

## 3. Escopo do projeto
Além de construir o software:
- Levantar requisitos junto às 19 escolas da rede
- Migrar a planilha atual, com 96 rotas, para a base nova
- Digitalizar 3.200 fichas de endereço
- Treinar 31 motoristas e 24 monitoras
- Operar um piloto em uma rota antes de expandir para as 96

## 4. Fora do escopo
- Rastreamento dos veículos por GPS em tempo real
- Aplicativo para o responsável acompanhar o embarque
- Integração com o sistema de folha de pagamento da prefeitura
- Gestão de manutenção mecânica da frota

## 5. Critérios de aceitação
| Código | Critério | Como será verificado |
|---|---|---|
| CA-1 | Prestação de contas trimestral em até 20 horas | Cronometrar o fechamento real |
| CA-2 | Registro de frequência sem conexão nas 23 rotas sem sinal | Teste em campo, uma rota de cada região |
| CA-3 | 100% dos 3.200 estudantes migrados sem perda de dado | Conferência por amostra de 5% |

## 6. Restrições
- Orçamento de R$ 180.000
- Prazo de 10 meses
- 23 das 96 rotas não têm sinal de celular
-## Dicionário da EAP
| Código | Pacote | Entrega verificável | Esforço (h) |
|---|---|---|---|
| 1.2.1 | Entrevistas nas 19 escolas | 19 roteiros preenchidos e assinados | 76 |
| 1.3.3 | Frequência offline | Registro funcionando sem rede, com sincronização | 10 |
| 1.4.1 | Digitalização das fichas | 3.200 registros conferidos por amostra | 160 |
| 1.6.1 | Treinamento de motoristas | 31 motoristas com presença registrada | 48 |