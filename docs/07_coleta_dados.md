# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 28/10/2026  
**Status:** 🟨 em andamento

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

Antes de decidir “que dados coletar”, retome os itens `[H]` e `[?]` da Entrega 1 e o registro de hipóteses em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md). A coleta deve responder perguntas reais do projeto, e não apenas produzir um formulário porque a técnica foi solicitada.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| Q06 | Quais informações o aluno interpreta, hoje, para decidir o que estudar quando trava? | Nenhuma | O que a interface precisa comunicar | alta |
| Q16 | Como e quando o aluno percebe que travou por falta de conteúdo? | Nenhuma; o "três submissões ou 30 minutos" do cenário C01 (Entrega 4) é estimativa da equipe | Ponto de início do cenário e da tarefa T01 | alta |
| H17, H18, H19 | Ao travar, o aluno recorre às tags, a editoriais/fóruns ou a um chatbot | Nenhuma; a ordem descrita no cenário C01 (Entrega 4) é estimativa da equipe | Quem é o concorrente real; cenário C01 | alta |
| H07 | O aluno quer destravar sem receber a solução pronta | Nenhuma | Delimitação do recorte: não entregar a solução | alta |
| H06 | O aluno não tem repertório para julgar se a orientação recebida está correta | Nenhuma | Explicabilidade e sinalização de incerteza (F05) | alta |
| H05 | A linguagem precisa ser compreensível para quem tem pouco domínio; os termos chegam em inglês | Entrega 2: Codeforces e ChatGPT usam estratégias opostas; nada sobre o aluno | Rótulos, idioma e glossário | alta |
| Q02 | O que significa concretamente "aluno iniciante"? | Nenhuma (P01 é proto-persona) | Persona P01 e nível de explicação | alta |
| H08, Q04 | Travar e buscar ajuda é frequente | Nenhuma | Prioridade do fluxo T01 | alta |
| H21, Q09 | O aluno treina e consulta em notebook/desktop | Nenhuma | Viabilidade do resultado em grafo (H15) e adaptação de telas para uso em dispositivo móvel | alta |
| Q12 | O aluno precisa recuperar o que consultou antes? | Nenhuma | Histórico entra ou não no escopo | alta |
| Q03 | Existe necessidade de acessibilidade nesse público? | Nenhuma | Requisitos de acessibilidade (Entrega 8) | alta |
| H20, Q05 | O erro mais relevante é estudar tópico sem relação com a questão; qual a consequência | [F] o modelo erra (F1 do núcleo de 0,82); consequência sem dado | Severidade (Entrega 13) | média |
| Q17 | Como o aluno decide que estudou o suficiente para voltar à questão? | Nenhuma | O que o resultado comunica sobre suficiência | média |

## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — Sebastian Citta

**Autor(a):** Sebastian Citta — 24.123.068-9

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Tempo de prática, faixa de rating no Codeforces e semestre | Q02 | Definir concretamente quem é o "iniciante" | Nível de explicação e linguagem da interface |
| Familiaridade com os termos das tags (`dp`, `greedy`...) e idioma preferido para estudar | H05 | O modelo devolve tópicos em inglês | Rótulos, idioma e glossário |
| Dispositivo em que resolve as questões e onde consulta ajuda | H21, Q09 | Um grafo legível em notebook pode ser impraticável em celular | Formato do resultado (H15) |
| Com que frequência trava a ponto de buscar ajuda | H08, Q04 | A prioridade de T01 pressupõe que isso é frequente | Prioridade de protótipo e teste |
| O que faz ao travar e o que faz primeiro | H17, H18, H19 | Definir o concorrente real | Cenário C01 |
| Que tipo de ajuda prefere receber | H07 | Se o aluno quiser a solução, o recorte muda | Delimitação do recorte |
| Se e como verifica uma explicação recebida | H06 | Base para explicabilidade | F05 |
| Em quantas sessões estuda um assunto e se volta ao material | Q12 | O histórico nunca foi investigado pela necessidade do aluno | Histórico no escopo |
| Recursos de acessibilidade que usa | Q03 | Nunca investigado | Requisitos da Entrega 8 |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Alunos de Ciência da Computação da FEI | 18 anos ou mais; tentou resolver ao menos uma questão de programação competitiva nos últimos 6 meses | P01 |
| Integrantes do time de maratona da FEI | Mesmos critérios | Mais experientes que P01; servem de contraste para definir "iniciante" (Q02) |

