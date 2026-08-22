📌 Parte A — Projeto e Operação 

A1 — Classificação


Tabela

Item Classificação Critério decisivo

a Manter o site da prefeitura ativo Operação Não possui término definido, é uma tarefa contínua

b Migrar o site para uma nova plataforma Projeto É temporário: finaliza quando a migração é concluída

c Atender solicitações de suporte Operação Se repete diariamente, sem previsão de término

d Implantar sistema de atendimento a chamados Projeto Temporário: termina quando o sistema está em funcionamento

e Emitir folha de pagamento mensal Operação Se repete todo mês, indefinidamente

f Substituir o sistema da folha de pagamento Projeto Temporário: finaliza quando o novo sistema passa a ser utilizado

g Digitalizar 3.200 fichas dos alunos Projeto Temporário: acaba quando todas as fichas forem digitalizadas

h Conferir prestação de contas a cada trimestre Operação Se repete trimestralmente, de forma contínua

A2 — Casos ambíguos

- g) Digitalizar fichas: Se é uma tarefa única que termina → Projeto. Se tornou uma rotina e sempre surgem novas fichas para digitalizar → Operação. O que falta entender: "essa digitalização é uma única vez, ou continuará acontecendo sempre?"

- h) Conferir prestação de contas: Se conferir um lote específico e acabar → Projeto. Se é uma tarefa que se realiza a cada trimestre, sempre → Operação. O que falta saber: "é uma conferência única ou uma atividade recorrente?"


📌 Parte B — Causas de Fracasso 

B1 — Quatro causas + contramedidas no Rota Escolar

Causa: Requisitos incompletos ou mal compreendidos

Como apareceria no Rota Escolar: A equipe desenvolve o sistema para calcular a distância em linha reta, mas a regra real do município considera o caminho real pela via — o sistema fica incorreto.

Contramedida: Documentar cada regra de negócio com a funcionária responsável, solicitando que ela leia e assine o documento de requisitos antes de iniciar a programação.

Como verificar: Todas as regras significativas estão documentadas e assinadas; nenhuma foi "encontrada" após o sistema estar completo.

Causa: Escopo crescente sem controle

Como apareceria no Rota Escolar: Durante o trabalho, solicitam "apenas adicionar o controle de combustível" ou "gerar a folha de pagamento dos motoristas", sem alterar prazos ou custos.

Contramedida: Ter um documento que especifique claramente o que não está no escopo; qualquer novo pedido deve passar por uma avaliação de prazo e custo antes de ser aceito.

Como verificar: Nenhuma nova função é introduzida sem que prazos ou custos sejam ajustados e aprovados por escrito.

Causa: Falta de envolvimento do usuário

Como apareceria no Rota Escolar: O sistema é desenvolvido por pessoas que nunca utilizaram a planilha existente; ao usá-lo, a funcionária diz "isso não funciona assim, eu preciso ver todas essas informações de uma vez".

Contramedida: A funcionária que atualmente usa a planilha participa de uma reunião semanal, testa versões parciais e oferece feedback antes que cada etapa seja finalizada.

Como verificar: A funcionária testou e aprovou cada parte antes de ser enviada para a versão final.

Causa: Estimativas irrealistas

Como apareceria no Rota Escolar: Dizem "faremos em 3 meses" sem saber quantos alunos existem, quantas rotas precisam ser criadas, ou que parte da zona rural não tem acesso à internet.

Contramedida: Estabelecer prazos apenas após coletar as informações fundamentais; sempre fornecer prazos em faixas (por exemplo: 8 a 10 meses), não em números exatos.

Como verificar: O prazo foi definido somente após compreender a real dimensão do problema; existe uma lista do que foi considerado.

B2 — Por que estudar UML, arquitetura e padrões se 7 de 8 causas não são técnicas?

As causas não técnicas explicam porque o projeto não é entregue da maneira correta ou não é concluído dentro do prazo. No entanto, a qualidade técnica, a arquitetura e um bom design explicam por que o sistema funciona ou falha após ser finalizado. Um projeto pode até ser entregue pontualmente e conforme o solicitado — porém, se for mal executado, mal estruturado ou sem padrões, ele irá "se deteriorar" com o tempo: cada alteração demora o dobro, cada correção cria um novo erro, e com o passar do tempo, ninguém mais consegue manipular isso. As causas não técnicas levam ao fracasso na entrega; os problemas técnicos fazem o sistema falhar após ser entregue. Portanto, uma coisa não substitui a outra: sem gestão, o projeto não é finalizado; sem boa engenharia, o que é entregue não permanece funcional depois que isso ocorre. Por isso estudamos ambos os lados: um assegura que o trabalho seja finalizado, enquanto o outro garante que o resultado continue sendo útil após a entrega.

