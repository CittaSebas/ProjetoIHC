# Entrega 4: Cenários de análise/problema

**Data:** 14/10/2026 
**Status:** `🟦 revisada após feedback`  
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

## Cenário C01: Inferência de tópicos a partir do enunciado

**Autor(a):** Sebastian Citta - 24.123.068-9
**Persona(s) relacionada(s):** P01
**Necessidade relacionada:** R01
**Situação concreta da Entrega 1 relacionada:** seção 4.5
**Hipóteses ainda presentes:** H05, H06, H07, H08, H17, H18, H19, H22, H23 e as lacunas Q02, Q06, Q08, Q16, Q17

## Cenário C02: Ancoragem dos tópicos em materiais didáticos consolidados

**Autor(a):** Juan Manuel Citta - 24.123.022-6
**Persona(s) relacionada(s):** P02  
**Necessidade relacionada:** R03
**Situação concreta da Entrega 1 relacionada:** H11
**Hipóteses ainda presentes:** H11, H24

> **C02 é um cenário exploratório.** Parte de uma proto-persona secundária (P02), construída sem nenhuma conversa com professores ou treinadores, e está ligado a H11, que continua aberta. Ele não orienta decisões de interface até H11 ser investigada. As decisões principais do projeto seguem o C01 e a persona primária P01.

### 1. Cenário inicial

C01 - Descobrir o que falta saber para resolver uma questão

Atores: Alfreda Marta (persona P01, Entrega 3), estudante de Ciência da Computação

Alfreda está no 3º semestre de Ciência da Computação e treina programação competitiva sozinha, no notebook, em casa. Ela programa com segurança e resolve sem ajuda as questões mais fáceis do Codeforces, mas ainda não sabe identificar, pelo enunciado, qual técnica uma questão exige. Hoje ela abriu um problema novo, com o enunciado em uma aba e o editor de código em outra, e o leu várias vezes. Escreveu uma primeira tentativa e submeteu, mas o veredito foi Wrong Answer. Ela entende o veredito, mas isso não a ajuda a saber o que fazer.

Alfreda já viu as palavras dp, greedy e constructive algorithms nas etiquetas de problemas. Algumas ela reconhece de disciplinas do curso, mas não consegue dizer qual delas se aplica à questão, nem o que precisaria estudar antes. Sem saber o que procurar, ela passa a tentar por eliminação: reescreve a solução com outra abordagem, submete de novo e erra de novo. A cada tentativa o tempo de treino diminui e a frustração aumenta. No meio disso, uma mensagem a interrompe, e ao voltar ela precisa reler o enunciado e o código para lembrar em que ponto estava.

Alfreda não quer a solução pronta, porque o objetivo é evoluir no treino. O que ela quer é descobrir o que lhe falta saber para destravar a questão. Mas, do jeito que está, ela sai do treino sem saber se o obstáculo foi uma técnica que desconhece, um pré-requisito que não estudou ou apenas um detalhe da implementação.

> **Hipóteses por trás dos detalhes do C01:** resolver sozinha as questões fáceis e não reconhecer a técnica pelo enunciado (H06, Q02); olhar as etiquetas e tentar por eliminação (H17); chegar à busca de ajuda já travada e com pressa (H22); ser interrompida durante o treino (H23); não querer a solução pronta (H07). Nenhum desses comportamentos foi observado ainda. A coleta da Entrega 7 vai confirmar ou corrigir cada um.

C02 - Confiar no material antes de repassá-lo aos alunos

Atores: José Carlos Trunchado (persona P02, Entrega 3), professor de Ciência da Computação e, eventualmente, treinador do time de maratona

José Carlos leciona em turmas grandes e, nos períodos de preparação para a competição, também treina o time de maratona da faculdade. Ele é especialista: lê o enunciado de uma questão e reconhece na hora a técnica que ela exige. O que lhe falta é tempo. Com poucas horas de aula e muitos alunos, não consegue atender individualmente quem trava, e o plano de treino da maratona acaba sendo montado às pressas.

Quando um aluno trava durante o treino, José Carlos costuma sugerir que ele consulte um dos modelos de IA disponíveis no mercado. Ele sabe que o aluno precisa de alguma ajuda, mas não tem como saber em quais fontes o modelo se baseia, nem se a explicação segue a mesma linha do material que ele já entregou à turma. Como tem o hábito de verificar as fontes antes de repassar qualquer conteúdo, isso o incomoda. Alguns alunos voltam com explicações que divergem do que foi ensinado, e ele gasta parte do pouco tempo de aula descobrindo de onde veio a divergência e desfazendo a confusão.

