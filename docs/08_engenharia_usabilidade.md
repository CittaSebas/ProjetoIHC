# Entrega 8: Ciclo de vida e engenharia de usabilidade

**Data:** 28/10/2026 (revisada em 09/11/2026 após o feedback do professor)  
**Status:** `🟦 revisada após feedback`, com metas provisórias até a análise dos dados da Entrega 7  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | Modelo Qwen3-4B-Instruct-2507 com ajuste fino, que classifica os rótulos do enunciado, mapeia para tópicos pedagógicos e monta a trilha | desempenho técnico não é substituído pelo teste de IHC |
| camada de interação da disciplina | Interface web. **Aluno (P01), perfil que dirige o projeto:** apresentar a questão, acompanhar o processamento e ver a trilha com a ordem e a dependência entre tópicos e a fonte de cada um (F01 a F05; tarefa T01). **Professor (P02), de forma provisória enquanto H11 estiver aberta:** ver de que fonte veio cada tópico da trilha, hoje o livro do Cormen (*Introduction to Algorithms*), na mesma interface do aluno (tarefa T02) | compreensão, eficácia, eficiência, satisfação, erros, acessibilidade etc. |
| integrações/dados simulados |  No protótipo em papel (Entrega 6), o processamento e a trilha são simulados pela equipe | Os testes avaliam como a trilha e as fontes são apresentadas, não se o modelo acertou. As trilhas exibidas podem conter erros reais do modelo, o que precisa ser considerado ao analisar MU01 e MU06 |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Aplicação web acessada pelo navegador. A inferência roda no Kaggle | O aluno não instala nada nem precisa de ambiente Python, barreira registrada na Entrega 1. A interface pode seguir convenções de páginas web que o público já usa (H12, H26) |
| Hardware/dispositivos | Do lado do aluno, notebook ou desktop, com o enunciado aberto em outra aba (H21, a confirmar pelas perguntas 9 e 10 do questionário da Entrega 7). Do lado do professor, computador usado na preparação de aula ou de treino (P02, hipótese). Do lado do sistema, ambiente de execução do Kaggle | A trilha precisa caber ao lado do enunciado numa tela de notebook. Se a Entrega 7 mostrar uso de celular, a equipe terá que desenvolver telas para uso em dispositivo móvel. |
| Capacidades | **Colar textos longos da área de transferência.** Justificativa: o enunciado inteiro é a entrada do modelo (T01, 1.1)<br>**Desenhar grafos interativos, com zoom e destaque.** Justificativa: é o que permite mostrar a ordem e a dependência entre tópicos (F03)<br>**Abrir links externos.** Justificativa: leva o aluno à fonte de cada tópico (F04, T02)<br>**Infraestrutura de acessibilidade do navegador (teclado, zoom, leitor de tela).** Justificativa: oferece a base para atender Q03, mas não torna a interface acessível sozinha. Os componentes precisam de semântica correta, ordem de foco e alternativa textual ao grafo para usar essa base<br>**Inferência em menos de 10 s.** Justificativa: média de 6,4 s por problema no Kaggle, medida pela equipe em 10 problemas (TCC) | Entrada única por colagem, sem configuração prévia (N01, RC01); grafo com zoom e caminho recomendado destacado (Entrega 5); um indicador simples de processamento é suficiente (ver princípio de tempo de resposta na seção 2.3) |
| Restrições | **O modelo pode errar a atribuição de tópicos.** Justificativa: F1 do núcleo de 0,82 em 10 problemas (TCC)<br>**O modelo não devolve grau de confiança por tópico.** Justificativa: a saída do modelo traz só os tópicos<br>**Os tópicos saem em inglês.** Justificativa: os rótulos do modelo são os do Codeforces (Tabela II do TCC)<br>**Grafos ficam ilegíveis em telas pequenas.** Justificativa: muitos nós e arestas num espaço reduzido | Como não há confiança por tópico, a trilha vem com o aviso de que a IA pode cometer erros. Os termos precisam de explicação em português (H05, N05). O grafo precisa de alternativa em lista |
| Conectividade/latência | Exige conexão com a internet. Depende de o serviço no Kaggle estar ativo | Sem conexão, ou com o serviço fora do ar, não há consulta. A interface deve dizer isso claramente em vez de parecer travada |
| Segurança/privacidade | O aluno envia enunciados públicos de juízes online. O enunciado é processado no Kaggle, um serviço externo | No recorte atual não há dado pessoal: enunciados são públicos e não há login. Se o histórico (Q12) ou contas entrarem no escopo, passa a existir dado pessoal e a LGPD se aplica (seção 2.2) |
| Volume de dados/histórico | Cada consulta gera uma trilha para uma única questão. A necessidade de guardar trilhas anteriores está em aberto (Q12, investigada na Entrega 7) | Não há volume que justifique busca, filtros ou paginação. Se Q12 for sustentada, basta uma lista simples das consultas anteriores |
| Tempo de processamento | Média de 6,4 s por problema, medida pela equipe no Kaggle em 10 problemas (TCC). Precisa ser medido de novo se o ambiente de execução mudar | Indicador de que a consulta está sendo processada (F02, RC02). Abaixo de 10 s não é preciso barra de progresso nem botão de cancelar (seção 2.3) |
| Papéis/permissões | Aluno (P01) e, de forma provisória, professor (P02). O professor só consulta a fonte da trilha; não altera trilhas nem fontes. Não há administrador | Como ninguém altera dados, não é preciso controle de permissões. A prevenção de erros fica na entrada: avisar quando o texto enviado está vazio ou não parece um enunciado |

