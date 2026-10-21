# Entrega 4 — Cenários de análise/problema

**Data:** 14/10/2002 
**Status:** 🟩 finalizada  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01 — Inferência de tópicos a partir do enunciado

**Autor(a):** Sebastian Citta - 24.123.068-9
**Persona(s) relacionada(s):** P01
**Necessidade relacionada:** R01
**Situação concreta da Entrega 1 relacionada:** H21
**Hipóteses ainda presentes:** H05, H06, H07, H08

## Cenário C02 — Ancoragem dos tópicos em materiais didáticos consolidados

**Autor(a):** Juan Manuel Citta - 24.123.022-6
**Persona(s) relacionada(s):** P02  
**Necessidade relacionada:** R03
**Situação concreta da Entrega 1 relacionada:** H11
**Hipóteses ainda presentes:** H10, 

### 1. Cenário inicial

C01 - Descobrir o que falta saber para resolver uma questão

Atores: Rafael (nome fictício), estudante de Ciência da Computação

Rafael é graduando em Ciência da Computação e treina programação competitiva sozinho, no notebook. Ele programa com segurança e resolve sem ajuda as questões mais fáceis do Codeforces, mas ainda não sabe identificar, pelo enunciado, qual técnica uma questão exige. Hoje ele abriu um problema novo, com o enunciado em uma aba e o editor de código em outra, e o leu várias vezes. Escreveu uma primeira tentativa e submeteu, mas o veredito foi Wrong Answer. Ele entende o veredito, mas isso não o ajuda a saber o que fazer.

Rafael já viu as palavras dp, greedy e constructive algorithms nas etiquetas de problemas. Algumas ele reconhece de disciplinas do curso, mas não consegue dizer qual delas se aplica à questão, nem o que precisaria estudar antes. Sem saber o que procurar, ele passa a tentar por eliminação: reescreve a solução com outra abordagem, submete de novo e erra de novo. A cada tentativa o tempo de treino diminui e a frustração aumenta. No meio disso, uma mensagem o interrompe, e ao voltar ele precisa reler o enunciado e o código para lembrar em que ponto estava.

Rafael não quer a solução pronta, porque o objetivo é evoluir no treino. O que ele quer é descobrir o que lhe falta saber para destravar a questão. Mas, do jeito que está, ele sai do treino sem saber se o obstáculo foi uma técnica que desconhece, um pré-requisito que não estudou ou apenas um detalhe da implementação.

C02 - Confiar no material antes de repassá-lo aos alunos

Atores: Helena (nome fictícia), professora de Ciência da Computação e, eventualmente, treinadora do time de maratona

Helena leciona em turmas grandes e, nos períodos de preparação para a competição, também treina o time de maratona da faculdade. Ela é especialista: lê o enunciado de uma questão e reconhece na hora a técnica que ela exige. O que lhe falta é tempo. Com poucas horas de aula e muitos alunos, não consegue atender individualmente quem trava, e o plano de treino da maratona acaba sendo montado às pressas.

Quando um aluno trava durante o treino, Helena costuma sugerir que ele consulte um dos modelos de IA disponíveis no mercado. Ela sabe que o aluno precisa de alguma ajuda, mas não tem como saber em quais fontes o modelo se baseia, nem se a explicação segue a mesma linha do material que ela já entregou à turma. Como tem o hábito de verificar as fontes antes de repassar qualquer conteúdo, isso a incomoda. Alguns alunos voltam com explicações que divergem do que foi ensinado, e ela gasta parte do pouco tempo de aula descobrindo de onde veio a divergência e desfazendo a confusão.

Helena não quer proibir os alunos de buscar apoio. O que ela quer é poder confiar no material antes de repassá-lo, porque a reputação dela e da instituição, assim como o resultado dos alunos, dependem disso. Do jeito que está, ela encerra o treino sem saber o que cada aluno estudou nem se o que estudou está correto.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