José Carlos não quer proibir os alunos de buscar apoio. O que ele quer é poder confiar no material antes de repassá-lo, porque a reputação dele e da instituição, assim como o resultado dos alunos, dependem disso. Do jeito que está, ele encerra o treino sem saber o que cada aluno estudou nem se o que estudou está correto.

> **Hipóteses por trás dos detalhes do C02:** usar a ferramenta para validar conteúdo (H11); conferir as fontes antes de repassar o material (H24); recomendar modelos de IA aos alunos, receber de volta explicações divergentes e ter a reputação ligada a esse material são suposições da equipe, sem conversa com nenhum professor. Nenhum desses comportamentos foi observado.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

C01:

Cada um dos sete elementos característicos (ambiente, atores, objetivos, planejamento, ações, eventos e avaliação) tem ao menos uma questão. Q5 é uma questão extra de verificação. Nenhuma questão foi respondida com dados ainda: a coluna "Status da resposta" diz o que a equipe tem hoje. Na coluna "Status da resposta", os IDs entre parênteses são hipóteses e lacunas da Entrega 1 (por exemplo, Q16 é "como o aluno percebe que travou"), e não questões deste refinamento. As questões deste refinamento são Q1 a Q10 e Q18 a Q23.

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta | Status da resposta |
|---|---|---|---|---|---|
| Q18 | Ambiente | Em que situações Alfreda treina (sozinha em casa, treino do time, competição) e quanta pressão de tempo existe em cada uma quando ela trava? | O cenário só mostra o treino em casa. A pressão de tempo muda o quanto ela pode esperar e ler quando trava, e o uso em competição ainda não foi decidido (Q08) | Entrevista; Entrega 7, investigação contextual (pergunta 1 do roteiro) | lacuna aberta (Q08, Q10) |
| Q19 | Atores | Quando Alfreda já estudou um tópico, ela reconhece num enunciado novo que ele se aplica? Ou conhecer o tópico e saber quando usá-lo são coisas diferentes para ela? | O cenário supõe que ela não reconhece a técnica porque não a estudou. Se ela também não reconhece tópicos que já estudou, o obstáculo é outro: saber quando aplicar, e não só o que estudar. A resposta pode ser "sim, reconhece", e isso também muda o cenário | Entrevista; Entrega 7, investigação contextual, observando se ela reconhece num enunciado um tópico que já cursou | lacuna aberta (Q02, Q06) |
| Q3 | Objetivos | De que informações ou conhecimento Alfreda precisa para distinguir se o obstáculo é técnica desconhecida, pré-requisito não estudado ou detalhe de implementação? | O cenário diz que ela sai sem saber o que a travou, mas não diz o que lhe permitiria saber | Entrevista com alunos e com um professor/treinador; análise de questões em que travaram | lacuna aberta (Q06) |
| Q1 | Planejamento | Que estratégias Alfreda conhece para descobrir o que estudar quando trava (etiquetas, editorial, colegas, busca, chatbot), e o que a faz escolher uma ou outra? | O cenário mostra só a tentativa por eliminação. Não se sabe se ela desconhece as outras estratégias ou se as conhece e elas falham | Entrevista; Entrega 7, questionário (perguntas 14 e 15) e investigação contextual (pergunta 7 do roteiro) | hipótese de trabalho (H17, H18, H19) |
| Q20 | Ações | O que Alfreda faz, passo a passo, depois de decidir buscar ajuda: o que abre, o que lê, o que copia e em que ordem? | O cenário lista as fontes que existem, mas não o que ela faz em cada uma. Só o comportamento observado mostra onde ela perde tempo | Observação; Entrega 7, investigação contextual (folha de anotação) | lacuna aberta (H17, Q06) |
| Q2 | Eventos | O que leva Alfreda a parar de tentar sozinha e buscar ajuda (número de submissões, tempo parado, cansaço)? | Define o estado em que ela chega à busca de ajuda e o que já gastou até lá (H22) | Entrega 7, questionário (perguntas 12 e 13) e investigação contextual (pergunta 6 do roteiro); histórico de submissões | lacuna aberta (Q16) |
| Q4 | Avaliação | Como Alfreda sabe que descobriu o que lhe faltava? É resolver a questão, entender o conceito ou ter um tópico para estudar? | Sem um critério de sucesso do objetivo, não há como avaliar se a solução funcionou | Entrega 7, questionário (pergunta 22) e investigação contextual (pergunta 10 do roteiro) | hipótese de trabalho (Q17) |
| Q5 | Verificação (extra) | Alfreda já recorre a chatbots quando trava em questões desse tipo, e confia no que recebe? | A persona usa LLMs no dia a dia (H19), mas o cenário inicial não mostra isso. Pode ser a estratégia atual mais comum e a principal concorrente | Entrega 7, questionário (perguntas 14, 17 e 18) | hipótese de trabalho (H06, H19) |