## 2. Princípios gerais do projeto

Inclua apenas normas, leis, padrões e princípios realmente relevantes, explicando **como** afetam o projeto. Não transforme esta seção em lista de links.

### 2.1 Contexto de uso

**Aluno (P01), perfil que dirige o projeto.** Aluno iniciante em programação competitiva, sozinho, em treino individual, no notebook, com o enunciado em outra aba. Chega à ferramenta já travado e frustrado. Não domina o vocabulário do domínio, que está em inglês. Depende de conexão (Entregas 1, 3 e 4).

**Professor (P02), provisório.** Especialista no domínio, prepara aula ou treino com pouco tempo e quer verificar a fonte do material antes de repassá-lo (H24, cenário C02). Este contexto só orienta decisões se H11 for sustentada.

### 2.2 Princípios direcionados ao negócio

Normas e regras que vêm do domínio e condicionam o produto.

| Referência | Descrição e por que importa ao projeto | Decisão/requisito decorrente | Link |
|---|---|---|---|
| LGPD (Lei nº 13.709/2018) | Regula o tratamento de dados pessoais. No recorte atual a interface não coleta dado pessoal: o aluno envia enunciados públicos, sem login. A lei passa a valer para a interface se o histórico (Q12) exigir identificar o aluno. Já vale para a coleta de dados da Entrega 7 | Sem login nem armazenamento de dado pessoal por padrão. Se o histórico entrar no escopo, guardar o mínimo, informar a finalidade e permitir apagar | <https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm> |
| Regra do Codeforces sobre uso de IA (2024) | O Codeforces proíbe usar ferramentas de IA para resolver questões durante rodadas valendo rating. Fora de competição, o uso para treino e estudo é livre. A ferramenta usa IA e recebe enunciados de questões | A interface se apresenta como apoio ao treino, não à competição. Isso apoia manter o uso em competição fora do recorte, mas Q08 continua aberta até a decisão da equipe ser registrada | <https://codeforces.com/blog/entry/133941> |
| Lei de Direitos Autorais (Lei nº 9.610/1998) | As trilhas se apoiam em livros protegidos, hoje o Cormen. Citar a obra é permitido; reproduzir trechos longos não | A trilha indica livro, capítulo e uma explicação curta escrita pela equipe. Não reproduz o texto do livro | <https://www.planalto.gov.br/ccivil_03/leis/l9610.htm> |

### 2.3 Princípios direcionados à interface

Padrões, diretrizes e regras de interação usados para orientar o design. Os quatro primeiros consolidam o que as Entregas 1 a 6 já apontavam.