Professores e treinadores (P02) não participam desta coleta, porque o tutor não influencia decisões de interface enquanto H11 estiver aberta (Entrega 1, 2.2). A amostra é de conveniência, de uma única instituição.

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

- **Voluntariedade:** os participantes são colegas de curso e de time, o que pode gerar pressão para responder. O convite é feito uma única vez nos grupos.
- **Consentimento:** a primeira seção do formulário explica objetivo, duração e uso dos dados; sem o aceite, o formulário é encerrado.
- **Minimização:** não são coletados nome, e-mail nem RA. Rating e tempo de prática são pedidos em faixas.
- **Privacidade e riscos:** Declarar uso de chatbot pode ser lido como "cola"; as perguntas tratam apenas de treino, e nenhuma resposta é repassada a professores ou ao time.
- **Gravação:** não se aplica.
- **Anonimização:** o formulário não coleta e-mail nem exige login. O contato de quem quiser participar da segunda etapa (I02) fica em um formulário separado. Como as respostas são anônimas, não é possível apagar uma resposta depois do envio, e isso é informado no termo.
- **Armazenamento e descarte:** respostas no Google Forms, com acesso apenas dos dois integrantes; a coluna de data e hora é apagada após a limpeza; tudo é excluído ao fim do semestre 2026/2.

### A02 — Juan Manuel Citta

**Autor(a):** Juan Manuel Citta — 24.123.022-6

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Sinais que o aluno olha na questão (enunciado, tags, rating, veredito) e o que conclui de cada um | Q06 | É a principal lacuna do projeto | O que a interface precisa comunicar |
| Momento em que trava e o que o leva a buscar ajuda (tempo, nº de submissões) | Q16 | Só aparece observando o treino | Ponto de início do cenário e da tarefa T01 |
| Fontes consultadas, na ordem em que o aluno as abre | H17, H18, H19 | Comparar o que o aluno faz com o que declara no questionário | Cenário C01 |
| Como avalia se o que recebeu está certo | H06 | Sondar H06 sem mostrar a ferramenta | F05 |
| Vocabulário que usa para dizer o que não sabe | H05 | O questionário mede reconhecimento de termos, não uso | Rótulos e linguagem do resultado |
| Organização da tela e interrupções durante o treino | H21, H23 | Ver onde a consulta "cabe" no espaço de trabalho | Layout e retomada |
| Como decide que estudou o suficiente para voltar à questão | Q17 | Critério de sucesso do objetivo A01 | O que o resultado comunica |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Alunos de Ciência da Computação da FEI ou do time de maratona da FEI | 18 anos ou mais; treina em juiz online; aceita uma sessão presencial de até 90 minutos no próprio computador. Prioridade para quem pratica há menos de 1 ano. De 3 a 5 sessões | P01 |

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

- **Voluntariedade:** convite individual, sem insistência; o participante pode pausar ou encerrar a sessão a qualquer momento, sem justificativa.
- **Consentimento:** termo impresso em duas vias, lido junto com o participante e assinado antes do início.
- **Minimização:** só se anota o que se refere ao treino. Não se anota conteúdo de mensagens ou notificações (apenas que houve interrupção), nem o código, o usuário do Codeforces ou outras abas.
- **Privacidade e riscos:** a sessão acontece onde o aluno costuma treinar; se for em casa, ele pode optar por levar o notebook a um laboratório da FEI. Ser observado travando por um colega pode constranger; por isso o investigador explica que o objetivo é entender o processo, e não avaliar o participante, e nada sobre o desempenho é repassado ao time ou ao treinador.
- **Gravação:** não há gravação de áudio, vídeo ou tela, nem fotos. O registro é feito só com anotações.
- **Anonimização:** a folha de anotação usa um código (IC-01, IC-02...). A lista que liga nome e código fica separada e é destruída no início da análise; até lá, o participante pode pedir o descarte dos seus dados.
- **Armazenamento e descarte:** as anotações são transcritas em até 24 horas, sem dados que identifiquem o participante, e o papel é destruído. Os termos assinados são guardados à parte até o fim do semestre 2026/2 e depois destruídos.

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Questionário