C02:

Cada um dos sete elementos característicos tem ao menos uma questão. Q10 é uma questão extra de verificação. **Nenhuma destas questões tem coleta prevista:** a Entrega 7 não inclui professores, porque P02 é secundária e depende de H11. Elas ficam registradas como lacuna ou hipótese até H11 ser investigada.

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta | Status da resposta |
|---|---|---|---|---|---|
| Q9 | Ambiente | Quanto tempo José Carlos tem entre preparar o material e o treino, e quem mais participa (monitores, outros treinadores, coordenação)? | Define a pressão real de tempo e se existem outras pessoas que dependem do resultado ou poderiam ajudar na revisão | Entrevista; levantamento do calendário de preparação | hipótese de trabalho, sem coleta prevista (H11) |
| Q8 | Atores | Como José Carlos fica sabendo hoje que um aluno trouxe uma explicação divergente (o aluno conta, ele percebe em aula, nunca)? | Mostra se a dor é percebida na hora ou só depois, e quanto tempo de aula ela custa | Entrevista com professores e conversa com alunos | hipótese de trabalho, sem coleta prevista (H11) |
| Q21 | Objetivos | O que José Carlos quer alcançar ao indicar material aos alunos: que resolvam a questão, que aprendam a técnica ou que sigam a mesma linha da aula? Esses objetivos entram em conflito? | O cenário diz que ele quer "confiar no material", mas não diz para quê. Isso define o que confiar significa para ele | Entrevista com professores e treinadores | lacuna aberta, sem coleta prevista (H11, H24) |
| Q6 | Planejamento | Como José Carlos monta hoje o plano de treino e o material entregue (de onde vêm as questões e o conteúdo, em que formato, quanto tempo leva)? | O cenário diz que o plano sai "às pressas", mas não como é feito. Sem isso não dá para saber onde o tempo se perde | Entrevista com professores e treinadores | lacuna aberta, sem coleta prevista (H11) |
| Q7 | Ações | Que critérios ele usa para considerar uma fonte confiável e o que faz para verificá-la? | O cenário afirma que ele verifica fontes, mas não como nem com qual critério | Entrevista; observação de uma preparação de aula | hipótese de trabalho, sem coleta prevista (H24) |
| Q22 | Eventos | Quando um aluno trava e o procura fora da aula, o que José Carlos faz? Com que frequência isso acontece? | O cenário diz que ele sugere IA quando o aluno trava, mas não diz em que momento o pedido chega nem com que frequência | Entrevista com professores e treinadores; conversa com alunos | lacuna aberta, sem coleta prevista (H11) |
| Q23 | Avaliação | Como José Carlos sabe se o material que indicou funcionou: o aluno resolveu, aprendeu a técnica, o desempenho do time melhorou? | Sem esse critério, não se sabe quando ele considera uma fonte boa o bastante | Entrevista com professores e treinadores | lacuna aberta, sem coleta prevista (H11) |
| Q10 | Verificação (extra) | José Carlos permitiria que os alunos usassem apoio de IA se as fontes tivessem sido definidas ou aprovadas por ele? | Testa se o problema é o uso de IA em si ou a falta de controle sobre as fontes, o que muda o que significa "confiar" | Entrevista com mais de um professor | hipótese de trabalho, sem coleta prevista (H11) |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

C01 - Descobrir o que falta saber para resolver uma questão

Atores: Alfreda Marta (persona P01, Entrega 3), estudante de Ciência da Computação

> Nenhuma questão foi respondida com dados ainda. O texto novo está marcado com `[NOVO, hipótese: ...]` e traz a resposta que a equipe supõe hoje. A coleta da Entrega 7 vai confirmar ou corrigir cada uma.