| Referência | Descrição e por que importa ao projeto | Decisão/requisito decorrente | Link |
|---|---|---|---|
| Visibilidade e reconhecimento (Barbosa e Silva, 2010; heurística 1 de Nielsen) | O sistema deve manter o usuário informado do que está acontecendo. O aluno chega travado e, sem retorno, não distingue "processando" de "travou" (F02) | Indicador de processamento logo após o envio (RC02). Mensagem própria quando o serviço não responder | <https://www.nngroup.com/articles/ten-usability-heuristics/> |
| Limites de tempo de resposta (Nielsen, 1993) | Até cerca de 1 s o usuário mantém o fluxo. Até cerca de 10 s mantém a atenção na tarefa. Acima disso, precisa de indicador de progresso e opção de cancelar | Com a inferência medida abaixo de 10 s, basta um indicador simples. Se o tempo passar de 10 s, a interface precisa de progresso e cancelamento | <https://www.nngroup.com/articles/response-times-3-important-limits/> |
| Correspondência com as expectativas do usuário (Barbosa e Silva, 2010; heurística 2 de Nielsen) | A linguagem deve ser a do usuário. Os tópicos saem em inglês e o iniciante não domina o jargão (H05) | Cada tópico em inglês vem com nome e explicação curta em português (RC03, provisória até a Entrega 7) | <https://www.nngroup.com/articles/ten-usability-heuristics/> |
| Simplicidade na estrutura das tarefas e conteúdo relevante (Barbosa e Silva, 2010; heurística 8 de Nielsen) | Reduzir planejamento e opções concorrentes. O aluno chega com um único objetivo (A01) | Primeira tela com uma única ação: colar o enunciado, sem configuração prévia (N01, RC01) | <https://www.nngroup.com/articles/ten-usability-heuristics/> |
| Projeto para erros (Barbosa e Silva, 2010; heurísticas 5 e 9 de Nielsen) | O modelo erra (F1 do núcleo de 0,82) e o iniciante pode não perceber (H06, H16). A entrada também pode vir vazia ou errada | Aviso de que a IA pode errar junto da trilha; fonte de cada tópico visível para conferência (F04, F05); aviso quando a entrada está vazia ou não parece um enunciado | <https://www.nngroup.com/articles/ten-usability-heuristics/> |
| WCAG 2.2 (W3C) | O resultado central é um grafo, que por padrão não é acessível a leitor de tela nem navegável por teclado. A necessidade específica do público ainda é desconhecida (Q03) | Alternativa textual do grafo como lista ordenada de tópicos (critério 1.1.1); todos os tópicos e links alcançáveis por teclado (2.1.1); dependência entre tópicos não indicada só por cor (1.4.1). Esses critérios valem mesmo que a Entrega 7 não encontre usuários com necessidade declarada | <https://www.w3.org/TR/WCAG22/> |

## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

### 3.1 Metas qualitativas

Metas marcadas como **provisórias** dependem de hipóteses ainda abertas e serão revistas após a análise dos dados da Entrega 7.

| Meta | Para quem/tarefa | Evidência desejada | Justificativa | Estado |
|---|---|---|---|---|
| Compreender por qual tópico começar e o que depende do quê | P01 / T01 | Ao ver a trilha, o aluno diz com as próprias palavras por onde começaria e por quê | A01, N02, F03 | firme |
| Saber onde estudar cada tópico | P01 / T01 | O aluno aponta a fonte indicada para um tópico sem ajuda | N03, F04 | firme |
| Distinguir "processando" de "travou" | P01 / T01 | O aluno não reenvia a questão nem fecha a página durante o processamento | N06, F02, RC02 | firme |
| Entender os termos da trilha ou saber onde consultar na fonte | P01 / T01 | O aluno não para diante de um termo sem saber o que fazer | N05, H05 | provisória (H05) |
| Não sentir que recebeu a solução pronta | P01 / T01 | O aluno diz que ainda vai resolver a questão sozinho | H07 | provisória (H07) |
| Identificar de que fonte veio cada tópico e julgar se pode repassá-lo | P02 / T02 | O professor aponta o livro e o capítulo de um tópico e diz se repassaria aquele material | H24, cenário C02 | provisória (H11) |

### 3.2 Metas quantitativas

População: alunos com o perfil de P01. A definição concreta de "iniciante" (Q02) vem da Entrega 7.