**Autor(a):** Sebastian Citta — 24.123.068-9  
**Técnica:** questionário  
**Objetivo:** levantar o perfil de quem pratica programação competitiva, a frequência com que trava, o que faz nesse momento, que ajuda espera, como verifica o que recebe e como estuda e retoma um assunto.  
**Público:** alunos de 18 anos ou mais, de Ciência da Computação da FEI ou do time de maratona da FEI.

#### Procedimento padronizado de aplicação

1. Montar o formulário no Google Forms com as perguntas abaixo, sem coletar e-mails e sem exigir login. Fazer um piloto com 2 pessoas de fora da equipe para medir o tempo e corrigir perguntas ambíguas, e descartar essas respostas.
2. Divulgar o link uma vez nos grupos do curso e do time, com um texto curto que diz objetivo, duração (10 a 15 minutos), anonimato e que a participação é opcional. A primeira seção do formulário repete essas informações e pede o aceite.
3. Deixar o formulário aberto por 2 semanas, com um lembrete após 1 semana. A equipe não esclarece perguntas individualmente, para não induzir respostas.
4. Fechar o formulário e agradecer nos mesmos grupos. Na tela final, oferecer o link do formulário de contato separado para quem quiser participar do I02.
5. Exportar as respostas para uma planilha com acesso apenas dos dois integrantes, apagar a coluna de data e hora e excluir tudo ao fim do semestre 2026/2.

#### Instrumento

Cole aqui o questionário/roteiro completo ou forneça link **mais uma cópia textual no repositório**.

**Link:** a inserir após a criação no Google Forms.

**Abertura:** "Somos Juan Manuel Citta e Sebastian Citta, alunos de Ciência da Computação da FEI. Este questionário faz parte da disciplina de Interação Humano-Computador e quer entender como estudantes treinam programação competitiva e o que fazem quando travam numa questão. Não há resposta certa: estudamos o processo, não a sua capacidade. Leva de 10 a 15 minutos. Não pedimos nome, e-mail, RA nem usuário do Codeforces. Você pode parar a qualquer momento; como as respostas são anônimas, depois do envio não é possível apagar uma resposta específica. Os dados serão usados só nesta disciplina e excluídos ao fim de 2026/2."