Alfreda está no 3º semestre de Ciência da Computação e treina programação competitiva sozinha, no notebook, em casa. Ela programa com segurança e resolve sem ajuda as questões mais fáceis do Codeforces, mas ainda não sabe identificar, pelo enunciado, qual técnica uma questão exige. **[NOVO, hipótese: nessas sessões em casa a pressão de tempo é moderada; o que pesa é a sessão curta, de uma ou duas horas. Nos treinos do time e em simulados a pressão é maior.]** [Q18] Hoje ela abriu um problema novo, com o enunciado em uma aba e o editor de código em outra, e o leu várias vezes. Escreveu uma primeira tentativa e submeteu, mas o veredito foi Wrong Answer. Ela entende o veredito, mas isso não a ajuda a saber o que fazer.

Alfreda já viu as palavras dp, greedy e constructive algorithms nas etiquetas de problemas. Algumas ela reconhece de disciplinas do curso, mas não consegue dizer qual delas se aplica à questão, nem o que precisaria estudar antes. **[NOVO, hipótese: mesmo um tópico que já estudou, como busca binária, ela nem sempre reconhece num enunciado novo. Conhecer o tópico não garante saber quando aplicá-lo.]** [Q19] **[NOVO, hipótese: quando trava, ela olha primeiro as etiquetas e depois pensa no editorial, em um colega do time ou em um chatbot. As etiquetas dão o nome, mas não dizem o que estudar; o editorial entrega a solução pronta; o colega nem sempre está disponível.]** [Q1] **[NOVO, hipótese: ela só desiste de tentar sozinha depois de várias submissões erradas seguidas ou de muito tempo sem progresso.]** [Q2] Até lá, passa a tentar por eliminação: reescreve a solução com outra abordagem, submete de novo e erra de novo. A cada tentativa o tempo de treino diminui e a frustração aumenta. No meio disso, uma mensagem a interrompe, e ao voltar ela precisa reler o enunciado e o código para lembrar em que ponto estava.

**[NOVO, hipótese: quando decide buscar ajuda, ela abre uma aba nova, procura a questão pelo nome ou copia o enunciado, lê o que encontra alternando entre essa aba e o enunciado, e volta ao editor para testar.]** [Q20] **[NOVO, hipótese: quando recorre a um chatbot, costuma receber a solução inteira, que ela não quer, e não tem como saber se a explicação está correta, porque não domina o assunto.]** [Q5]

Alfreda não quer a solução pronta, porque o objetivo é evoluir no treino. O que ela quer é descobrir o que lhe falta saber para destravar a questão. **[NOVO, hipótese: para isso, precisaria saber qual é o tópico provável, quais pré-requisitos ele exige e se o erro do seu código está na ideia ou no detalhe, por exemplo quando passa nos exemplos mas falha em casos de borda.]** [Q3] **[NOVO, hipótese: ela considera que descobriu o que lhe faltava quando consegue dizer, com as próprias palavras, qual tópico estudar e por quê, mesmo antes de resolver a questão. Resolver a questão é a confirmação final.]** [Q4] Mas, do jeito que está, ela sai do treino sem saber se o obstáculo foi uma técnica que desconhece, um pré-requisito que não estudou, um tópico que já conhecia mas não reconheceu, ou apenas um detalhe da implementação.


C02 - Confiar no material antes de repassá-lo aos alunos

Atores: José Carlos Trunchado (persona P02, Entrega 3), professor de Ciência da Computação e, eventualmente, treinador do time de maratona

> Nenhuma questão foi respondida com dados, e nenhuma tem coleta prevista enquanto H11 estiver aberta. O texto novo está marcado com `[NOVO, hipótese: ...]` e traz a resposta que a equipe supõe hoje.

José Carlos leciona em turmas grandes e, nos períodos de preparação para a competição, também treina o time de maratona da faculdade. Ele é especialista: lê o enunciado de uma questão e reconhece na hora a técnica que ela exige. O que lhe falta é tempo. Com poucas horas de aula e muitos alunos, não consegue atender individualmente quem trava, e o plano de treino da maratona acaba sendo montado às pressas. **[NOVO, hipótese: ele monta o plano a partir de listas de problemas de edições anteriores e de questões escolhidas em juízes online, reunidas em um documento compartilhado com o time, e isso toma um tempo que ele não tem.]** [Q6] **[NOVO, hipótese: entre preparar o material e realizar o treino passa pouco tempo, e pode haver outras pessoas envolvidas, como monitores ou a coordenação do curso.]** [Q9] **[NOVO, hipótese: ao indicar material, o que ele mais quer é que o aluno aprenda a técnica e siga a mesma linha da aula, e não só que resolva a questão.]** [Q21]

