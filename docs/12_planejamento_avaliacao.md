# Entrega 12: Planejamento da avaliação de usabilidade (DECIDE)

**Data:** 17/11/2026  
**Status:** 🟩 concluída  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.

## O que está sendo avaliado

A avaliação investiga a qualidade da interação com a aplicação: entender a trilha, descobrir por onde começar, achar onde estudar cada tópico, tirar uma dúvida e consultar o grafo de conhecimento. Ela não avalia se o modelo escolhe os tópicos certos. Isso é avaliado no TCC (F1 do núcleo de 0,82).

Nada é simulado: os participantes usam a aplicação em funcionamento, e a trilha é gerada pelo modelo na hora. Para que um erro do modelo não se confunda com um problema de interface, todos recebem o mesmo problema, cuja trilha foi conferida antes pela equipe. Se o modelo devolver uma trilha diferente durante a sessão, o moderador registra o fato, e os critérios são avaliados sobre a trilha exibida.

É uma avaliação somativa sobre o sistema implementado. Os resultados alimentam o redesenho (Entrega 8, seção 4.3).

## A. Método DECIDE

| Etapa | Aplicação no projeto |
|---|---|
| **D: Determine the goals** | Verificar se o aluno iniciante descobre, sem ajuda, por qual tópico começar a estudar para resolver um problema, e se acha onde estudar cada tópico. As metas são as de P01 na Entrega 8: MU01, MU02, MU03 e MU06. As metas de P02 (MU04 e MU05) ficam fora desta rodada. |
| **E: Explore the questions** | O aluno conclui a tarefa sem ajuda e em quanto tempo? Escolhe um ponto de partida que respeita a ordem da trilha? Acha o livro e o capítulo de um tópico? A interface tem problemas de feedback e de recuperação de erros? |
| **C: Choose the evaluation paradigm and techniques** | Dois métodos complementares. **Avaliação heurística** (Entrega 13): cada integrante inspeciona as telas com as 10 heurísticas de Nielsen e encontra problemas sem depender de usuários. **Teste de usabilidade por observação** (Entrega 14): alunos fazem tarefas enquanto falam em voz alta; mede as metas da Entrega 8. |
| **I: Identify the practical issues** | 3 alunos com o perfil de P01. Sessões individuais, presenciais, no notebook da equipe, com Chrome. Um integrante modera e anota em cada sessão, alternando entre as sessões. Piloto interno: um integrante aplica as instruções ao outro antes do primeiro participante. Risco técnico: o modelo precisa estar em execução; a equipe confere antes de cada sessão e remarca se estiver fora do ar. |
| **D: Decide how to deal with ethical issues** | Termo de consentimento antes do teste, dizendo que a interface é avaliada, não a pessoa. Participantes identificados como U01 a U03. Entrada como convidado, sem e-mail. A sessão não é gravada, para preservar a privacidade; o registro é feito por anotação. O participante pode parar a qualquer momento. |
| **E: Evaluate, interpret and present the data** | Sucesso, tempo, ajudas, erros e SEQ por tarefa e por participante, comparados com as metas da Entrega 8. Problemas observados e da inspeção heurística classificados pela severidade de 0 a 4 e apresentados em tabela, do mais grave ao menos grave. |

## B. Perguntas de avaliação

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O aluno descobre por qual tópico começar sem ajuda? | observação (UT01) | sucesso, pedidos de ajuda | MU01: os 3 participantes concluem sem ajuda |
| QA02 | Quanto tempo ele leva para descobrir? | observação (UT01) | tempo | MU02: mediana ≤ 3 min |
| QA03 | Ele acha a tarefa fácil? | questionário pós-tarefa (UT01) | SEQ de 1 a 7 | MU03: média ≥ 5,5 |
| QA04 | Ele escolhe um ponto de partida que respeita a ordem da trilha? | observação (UT01) | tópico indicado | MU06: nenhum participante indica um tópico que depende de outro na trilha |
| QA05 | Ele acha onde estudar um tópico e o que estudar antes dele? | observação (UT02 e UT04) | sucesso, tempo | os 3 participantes concluem sem ajuda |
| QA06 | A interface tem problemas de feedback, consistência e recuperação de erros? | avaliação heurística | violações das heurísticas H1 a H10 | nenhum problema de severidade 3 ou 4 nos fluxos de T01 |

Com 3 participantes, 2 conclusões em 3 dão 67%, abaixo dos 78% de MU01. Por isso o critério exige que os 3 concluam. Pelo mesmo motivo, MU06 (≤ 10%) não admite nenhum erro.