C01:
| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | **[Planejamento]** Como os alunos que treinam sozinhos tentam hoje descobrir o que estudar quando travam (editorial, tags, colegas, busca, LLM)? Quais estratégias conhecem e quando usam cada uma? | O cenário mostra só a tentativa por eliminação. Não se sabe se Rafael desconhece as outras estratégias ou se as conhece e elas falham. | Entrevista com integrantes do time; observação de uma sessão de treino. |
| Q2 | **[Evento]** O que leva o aluno a parar de tentar sozinho e buscar ajuda (número de submissões, tempo parado, cansaço)? | Define em que momento o sistema precisa estar disponível e o que Rafael já gastou até chegar a ele (H23). | Entrevista; histórico de submissões no Codeforces. |
| Q3 | **[Objetivo]** De que informações ou conhecimento o aluno precisa para distinguir se o obstáculo é técnica desconhecida, pré-requisito não estudado ou detalhe de implementação? | O cenário diz que Rafael sai sem saber o que o travou, mas não diz o que lhe permitiria saber. | Entrevista com o aluno e com um professor/treinador; análise de casos de questões em que travaram. |
| Q4 | **[Avaliação]** Como o aluno sabe que descobriu o que lhe faltava? É resolver a questão, entender o conceito ou ter um tópico para estudar? | Sem um critério de sucesso do objetivo, não há como avaliar se a solução funcionou. | Entrevista; teste com protótipo de baixa fidelidade. |
| Q5 | **[Verificação]** O aluno já recorre a LLMs quando trava em questões desse tipo, e confia no que recebe? | A persona usa LLMs no dia a dia (H19), mas o cenário não mostra isso. Pode ser a estratégia atual mais comum e a principal concorrente. | Questionário curto ou entrevista com o time. |


C02:
| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q6 | **[Planejamento]** Como Helena monta hoje o plano de treino e o material entregue (de onde vêm as questões e o conteúdo, em que formato, quanto tempo leva)? | O cenário diz que o plano sai “às pressas”, mas não como é feito. Sem isso não dá para saber onde o tempo se perde. | Entrevista com professores/treinadores. |
| Q7 | **[Ação]** Que critérios ela usa para considerar uma fonte confiável e que ações faz ao verificá-la? | O cenário afirma que ela verifica fontes (H25), mas não como nem com qual critério. | Entrevista; observação de uma preparação de aula. |
| Q8 | **[Ator]** Como Helena fica sabendo hoje que um aluno trouxe uma explicação divergente (ele conta, ela percebe em aula, nunca)? | Mostra se a dor é detectada na hora ou só depois, e quanto tempo de aula ela custa. | Entrevista com o professor e conversa com alunos. |
| Q9 | **[Ambiente]** Quanto tempo ela tem entre preparar o material e o treino, e quem mais participa (monitores, outros treinadores, coordenação)? | Define a pressão real de tempo e se existem outras pessoas que dependem do resultado ou poderiam ajudar na revisão. | Entrevista; levantamento do calendário de preparação. |
| Q10 | **[Verificação]** Helena permitiria que os alunos usassem apoio de IA se as fontes tivessem sido definidas ou aprovadas por ela? | Testa se o problema é o uso de IA em si ou a falta de controle sobre as fontes, o que muda o que significa “confiar”. | Entrevista. Validação com mais de um professor. |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

Rafael é graduando em Ciência da Computação e treina programação competitiva sozinho, no notebook. Ele programa com segurança e resolve sem ajuda as questões mais fáceis do Codeforces, mas ainda não sabe identificar, pelo enunciado, qual técnica uma questão exige. Hoje ele abriu um problema novo, com o enunciado em uma aba e o editor de código em outra, e o leu várias vezes. Escreveu uma primeira tentativa e submeteu, mas o veredito foi Wrong Answer. Ele entende o veredito, mas isso não o ajuda a saber o que fazer.

Rafael já viu as palavras dp, greedy e constructive algorithms nas etiquetas de problemas. Algumas ele reconhece de disciplinas do curso, mas não consegue dizer qual delas se aplica à questão, nem o que precisaria estudar antes. Quando trava, ele costuma tentar, nesta ordem: ver as etiquetas do problema, ler o editorial, perguntar a um colega do time por mensagem e, por último, colar o enunciado em um LLM. As etiquetas dão o nome, mas não dizem o que estudar, o editorial entrega a solução pronta, e o colega nem sempre está disponível[Q1]. Ele só desiste de tentar sozinho depois de umas três submissões erradas seguidas ou de cerca de 30 minutos sem progresso, o que vier primeiro[Q2]. Até lá, passa a tentar por eliminação: reescreve a solução com outra abordagem, submete de novo e erra de novo. A cada tentativa o tempo de treino diminui e a frustração aumenta. No meio disso, uma mensagem o interrompe, e ao voltar ele precisa reler o enunciado e o código para lembrar em que ponto estava.