0. Li as informações acima e: ( ) Concordo e quero participar ( ) Não quero participar *(encerra)*
1. Você tem 18 anos ou mais? ( ) Sim ( ) Não *(encerra)*
2. Nos últimos 6 meses, você tentou resolver alguma questão de programação competitiva? ( ) Sim ( ) Não *(encerra)*
3. Em que semestre você está? ( ) 1º–2º ( ) 3º–4º ( ) 5º–6º ( ) 7º–8º ( ) Já me formei ( ) Outro
4. Há quanto tempo pratica programação competitiva? ( ) Menos de 3 meses ( ) 3 a 6 meses ( ) 6 meses a 1 ano ( ) 1 a 2 anos ( ) Mais de 2 anos
5. Qual é o seu rating no Codeforces? ( ) Não tenho conta ( ) Tenho conta, sem rating ( ) Abaixo de 1200 ( ) 1200–1399 ( ) 1400–1599 ( ) 1600 ou mais ( ) Prefiro não informar
6. Para cada termo, marque o que melhor descreve você (*Nunca vi / Já vi, mas não sei o que é / Sei o que é, mas não sei quando usar / Sei quando usar*): `implementation`, `greedy`, `dp`, `binary search`, `two pointers`, `constructive algorithms`, `dfs and similar`
7. *(opcional)* Com as suas palavras, o que significa `dp`? Se não souber, escreva "não sei".
8. Em que idioma prefere estudar um assunto novo? ( ) Português ( ) Inglês ( ) Tanto faz
9. Em qual dispositivo você resolve as questões? [ ] Notebook [ ] Desktop [ ] Tablet [ ] Celular
10. Quando precisa consultar algo durante o treino, onde consulta? [ ] Outra aba ou janela do mesmo computador [ ] Segundo monitor [ ] Celular [ ] Material impresso
11. Nas últimas 4 semanas, quantas vezes você travou numa questão a ponto de procurar ajuda? ( ) Nenhuma ( ) 1–2 ( ) 3–5 ( ) 6 ou mais ( ) Não treinei nesse período
12. O que costuma fazer você parar de tentar sozinho(a)? [ ] Várias submissões erradas [ ] Muito tempo sem progresso [ ] Não saber por onde começar [ ] Passar nos exemplos e falhar em outro teste [ ] Cansaço ou falta de tempo [ ] Outro
13. Quanto tempo tenta sozinho(a) antes de procurar ajuda? ( ) Menos de 15 min ( ) 15–30 min ( ) 30–60 min ( ) Mais de 1 h ( ) Varia muito
14. Nas últimas 4 semanas, quando travou, o que você fez? [ ] Olhei as tags [ ] Li o editorial [ ] Li comentários ou blogs [ ] Perguntei a colega ou ao time [ ] Perguntei a treinador ou professor [ ] Perguntei a um chatbot de IA [ ] Pesquisei em buscador ou vídeo [ ] Consultei livro ou apostila [ ] Pulei a questão [ ] Outro
15. Qual dessas costuma ser a primeira coisa que você faz? (mesmas opções da 14, escolha única)
16. Quando trava, que ajuda você mais gostaria de receber? ( ) Uma dica pequena, sem revelar a solução ( ) Saber qual técnica a questão exige ( ) Saber o que estudar antes de tentar de novo ( ) A ideia da solução ( ) O código da solução ( ) Outro
17. "Quando um chatbot me explica uma questão, consigo perceber se a explicação está errada." (1 = discordo totalmente … 5 = concordo totalmente)
18. Quando recebe uma explicação, você verifica se está correta? Como? [ ] Testo no meu código [ ] Comparo com outra fonte [ ] Pergunto a alguém [ ] Verifico se a fonte é confiável [ ] Não costumo verificar
19. Já estudou um assunto e depois descobriu que ele não tinha relação com a questão? ( ) Sim, mais de uma vez ( ) Sim, uma vez ( ) Não ( ) Não sei
20. Quando precisa aprender um assunto novo por causa de uma questão, por quanto tempo estuda? ( ) Só na mesma sessão ( ) Em 2 ou 3 sessões ( ) Uma semana ou mais ( ) Não estudo, só tento resolver a questão
21. Você volta a materiais que já consultou? Como os encontra? [ ] Favoritos [ ] Histórico do navegador ou do chatbot [ ] Anotações [ ] Procuro de novo [ ] Não costumo voltar
22. *(opcional)* Como você decide que já estudou o suficiente para tentar a questão de novo?
23. *(opcional)* Você usa algum destes recursos ao estudar ou programar? [ ] Leitor de tela [ ] Zoom alto [ ] Alto contraste por necessidade visual [ ] Navegação só por teclado [ ] Nenhum [ ] Prefiro não responder

**Encerramento:** "Obrigado! Se quiser participar de uma sessão presencial em que acompanhamos seu treino, deixe seu contato neste outro formulário (separado, para manter suas respostas anônimas): link a inserir."

#### Como os dados serão analisados

Distribuição das respostas fechadas, em contagens, separando iniciantes dos demais a partir das perguntas 4 e 5. A escala da pergunta 17 é resumida pela mediana. As respostas abertas (7 e 22) passam por codificação temática, feita pelos dois integrantes de forma independente e depois comparada. Cada resultado é confrontado com a hipótese correspondente da tabela inicial.

### Instrumento I02 — Investigação contextual

**Autor(a):** Juan Manuel Citta — 24.123.022-6  
**Técnica:** investigação contextual (observação no ambiente do aluno com *think-aloud* e perguntas no modelo mestre–aprendiz)  
**Objetivo:** observar, no treino real, o momento em que o aluno trava: o que ele olha, o que conclui, quando decide buscar ajuda, a que fontes recorre e como avalia o que recebe.  
**Público:** alunos de 18 anos ou mais, de Ciência da Computação da FEI ou do time de maratona da FEI, que treinam em juiz online.

#### Procedimento padronizado de aplicação