| ID | Meta de Nielsen | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|---|
| MU01 | facilidade de aprendizado | eficácia | taxa de conclusão sem ajuda, no primeiro uso | T01 | ≥ 78% | teste observado | Concluir é dizer, sem ajuda, por qual tópico começaria e por quê (A01, F03). 78% é a taxa mediana de conclusão em cerca de 1.200 tarefas analisadas por Sauro (MeasuringU): é o nível de uma tarefa comum. Abaixo de 49%, a tarefa fica no quartil inferior. Com 5 participantes, a meta exige que 4 concluam |
| MU02 | eficiência | eficiência | tempo mediano | T01 | ≤ 3 min | cronômetro | Do abrir a página até dizer por onde começaria. Inclui colar o enunciado, a inferência (menos de 10 s, medida) e a leitura da trilha. O aluno chega travado e com o tempo de treino correndo (H22); se a consulta demorar mais que a alternativa, ele volta ao chatbot (H19). O valor de 3 min é estimativa da equipe e será recalibrado com o primeiro teste e com o tempo que o aluno tenta sozinho (pergunta 13 do questionário, Q16) |
| MU03 | satisfação | satisfação | Single Ease Question, escala de 1 a 7, após a tarefa | T01 | ≥ 5,5 | questionário pós-tarefa | Sauro (MeasuringU) registra média entre 5,3 e 5,6 em mais de 400 tarefas e 10 mil usuários. A ferramenta concorre com chatbots e editoriais que o aluno já conhece; ficar abaixo da média de tarefas comuns indica que a consulta é percebida como mais difícil que o normal |
| MU06 | baixa taxa de erros | eficácia | proporção de participantes que indicam como ponto de partida um tópico que, na própria trilha exibida, depende de outro | T01 | ≤ 10% | teste observado | É o erro silencioso de maior custo: o aluno estuda na ordem errada e perde tempo de treino sem perceber (H16, H20). Por isso a meta é mais rígida que a de conclusão. Com 5 participantes, a meta exige nenhum erro. A medida avalia a leitura da trilha exibida, não o acerto do modelo |

**Metas provisórias de P02.** As metas abaixo só passam a valer se H11 for sustentada. Até lá, não orientam decisões de interface e não entram na priorização (seção 3.3).

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU04 | eficácia | taxa de conclusão sem ajuda | T02 | ≥ 78% | teste observado | Concluir é o professor apontar, sem ajuda, o livro e o capítulo de onde veio um tópico. Mesma referência de MU01 |
| MU05 | eficiência | tempo mediano | T02 | ≤ 1 min | cronômetro | Da trilha exibida até o professor chegar à fonte de um tópico. O professor tem pouco tempo de preparação (C02). Valor estimado pela equipe, a recalibrar no primeiro teste |

Facilidade de memorização não tem meta quantitativa nesta etapa: ela só pode ser medida com retorno do mesmo participante depois de um intervalo, e a frequência de uso ainda é desconhecida (H08, Q04).

### 3.3 Priorização das metas

Pesos de prioridade entre as cinco metas de usabilidade de Nielsen, somando 100%. Os pesos indicam o que pesa mais nas decisões de design quando houver conflito; não são métricas.

| Meta de Nielsen | Peso | Justificativa | Medida em |
|---|---:|---|---|
| Facilidade de aprendizado | 35% | P01 tem baixo conhecimento do domínio, usa a ferramenta sozinha (H09) e chega travada (H22). Não há quem explique a interface, e cada consulta tende a ser quase um primeiro uso | MU01 |
| Baixa taxa de erros | 25% | O modelo erra (F1 do núcleo de 0,82) e o iniciante pode não perceber (H06, H16). Um erro de leitura da trilha faz o aluno estudar na ordem errada sem saber | MU06 |
| Eficiência | 15% | O aluno quer voltar logo ao treino (H22), mas a tarefa é curta e tem poucos passos | MU02 |
| Satisfação | 15% | A ferramenta concorre com chatbots e editoriais que o aluno já usa (H17 a H19). Se a experiência for pior, ele não volta | MU03 |
| Facilidade de memorização | 10% | A interface tem uma ação principal e pouco a lembrar entre usos. O peso sobe se o histórico (Q12) entrar no escopo, porque aí haverá mais funções para lembrar | sem meta quantitativa nesta etapa |
| **Total** | **100%** | | |