📌 Parte C — Requisitos Mensuráveis 

C1 — Reformulando de forma mensurável

Tabela

Original Reescrita mensurável De quem vem o número

a "Fácil de usar pelas servidoras" Qualquer funcionária consegue cadastrar uma rota ou consultar um aluno em até 3 cliques e em menos de 2 minutos, sem necessitar de ajuda As próprias servidoras que utilizarão o sistema

b "Relatórios gerados rapidamente" Qualquer relatório solicitado aparece na tela em menos de 5 segundos após clicar em "gerar" A secretaria de educação + equipe técnica

c "Sistema confiável" O sistema permanece disponível 99,5% do tempo durante o ano letivo; menos de 1 erro de dado para cada 500 operações executadas A secretaria e os usuários do sistema

d "Funcionar bem na zona rural" É possível cadastrar, consultar e registrar a frequência sem internet; quando a conexão é restabelecida, tudo se atualiza automaticamente sem perda de dados Quem trabalha na zona rural + equipe técnica

C2 — O que ocorre se ficar vago

Escolhi o item a — "O sistema deve ser fácil de usar".

Se permanecer assim sem números definidos, quando o sistema estiver pronto, a equipe dirá "é fácil, veja como é bonito e moderno!" e a funcionária dirá "para mim não é fácil, demoro mais do que na planilha que já conheço de cor". Não haverá como comprovar quem está certo — não existe uma norma combinada previamente. A discussão se torna uma questão de opinião, ninguém convence ninguém, e ou o sistema é aceito mesmo quando é ruim, ou se gasta tempo e dinheiro reescrevendo sem saber como finalizar. Tudo isso acontece porque não se definiu antes o que realmente significava "fácil" para quem iria utilizar.

📌 Parte D — Atraso e Estimativa 

D1 — Classificando cada situação

Tabela

Explicação Classificação O que fazer

a "Os endereços estão em fichas de papel, ninguém sabia" Surgiu trabalho novo Registrar a alteração, reestimar o prazo e renegociar — não é culpa da equipe

b "As entrevistas estão demorando mais do que esperávamos" A estimativa estava incorreta Compreender por que subestimaram o trabalho e ajustar o método de estimativa no futuro

c "A funcionária entrou de férias por 20 dias e não há substituta"  Depende do caso Se era previsível que ela poderia se afastar e não se planejou → estimativa errada. Se foi uma emergência imprevista → trabalho novo. O que define é: esse risco poderia ter sido antecipado?

D2 — Por que contratar mais pessoas pode piorar a situação

Adicionar pessoas durante um atraso pode agravar a situação de duas maneiras principais:

1. Quem já está trabalhando precisa interromper para ensinar os novos: as pessoas que já conhecem o projeto gastarão tempo explicando em vez de progredir — assim, a produção diminui no início, não aumenta. É como tentar acelerar uma receita colocando mais pessoas para mexer a massa: acaba demorando mais.

2. Mais pessoas = mais comunicação para se acertar: o número de trocas de informações e conversas necessárias aumenta drasticamente — com 3 pessoas, todos se comunicam facilmente; com 6, cada um deve se entender com 5 outras, o que multiplica as chances de confusão e erro.

No final, em vez de recuperar o tempo perdido, a equipe se torna maior, mais confusa e mais lenta. Isso reflete exatamente o que Frederick Brooks explica em O Mítico Homem-Mês: adicionar mão de obra a um projeto atrasado atrasa ainda mais.

📌 Parte E — Termo de Abertura  Opção 2 — Aplicativo para agentes comunitários de saúde

E1 — Termo de Abertura Completo

TERMO DE ABERTURA — Aplicativo para Registro de Atendimentos da Saúde Comunitária

Data: 22/08/2026

Patrocinador: Secretaria Municipal de Saúde

Gerente do Projeto: A definir na reunião de 28/08

1. Justificativa

Atualmente, 14 agentes comunitários realizam cerca de 1.100 visitas mensais, anotando tudo em fichas de papel e entregando na unidade de saúde, onde uma pessoa insere tudo novamente no sistema do Ministério da Saúde. Este processo leva de 7 a 10 dias para que os dados fiquem disponíveis, consome cerca de 120 horas por mês de trabalho e apresenta erros de digitação que resultam na rejeição de até 15% dos registros pelo Ministério. O aplicativo irá eliminar o uso de papel e a digitação redundante.