Quando recorre ao LLM, Rafael costuma receber a solução inteira, que ele não quer, e não tem como saber se a explicação está correta, porque não domina o assunto[Q5].

Rafael não quer a solução pronta, porque o objetivo é evoluir no treino. O que ele quer é descobrir o que lhe falta saber para destravar a questão. Para isso, precisaria saber qual é o tópico provável, quais pré-requisitos ele exige e se o erro do seu código está na ideia ou no detalhe, por exemplo quando passa nos exemplos mas falha em casos de borda[Q3]. Ele considera que descobriu o que lhe faltava quando consegue dizer, com as próprias palavras, qual tópico estudar e por quê, mesmo antes de resolver a questão. Resolver o problema é a confirmação final[Q4]. Mas, do jeito que está, ele sai do treino sem saber se o obstáculo foi uma técnica que desconhece, um pré-requisito que não estudou ou apenas um detalhe da implementação.


C02 - Confiar no material antes de repassá-lo aos alunos

Atores: Helena (nome fictício), professora de Ciência da Computação e, eventualmente, treinadora do time de maratona

Helena leciona em turmas grandes e, nos períodos de preparação para a competição, também treina o time de maratona da faculdade. Ela é especialista: lê o enunciado de uma questão e reconhece na hora a técnica que ela exige. O que falta para ela é tempo. Com poucas horas de aula e muitos alunos, não consegue atender individualmente quem trava, e o plano de treino da maratona acaba sendo montado às pressas. Ela monta o plano a partir de listas de problemas de edições anteriores e de questões escolhidas em juízes online, reunidas em um documento compartilhado com o time. Isso consome algumas horas por semana que ela não tem[Q6]. Entre preparar o material e realizar o treino costumam passar poucos dias, nos intervalos entre as aulas. Um monitor veterano ajuda com a organização, e a coordenação do curso cobra resultado na competição[Q9].

Quando um aluno trava durante o treino, Helena costuma sugerir que ele consulte um dos modelos de IA disponíveis no mercado. Ela sabe que o aluno precisa de alguma ajuda, mas não tem como saber em quais fontes o modelo se baseia, nem se a explicação segue a mesma linha do material que ela já entregou à turma. Como tem o hábito de verificar as fontes antes de repassar qualquer conteúdo, isso a incomoda. Ela considera confiável uma fonte que já conhece ou que é referência reconhecida, como editoriais oficiais, livros-texto e material de outros treinadores. Ao verificar, confere por conta própria a solução e a técnica indicada[Q7]. Alguns alunos voltam com explicações que divergem do que foi ensinado. Ela só percebe a divergência no próprio treino, quando o aluno expõe a explicação e ela nota a diferença. Raramente o aluno avisa antes[Q8]. Então gasta parte do pouco tempo de aula descobrindo de onde veio a divergência e desfazendo a confusão.

Helena não quer proibir os alunos de buscar apoio. O incômodo dela não é a IA em si, e sim a falta de controle sobre as fontes. Ela aceitaria o uso se as fontes fossem definidas ou aprovadas por ela[Q10]. O que ela quer é poder confiar no material antes de repassá-lo, porque a reputação dela e da instituição, assim como o resultado dos alunos, dependem disso. Do jeito que está, ela encerra o treino sem saber o que cada aluno estudou nem se o que estudou está correto.

### 4. Elementos extraídos