Quando um aluno trava durante o treino, José Carlos costuma sugerir que ele consulte um dos modelos de IA disponíveis no mercado. **[NOVO, hipótese: muitas vezes o pedido chega fora da aula, por mensagem, num momento em que ele não tem tempo de responder com calma.]** [Q22] Ele sabe que o aluno precisa de alguma ajuda, mas não tem como saber em quais fontes o modelo se baseia, nem se a explicação segue a mesma linha do material que ele já entregou à turma. Como tem o hábito de verificar as fontes antes de repassar qualquer conteúdo, isso o incomoda. **[NOVO, hipótese: ele considera confiável uma fonte que já conhece ou que é referência reconhecida, como editoriais oficiais e livros-texto, e ao verificar confere por conta própria a solução e a técnica indicada.]** [Q7] Alguns alunos voltam com explicações que divergem do que foi ensinado. **[NOVO, hipótese: ele só percebe a divergência no próprio treino, quando o aluno expõe a explicação.]** [Q8] Então gasta parte do pouco tempo de aula descobrindo de onde veio a divergência e desfazendo a confusão.

José Carlos não quer proibir os alunos de buscar apoio. **[NOVO, hipótese: o incômodo dele não é a IA em si, e sim a falta de controle sobre as fontes; ele aceitaria o uso se as fontes fossem conhecidas ou aprovadas por ele.]** [Q10] O que ele quer é poder confiar no material antes de repassá-lo, porque a reputação dele e da instituição, assim como o resultado dos alunos, dependem disso. **[NOVO, hipótese: ele considera que um material funcionou quando o aluno consegue explicar a técnica e aplicá-la em outra questão, e não só quando resolve aquela.]** [Q23] Do jeito que está, ele encerra o treino sem saber o que cada aluno estudou nem se o que estudou está correto.

### 4. Elementos extraídos

C01:
| Elemento | Evidência no cenário |
| --- | ---- |
| Ator(es) | Alfreda Marta (P01), aluna do 3º semestre que treina sozinha, sem tutor. Colega do time, consultado quando está disponível [Q1, hipótese]. |
| Objetivo(s) | Descobrir o que lhe falta saber (técnica desconhecida, pré-requisito não estudado, tópico que não reconheceu ou detalhe de implementação) sem receber a solução pronta, para evoluir no treino. |
| Contexto | Treino individual em casa, no notebook, com enunciado e editor em abas separadas; pressão de tempo moderada em casa e maior nos treinos do time [Q18, hipótese]. Sofre interrupções por mensagens. Chega à busca de ajuda já travada e frustrada, depois de várias submissões erradas ou muito tempo sem progresso [Q2, hipótese]. |
| Recursos/informações | Enunciado, veredito do Codeforces (*Wrong Answer*), etiquetas (*dp*, *greedy*, *constructive algorithms*), editorial, colega do time, chatbot e conhecimento de disciplinas já cursadas. |
| Ações | Ler o enunciado, escrever a solução, submeter, interpretar o veredito, consultar etiquetas, pensar em editorial, colega ou chatbot [Q1, hipótese], abrir uma aba nova, copiar o enunciado e alternar entre a resposta e o enunciado [Q20, hipótese], reescrever por eliminação e reler enunciado e código após cada interrupção. |
| Problemas/rupturas | Não identifica a técnica pelo enunciado, às vezes nem a de um tópico já estudado [Q19, hipótese]. As etiquetas dão o nome mas não dizem o que estudar. O editorial entrega a solução pronta. O colega nem sempre está disponível. O chatbot devolve a solução inteira e ela não consegue verificar se está correta [Q5, hipótese]. Não distingue se o erro está na ideia ou no detalhe [Q3, hipótese]. As interrupções a obrigam a reler tudo. |
| Consequências | Perda de tempo de treino, frustração crescente, tentativas repetidas sem aprendizado. Ela sai do treino sem saber qual foi o obstáculo, e a evolução fica comprometida. |