## 4. Como o ciclo será iterado

### 4.1 Modelo adotado

O projeto segue o **Ciclo de Vida da Engenharia de Usabilidade de Mayhew**, apresentado em aula (Barbosa e Silva, 2010). Ele tem três fases: análise de requisitos; projeto, teste e desenvolvimento em três níveis; e instalação. Cada nível é repetido até as metas serem atingidas, antes de passar ao próximo.

### 4.2 Fases e entregas da disciplina

| Fase do ciclo | Etapa | Entregas | Estado real |
|---|---|---|---|
| Análise de requisitos | Perfil do usuário | 1, 3 e 7 | Proto-personas prontas. Coleta da Entrega 7 planejada, ainda não aplicada |
| | Análise do contexto da tarefa | 4 e 5 | Cenários e tarefas prontos. T01 e T02 em revisão após o feedback da Entrega 5 |
| | Capacidades e restrições da plataforma | 8, seção 1 | Feita |
| | Princípios gerais do projeto | 8, seção 2 | Feita |
| | Metas de usabilidade | 8, seção 3 | Feitas, com valores provisórios |
| Nível 1: projeto essencial | Modelo conceitual | 9 e 10 | Entrega 9 em andamento |
| | Maquete em papel e teste por simulação | 6 | Telas prontas, walkthrough ainda não realizado |
| Nível 2: padrões de telas | Protótipo de maior fidelidade | 11 | Não iniciado |
| | Avaliação | 12, 13 e 14 | Não iniciadas |
| Nível 3: projeto detalhado | Projeto e teste do sistema final | fora da disciplina | Fica para a implementação do TCC |
| Instalação | Retorno de usuários após uso real | fora da disciplina | Não se aplica |

A Entrega 6 deveria anteceder esta entrega no cronograma. Seu walkthrough está pendente e será feito antes do protótipo da Entrega 11.

### 4.3 Como cada iteração funciona

1. **Análise alimenta as metas.** Personas (Entrega 3), tarefas (Entrega 5) e plataforma (seção 1) definem quem é medido, em qual tarefa e com quais limites (seção 3).
2. **Metas são verificadas em dois momentos.** As qualitativas no walkthrough do protótipo em papel (Entrega 6). As quantitativas no teste com usuários (Entrega 14), sobre o protótipo da Entrega 11.
3. **Meta não atingida leva a revisão.** Se o problema é de interface, a equipe volta ao nível do projeto (modelo conceitual ou protótipo) e testa de novo. Se o problema é de requisito (perfil, tarefa ou meta errada), volta à análise.
4. **Dados novos também levam a revisão.** Após a análise dos dados da Entrega 7: revisar as hipóteses em `RASTREABILIDADE.md`, as personas P01 e P02 (Entrega 3), os cenários C01 e C02 (Entrega 4), as tarefas T01 e T02 (Entrega 5) e, nesta entrega, dispositivo, histórico e os valores de MU01 a MU06. Se H11 for refutada, MU04 e MU05 saem.
5. **Artefatos atualizados a cada iteração:** `RASTREABILIDADE.md` (hipóteses e registro de mudanças), personas, tarefas, metas e princípios. Correções de tela que não mudam esses artefatos são registradas só na entrega do protótipo.

## Referências

- BARBOSA, S. D. J.; SILVA, B. S. *Interação Humano-Computador*. Rio de Janeiro: Elsevier, 2010.
- NIELSEN, J. *Usability Engineering*. San Francisco: Morgan Kaufmann, 1993.
- SAURO, J. What Is A Good Task-Completion Rate? MeasuringU. <https://measuringu.com/task-completion/>
- SAURO, J. 10 Things To Know About The Single Ease Question (SEQ). MeasuringU. <https://measuringu.com/seq10/>

## Checklist

- [x] Capacidades e restrições têm impacto de IHC explicitado.
- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [x] Resultados/processamento simulados no protótipo foram explicitados.
- [x] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [x] Normas/princípios estão contextualizados, não apenas copiados.
- [x] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [x] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [x] Metas poderão ser verificadas nas Entregas 12 a 14.