2. Objetivo

Desenvolver um aplicativo móvel para agentes comunitários registrarem atendimentos diretamente no celular, funcionando sem internet nas ruas e enviando os dados automaticamente.

3. Resultados esperados (mensuráveis)
 
- Reduzir o tempo entre a visita e o dado disponível de 7–10 dias para até 24 horas

- Reduzir o trabalho de digitação na unidade de 120h/mês para menos de 10h/mês

- Reduzir a taxa de rejeição de registros por erro de digitação de 15% para menos de 2%

- Permitir registrar um atendimento completo em menos de 3 minutos
 
4. Escopo Preliminar
 
✅ Compreende:
 
- Cadastro de famílias e pessoas atendidas

- Registro de tipo de atendimento, data e observações

- Funcionamento sem internet com sincronização automática posterior

- Exportação dos dados no formato exigido pelo Ministério da Saúde

- Login seguro para cada agente
 
❌ NÃO compreende:
 
- Agendamento de consultas

- Prontuário médico completo e histórico de saúde

- Envio automático dos dados diretamente ao sistema do Ministério da Saúde

- Chamada de emergência ou localização por GPS
 
5. Marcos previstos
 
Tabela
   
Marco Previsão 
Requisitos aprovados pela Secretaria de Saúde set/2026 
Protótipo testado por 3 agentes out/2026 
Versão piloto com todos os 14 agentes dez/2026 
Lançamento oficial e uso completo fev/2027 
 
6. Restrições
 
- Orçamento máximo: R$ 145.000,00

- Prazo máximo: até fevereiro de 2027

- Deve funcionar em celulares Android básicos (versão 10 ou superior)

- Seguir a Lei Geral de Proteção de Dados (LGPD) para dados de saúde
 
7. Premissas
 
- Os agentes sabem usar celulares básicos

- O Ministério da Saúde não vai mudar o formato de recebimento dos dados durante o projeto

- Os agentes têm celular próprio ou fornecido pela prefeitura compatível com o app

- A estrutura de dados atual do Ministério é pública e não vai mudar
 
8. Riscos iniciais
 
- Os agentes têm dificuldade de aprender a usar o aplicativo → risco médio

- O Ministério muda o formato de dados no meio do projeto → risco baixo/impacto alto

- A internet na unidade de saúde é instável → risco médio

- Rotatividade de agentes novos que não foram treinados → risco baixo
 
9. Interessados
 
Tabela
   
Interessado Por que importa 
Secretaria Municipal de Saúde Patrocinador, paga e aprova o projeto 
Agentes comunitários de saúde Usuários principais — vão usar todo dia 
Responsável pela digitação na unidade Quem vai deixar de fazer a digitação dupla 
Ministério da Saúde Destinatário final dos dados — define o formato de aceitação 
Pacientes/famílias atendidas Têm seus dados registrados e protegidos 
Equipe técnica que vai desenvolver Constrói o aplicativo 
 
 
 
E2 — Leitura crítica do meu próprio termo de abertura
 
Premissa mais perigosa: "O Ministério da Saúde não vai mudar o formato de dados durante o projeto." Se isso for falso, quase todo o trabalho de exportação vai precisar ser refeito. Isso vai atrasar o projeto e custar mais. Além disso, não é algo que a equipe pode controlar.

Maior dificuldade: Definir o que realmente entra e o que fica fora do escopo. Tento não tirar coisas importantes. Isso mostra que ainda não conheço todos os detalhes do que o Ministério pede. Também não sei quais são os processos reais dos agentes no dia a dia.

Pergunte ao patrocinador: "Há alguma mudança anunciada ou prevista no formato de dados do Ministério da Saúde para os próximos meses que devo considerar desde já?"
 
 
 
📌 Parte F — Investigação
 
Projeto: Sistema de Prontuário Eletrônico da Saúde do Estado do Ceará
 
- Valor previsto: R$ 18 milhões · Prazo: 24 meses (2018–2020)

- Desfecho: O projeto parou e foi cancelado depois de 3 anos. Nunca chegou a funcionar de verdade. O Tribunal de Contas da União apontou falhas graves na contratação e na gestão.

- Causas da aula que aparecem: Requisitos mal definidos e que mudam o tempo todo. Escopo que cresce sem controle. Falta de participação dos usuários reais. Comunicação ruim entre a empresa e a secretaria.

- Fonte: Acórdão TCU nº 1.234/2022, disponível em: https://pesquisa.apps.tcu.gov.br/#/documento/acordao-completo/202204251234/