Durante as tarefas, o moderador também anota duas metas qualitativas da Entrega 8: se o participante reenvia a questão ou desiste durante o processamento ("processando" ou "travou") e se ele menciona o aviso de que a IA pode errar.

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| Perfis | Aluno iniciante em programação competitiva (P01) |
| Critérios de inclusão/exclusão | Inclusão: aluno de computação que sabe programar e tem pouca ou nenhuma prática em programação competitiva. Exclusão: integrantes do time de maratona, que são mais experientes que P01 (Entrega 7), e quem já usou a aplicação. |
| Nº de participantes | 3 alunos no teste; 2 integrantes da equipe na avaliação heurística |
| Ambiente | Presencial, em sala tranquila, uma sessão por vez |
| Dispositivo | Notebook da equipe, com Chrome, mouse e tela de pelo menos 14 polegadas |
| Protótipo/versão | Aplicação em funcionamento, a mesma das telas da Entrega 11, acessada pela entrada como convidado |
| Teste piloto | Interno, em 17/11/2026: um integrante aplica as instruções e as tarefas ao outro, para conferir a clareza das instruções e o tempo da sessão |

**Fora do teste com usuários:** avaliar a trilha (O03) e marcar tópico como estudado (O05) são ações de um clique e ficam para a avaliação heurística, para a sessão não ficar longa. A tela inicial de login também fica fora, porque não faz parte das tarefas.

**Pré-teste:** antes das tarefas, o moderador pergunta o semestre, o tempo de prática em programação competitiva e o que o aluno usa hoje quando trava em um problema (Entrega 7). Esses dados ajudam a interpretar os resultados.

## D. Lista de tarefas de avaliação

O problema usado é o [Weird Algorithm (CSES 1068)](https://cses.fi/problemset/task/1068). O participante recebe o enunciado em texto, copiado do CSES. A trilha conferida pela equipe tem 3 tópicos: Variáveis e tipos de dados → Estruturas condicionais (if/else) → Laços de repetição (for/while).

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | "Você está treinando para uma competição e travou neste problema. Use a ferramenta para descobrir por qual assunto começar a estudar e explique por quê." | T01, O01 e O02; MU01, MU02, MU03 e MU06 | Indica um tópico que não depende de outro na trilha exibida (Variáveis e tipos de dados) e justifica pela ordem | 5 min |
| UT02 | "Você decidiu estudar laços de repetição. Descubra em que parte do livro de referência esse assunto é tratado." | O04; saber onde estudar cada tópico | Diz que o assunto não tem capítulo específico no CLRS, por ser um tema de programação básica | 2 min |
| UT03 | "Você ainda não entendeu quando usar um laço que repete sem saber quantas vezes. Tire essa dúvida usando a ferramenta." | O06 | Obtém uma resposta sobre o assunto, pelo painel do tópico ou pelo chat | 3 min |
| UT04 | "Um colega comentou sobre caminhos mínimos de origem única. Descubra o que você precisa estudar antes desse assunto." | O07 e O04 | Cita os dois pré-requisitos: busca em largura (BFS) e heap e heapsort. O caminho usado é registrado | 3 min |

## E. Instrumentos

- [Termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- [Questionário pós-teste](../instrumentos/questionario_pos_teste.md)

## F. Plano de análise

- **Sucesso total:** o participante conclui sozinho, dentro do tempo-limite.
- **Sucesso parcial:** conclui depois de uma ajuda do moderador.
- **Falha:** desiste, passa do tempo-limite ou dá uma resposta errada sem perceber.
- **Erro:** ação que afasta o participante do objetivo, como abrir um tópico que não é o pedido. Em UT01, indicar um tópico que depende de outro conta como erro de MU06.
- **Ajuda:** qualquer esclarecimento do moderador além de repetir a instrução.
- **Tempo:** medido com cronômetro pelo moderador, do momento em que o participante termina de ler a instrução até dizer a resposta.
- **Satisfação:** SEQ de 1 a 7 após cada tarefa, e perguntas abertas no fim da sessão.
- **Falas:** as falas em voz alta são anotadas e agrupadas por tela e por tipo de dificuldade.
- **Priorização:** problemas classificados pela severidade de Nielsen: 0 (não é problema), 1 (cosmético), 2 (pequeno), 3 (grande) e 4 (catastrófico). A severidade considera frequência, impacto e persistência.
- **Comparação com as metas:** uma tabela por tarefa, com o resultado de cada participante, a mediana ou média e a meta da Entrega 8 ao lado.

## Checklist

- [x] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [x] Perguntas de avaliação têm método e evidência correspondentes.
- [x] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [x] Dados ou processamentos simulados no protótipo estão declarados.
- [x] Tarefas vêm de objetivos/cenários relevantes.
- [x] Critérios de sucesso foram definidos antes da coleta.
- [x] Questões práticas e éticas estão resolvidas.
- [x] Instrumentos estão prontos antes da Entrega 13/14.
- [x] Plano diz como dados serão analisados e apresentados.