C02:
| Elemento | Evidência no cenário |
| ----- | ----- |
| Ator(es) | José Carlos Trunchado (P02), professor e eventual treinador do time de maratona. Alunos do time, que consomem o material e consultam IA. Possivelmente monitores ou a coordenação do curso [Q9, hipótese]. |
| Objetivo(s) | Poder confiar no material antes de repassá-lo aos alunos, sem proibi-los de buscar apoio; que o aluno aprenda a técnica na mesma linha da aula [Q21, hipótese]. |
| Contexto | Turmas grandes e poucas horas de aula. Preparação para a competição, com pouco tempo entre preparar o material e treinar [Q9, hipótese]. Pedidos de ajuda que chegam fora da aula [Q22, hipótese]. Pressão por reputação (dele e da instituição) e por resultado dos alunos. |
| Recursos/informações | Listas de edições anteriores, questões de juízes online, documento compartilhado com o time [Q6, hipótese]. Fontes que ele considera confiáveis: editoriais oficiais e livros-texto [Q7, hipótese]. |
| Ações | Montar o plano de treino, entregar o material, sugerir que o aluno consulte uma IA ao travar, verificar fontes conferindo solução e técnica [Q7, hipótese], notar divergências no treino [Q8, hipótese], investigar a origem e desfazer a confusão. |
| Problemas/rupturas | Plano montado às pressas, com um tempo que ele não tem [Q6, hipótese]. Falta de controle sobre as fontes da IA. Explicações que divergem do material entregue. A divergência só aparece no treino, quando o aluno a expõe [Q8, hipótese]. Dificuldade de atender individualmente quem trava. |
| Consequências | Parte do pouco tempo de aula é gasta investigando divergências. Risco à reputação dele e da instituição e ao aprendizado dos alunos. Ele encerra o treino sem saber o que cada aluno estudou nem se está correto, e sem um critério claro de que o material funcionou [Q23, hipótese]. |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

C01:
Tarefas que merecem análise

- Diagnosticar o tipo de obstáculo (técnica desconhecida, pré-requisito, tópico conhecido mas não reconhecido, ou implementação). É o núcleo do objetivo e hoje não tem estratégia que o atenda.
- Reconhecer, num enunciado novo, um tópico que já estudou (Q19).
- Decidir quando parar de tentar sozinha e buscar ajuda, já que esse momento define o estado em que ela chega (H22).
- Consultar as fontes disponíveis (etiquetas, editorial, colega, chatbot), analisando o que cada uma entrega e onde falha.
- Retomar o trabalho depois de uma interrupção.

Informações a coletar (todas previstas na Entrega 7)

- Quais estratégias os alunos usam e como escolhem entre elas (Q1), e o que os faz parar de tentar sozinhos (Q2). A equipe não tem números para isso: o momento de parar fica em aberto até a coleta.
- Em que situações treinam e com que pressão de tempo (Q18).
- Se reconhecem num enunciado um tópico que já estudaram (Q19). Esta observação ainda precisa entrar no roteiro da investigação contextual da Entrega 7.
- O que fazem, passo a passo, ao buscar ajuda (Q20).
- Como reconhecem que descobriram o que faltava (Q4), para ter um critério de sucesso do objetivo.
- Com que frequência e com que resultado usam chatbots ao travar, e quanto confiam neles (Q5).
- Que informações precisariam ter para distinguir os tipos de obstáculo (Q3).
- Acessibilidade (Q03 da Entrega 1) continua sem investigação.

C02:
Tarefas que merecem análise

- Verificar a fonte de um conteúdo antes de repassá-lo aos alunos (Q7). É a tarefa que liga P02 ao recorte, e só merece modelagem detalhada se H11 for sustentada.
- Montar o material de treino a partir de fontes que ele conhece (Q6).

Informações a coletar (sem coleta prevista: dependem de investigar H11)

- Se professores e treinadores usariam uma ferramenta assim (H11) e se conferir a fonte é de fato responsabilidade deles (H24).
- O que querem alcançar ao indicar material (Q21) e como sabem que funcionou (Q23).
- Como e quando ficam sabendo das dúvidas e das explicações divergentes dos alunos (Q8, Q22).
- Se aceitariam apoio de IA com fontes conhecidas ou aprovadas (Q10).
- Se a equipe decidir investigar H11, estas perguntas viram um roteiro de entrevista curta com um ou dois professores, a incluir na Entrega 7.

## Checklist

- [x] Há um cenário completo por integrante.
- [x] Cada cenário tem título, ator, objetivo, contexto e problema.
- [x] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [x] O texto descreve a situação atual, sem antecipar a solução.
- [x] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [x] Questões de refinamento acrescentam informação nova.
- [x] O refinamento mostra claramente o que foi adicionado/alterado.
- [x] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [x] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