1. Recrutar pelo formulário de contato do I01 e por convite direto. Combinar dia, horário e o local onde o aluno costuma treinar (ou um laboratório da FEI, se ele preferir). Levar o termo em duas vias, o roteiro e a folha de anotação. Fazer uma sessão-piloto com uma pessoa de fora da equipe.
2. Explicar o objetivo ("entender como você treina e o que faz quando uma questão fica difícil"), que o aluno é quem ensina e o investigador aprende, que não haverá ajuda com a questão nem gravação, e que ele pode parar quando quiser. Ler e assinar o termo.
3. O aluno escolhe e resolve questões normalmente, pensando em voz alta, por até 60 minutos. O investigador anota e faz as perguntas do roteiro só nas pausas, sem ajudar, sem sugerir fontes e sem comentar se algo está certo. Se o aluno não travar em cerca de 40 minutos, pedir que mostre a última questão em que travou e o que fez naquela vez. Ao final, o investigador resume o que entendeu do episódio e o aluno corrige.
4. Fazer as perguntas finais, agradecer e informar até quando o participante pode pedir o descarte dos dados.
5. Em até 24 horas, transcrever as anotações com o código da sessão, sem dados que identifiquem o participante, e destruir o papel. Guardar os termos à parte até o fim de 2026/2.

#### Instrumento

Cole aqui o questionário/roteiro completo ou forneça link **mais uma cópia textual no repositório**.

**Termo de consentimento:** "Você está sendo convidado(a) a participar de uma sessão em que acompanharemos seu treino de programação competitiva, para entender como estudantes treinam e o que fazem quando uma questão fica difícil. Estamos estudando o processo, não a sua capacidade. Você treinará normalmente no seu computador, por até 1h30, pensando em voz alta, e o pesquisador fará algumas perguntas nas pausas. Não haverá gravação de áudio, vídeo ou tela, nem fotos: apenas anotações identificadas por um código. De mensagens ou notificações, anotaremos só que ocorreram. Nada sobre o seu desempenho será repassado ao time ou a professores. A participação é voluntária, pode ser interrompida a qualquer momento e, até o início da análise, você pode pedir o descarte das suas anotações. Os dados serão usados só na disciplina de Interação Humano-Computador e descartados ao fim de 2026/2. Responsáveis: Juan Manuel Citta e Sebastian Citta."
Participante: ____________ Assinatura: ____________ Data: ___/___/2026

**Roteiro**

*Antes de começar*
1. Como é uma sessão de treino típica sua?
2. Como você escolhe a próxima questão?

*Durante o treino (somente quando o evento ocorrer)*

3. Ao ler o enunciado: "O que você está procurando no enunciado agora?"
4. Ao olhar tags, rating ou veredito: "O que isso te diz?"
5. Em uma pausa longa: "O que está passando pela sua cabeça?"
6. Ao decidir buscar ajuda: "O que fez você decidir procurar ajuda agora? O que acha que está faltando?"
7. Ao abrir uma fonte: "Por que essa primeiro? O que espera encontrar?"
8. Depois de usar a fonte: "Isso te ajudou? Como você sabe que está certo?"
9. Ao voltar de uma interrupção: "O que você precisou fazer para voltar de onde estava?"
10. Ao estudar um material: "Como vai decidir que já pode voltar à questão?"

*Perguntas finais*

11. Quando estuda um assunto por causa de uma questão, você volta a ele em outros dias? Como encontra de novo?
12. O que você considera uma ajuda boa quando trava? E o que estraga a questão para você?

**Folha de anotação**

Código: IC-__ · Data: __/__/2026 · Local: ______ · Tempo de prática / faixa de rating: ______ · Questão escolhida (plataforma, identificador, rating): ______

| Horário | O que o aluno fez | O que olhou/consultou | O que disse | Pergunta → resposta |
|---|---|---|---|---|
| | | | | |

#### Como os dados serão analisados

Para cada sessão, uma linha do tempo do episódio de travamento (gatilho, sinais consultados, fontes na ordem, avaliação do que recebeu, desfecho). Entre sessões, agrupamento das anotações em diagrama de afinidade, feito pelos dois integrantes. Os resultados são comparados com o que os alunos declararam no I01, para identificar diferenças entre o que dizem e o que fazem.

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

O questionário (I01) reduz as lacunas sobre quem é o aluno e com que frequência as situações ocorrem: perfil do iniciante, frequência de travar, ferramentas, dispositivo, tipo de ajuda desejada e hábito de retomar materiais. A investigação contextual (I02) reduz a lacuna sobre o que o aluno faz no momento em que trava, que o questionário não alcança, e permite comparar o que é declarado com o que é feito.


## Checklist

- [ ] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [ ] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [ ] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [ ] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [ ] Parte A identifica dados e perfis de coleta de forma específica.
- [ ] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [ ] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [ ] Perguntas evitam indução e coletam apenas dados necessários.
- [ ] Está claro como os dados serão analisados e usados no design.