C01:
| Elemento | Evidência no cenário |
| --- | ---- |
| Ator(es) | Rafael, graduando em Ciência da Computação que treina sozinho, sem tutor. Colega do time, consultado por mensagem quando está disponível [Q1]. |
| Objetivo(s) | Descobrir o que lhe falta saber (técnica desconhecida, pré-requisito não estudado ou detalhe de implementação) sem receber a solução pronta, para evoluir no treino. |
| Contexto | Treino individual no notebook, com enunciado e editor em abas separadas. Sofre interrupções por mensagens. Chega ao sistema já travado e frustrado, depois de cerca de 3 submissões erradas ou 30 minutos sem progresso [Q2]. |
| Recursos/informações | Enunciado, veredito do Codeforces (*Wrong Answer*), etiquetas (*dp*, *greedy*, *constructive algorithms*), editorial, colega do time, LLM e conhecimento de disciplinas já cursadas. |
| Ações | Ler o enunciado, escrever a solução, submeter, interpretar o veredito, consultar etiquetas, ler o editorial, perguntar ao colega, colar o enunciado em um LLM [Q1], reescrever com outra abordagem por eliminação e reler enunciado e código após cada interrupção. |
| Problemas/rupturas | Não identifica a técnica pelo enunciado. As etiquetas dão o nome mas não dizem o que estudar. O editorial entrega a solução pronta. O colega nem sempre está disponível. O LLM devolve a solução inteira e Rafael não consegue verificar se está correta [Q5]. Não distingue se o erro está na ideia ou no detalhe [Q3]. As interrupções o obrigam a reler tudo. |
| Consequências | Perda de tempo de treino, frustração crescente, tentativas repetidas sem aprendizado. Ele sai do treino sem saber qual foi o obstáculo, e a evolução fica comprometida. |
| Elemento | Evidência no cenário |

C02:
| Elemento | Evidência no cenário |
| ----- | ----- |
| Ator(es) | Helena, professora e eventual treinadora do time de maratona. Alunos do time, que consomem o material e consultam IA. Coordenação do curso, que cobra resultado [Q9]. |
| Objetivo(s) | Poder confiar no material antes de repassá-lo aos alunos, sem proibi-los de buscar apoio. |
| Contexto | Turmas grandes e poucas horas de aula. Preparação para a competição, com poucos dias entre preparar o material e treinar [Q9]. Pressão por reputação (dela e da instituição) e por resultado dos alunos. |
| Recursos/informações | Listas de edições anteriores, questões de juízes online, documento compartilhado com o time [Q6]. Fontes que ela considera confiáveis: editoriais oficiais, livros-texto e material de outros treinadores [Q7]. |
| Ações | Montar o plano de treino, entregar o material, sugerir que o aluno consulte uma IA ao travar, verificar fontes conferindo solução e técnica [Q7], notar divergências no treino [Q8], investigar a origem e desfazer a confusão. |
| Problemas/rupturas | Plano montado às pressas, com algumas horas semanais que ela não tem [Q6]. Falta de controle sobre as fontes da IA. Explicações que divergem do material entregue. A divergência só aparece no treino, quando o aluno a expõe [Q8]. Dificuldade de atender individualmente quem trava. |
| Consequências | Parte do pouco tempo de aula é gasta investigando divergências. Risco à reputação dela e da instituição e ao aprendizado/resultado dos alunos. Ela encerra o treino sem saber o que cada aluno estudou nem se está correto. |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

C01:
Tarefas que merecem análise

- Diagnosticar o tipo de obstáculo (técnica, pré-requisito ou implementação). É o núcleo do objetivo e hoje não tem estratégia que o atenda.
- Decidir quando parar de tentar sozinho e buscar ajuda, já que o ponto de chegada condiciona o estado do usuário (H23).
- Consultar as fontes disponíveis (etiquetas, editorial, colega, LLM), analisando o que cada uma entrega e onde falha.
- Retomar o trabalho depois de uma interrupção (H24).

Informações a coletar

- Se as estratégias descritas em Q1 e o gatilho de 3 submissões ou 30 minutos em Q2 se confirmam com integrantes do time, e se há outras estratégias que não apareceram.
- Como o aluno reconhece que descobriu o que faltava (Q4), para ter um critério de sucesso do objetivo.
- Com que frequência e com que resultado Rafael usa LLMs ao travar, e quanto confia neles (Q5).
- Que informações o aluno precisaria ter para distinguir os três tipos de obstáculo (Q3).
- Acessibilidade (Q3 da persona) continua sem investigação.

## Checklist

- [ X] Há um cenário completo por integrante.
- [ X] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ X] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ X] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [X ] Questões de refinamento acrescentam informação nova.
- [ X] O refinamento mostra claramente o que foi adicionado/alterado.
- [ X] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ X] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
