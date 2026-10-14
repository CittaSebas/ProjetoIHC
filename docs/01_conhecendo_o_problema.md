# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 13/08/2026  
**Status:** 🟦 revisada após feedback  
**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Sebastian Citta | 24.123.068-9 | @CittaSebas |
| Juan Manuel Citta | 24.123.022-6 | @JuanCitta |

## 0.2 Título atual do TCC

Geração Automática de Trilhas de Estudo para Programação Competitiva

## 0.3 Orientador(a)

Charles Henrique Porto Ferreira

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [X] sistema/aplicação interativa;
- [ ] algoritmo;
- [X] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: Não se aplica.

**Descrição:** O objetivo do trabalho é o desenvolvimento de uma ferramenta para a geração de trilhas de estudos focada em Programação Competitiva. O usuário deve poder enviar uma pergunta e com base nas informações entregues uma LLM deve gerar um grafo baseado em livros didáticos para aprender a resolver dito problema. 

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [X] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** Está previsto a criação de uma interface WEB para o uso da ferramenta.

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Desenvolvimento de uma ferramenta para a geração de trilhas de estudos focada em Programação Competitiva.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

[F] Estudantes iniciantes de programação competitiva enfrentam um abismo entre a teoria estudada e a prática exigida pelas questões. Ribeiro e Guerreiro (2008) mostram que introduzir estudantes de computação a uma prática semelhante à programação competitiva aumenta significativamente a quantidade de programas escritos e o interesse por problemas de programação, mas registram que esse abismo se manifesta quando o estudante não domina o assunto tratado na questão. *Fonte:* RIBEIRO, P.; GUERREIRO, P. **Early introduction of competitive programming**. Olympiads in Informatics, v. 2, p. 149–162, 2008.


## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Complete, se ajudar:

> “Nosso TCC produz, melhora, analisa ou permite `{{capacidade}}`.”

Exemplos: otimizar consultas; classificar imagens; detectar anomalias; comparar modelos; identificar padrões; prever demanda; analisar desempenho; gerar resumos; recomendar configurações.

Nosso TCC permite a exploração autônoma da programação competitiva ao gerar uma trilha de estudo pautada por bases de conhecimento consolidadas. 

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

[H] H01 - Espera-se que as trilhas de estudo geradas sejam comparáveis às trilhas apresentadas nos livros-fonte. *(hipótese técnica do TCC, não de IHC — ver seção 10)*

[?] H02 - Espera-se que a ferramenta seja bem recebida pelos usuários. A equipe reconhece que "bem recebida" ainda não é uma afirmação investigável: pode significar compreensão, utilidade percebida, confiança, facilidade de decidir o próximo passo ou intenção de uso. Qual desses aspectos importa ao projeto será decidido a partir das necessidades levantadas nas Entregas 3 e 7, e não escolhido antecipadamente.


## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Geração automática de trilhas de aprendizado | Ferramenta que facilita o aprendizado não supervisionado por tutor e de amplo acesso através da Web |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

Se não houver interface prevista no TCC, escreva `NÃO SE APLICA AO ESCOPO ORIGINAL` e prossiga para 2.2.

[F] Estudantes de programação competitiva.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Papel no recorte de IHC | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|---|
| Aluno iniciante em programação competitiva | **usuário primário** | Usuário direto da interface | Submeter um enunciado e usar a trilha gerada para decidir o que estudar antes de tentar resolver a questão | [F] público-alvo declarado na Seção II do TCC: "ferramenta de auxílio ao estudo em programação competitiva" |
| Tutor / treinador de equipe | **usuário secundário, não prioritário** | Usuário direto da interface, em hipótese | Gerar trilhas para montar plano de treino | [H] H11 — a equipe não tem evidência de que tutores usariam a ferramenta nem de que assumiriam essa responsabilidade |
| Pesquisador de PLN/educação | **fora do recorte de IHC** | Consome o artefato técnico do TCC (o modelo), não a interface | Baixar o modelo publicado no Hugging Face e reproduzir os experimentos | [H] H03 quanto ao interesse efetivo; [F] quanto à publicação do modelo (Seção VI.C.1 do TCC) |

**Decisão de recorte (revisão após feedback):** o projeto de IHC será conduzido para o **aluno iniciante**. O tutor permanece no mapa de stakeholders, mas **não influenciará decisões de interface** enquanto H11 não for investigada. O pesquisador está fora do recorte: ele usa a contribuição técnica do TCC, não a interação projetada aqui.


## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Pesquisador de PLN/educação | Consome o modelo por linha de comando ou *notebook*, sem passar pela interface projetada na disciplina | não | [H] H04 — plausível pela publicação do modelo no Hugging Face, mas a equipe não observou nenhum uso real |
| Professor ou instituição que venha a adotar a ferramenta em disciplina ou treino | Passaria a depender da qualidade das trilhas para orientar turmas | indiretamente | [?] Q01 — não sabemos se existe interesse institucional; nenhuma evidência foi levantada |


## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] H05 - A interação com a aplicação por parte de um aluno exige que a linguagem seja compreensível para indivíduos com pouco conhecimento em termos de programação competitiva.

[H] H06 - O aluno iniciante sabe operar uma interface web sem dificuldade, mas não tem repertório para julgar se a trilha recebida está correta.

[?] Q02 - Não sabemos o que significa concretamente "aluno iniciante" neste domínio: quanto de programação já sabe, se já usa juiz online, se reconhece os nomes dos tópicos algorítmicos, há quanto tempo pratica. Essas diferenças podem alterar bastante a interação e serão investigadas na Entrega 3.

[?] Q03 - Não sabemos se há necessidade de acessibilidade específica nesse público (contraste, navegação por teclado, leitor de tela, alternativa textual a uma representação gráfica). Será investigado na Entrega 3 e tratado na Entrega 8.

---


# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[H] H07 - O aluno está tentando **destravar em uma questão e voltar a progredir no treino**: ele quer adquirir o conhecimento que lhe falta para resolver aquela questão por conta própria, sem receber a solução pronta.

> **Revisão após feedback:** a formulação anterior de H07 dizia "de forma visual e consolidada em fontes confiáveis". Isso descrevia características da solução imaginada pela equipe, não o objetivo do aluno. Essas características foram separadas e passaram a ser a hipótese de design H15 (seção 10), que precisa ser investigada antes de virar requisito.


## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Descobrir o que precisa saber para conseguir resolver uma questão em que travou | Aluno | [H] alta frequência / [H] alta criticidade | [F] a atividade existe e motiva o TCC (Seção I); [H] H08 quanto à frequência e [H] H16 quanto à criticidade — a equipe ainda não observou alunos |
| A02 | Montar um plano de estudo/treino a partir de um conjunto de questões | Tutor | [?] frequência e criticidade desconhecidas | [H] H11 — a própria existência desta atividade como uso da ferramenta é hipótese |

> A classificação de frequência e criticidade acima era apresentada como fato na versão anterior. Nenhuma das duas foi medida; ambas passam a ser hipóteses rastreadas na seção 10.


## 3.3 Qual atividade parece mais frequente? Por quê?

[H] H08 - A atividade mais frequente parece ser A01, a consulta feita por um aluno para descobrir os tópicos de uma determinada questão. O raciocínio da equipe é que existem muito mais alunos do que tutores e que o aluno encontra várias questões por sessão de treino. **Isso é plausível, não observado.**

[?] Q04 - Não sabemos com que frequência um aluno realmente trava a ponto de buscar ajuda externa, nem quantas vezes isso acontece por sessão de treino. Será investigado na Entrega 7.


## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[H] H16 - A atividade mais crítica é A01. Ela é crítica porque, segundo H06, o aluno iniciante não tem repertório para perceber que a orientação recebida está errada — e por isso pode confiar mais em uma orientação incorreta do que em uma correta que contrarie sua intuição.

**Distinção entre tipos de erro (revisão após feedback).** A versão anterior falava genericamente em "passar o conteúdo errado". São quatro coisas diferentes, com consequências diferentes:

| Tipo de erro | O que acontece | Consequência | Onde será tratado |
|---|---|---|---|
| Erro da atividade atual do aluno | Sem a ferramenta, o aluno escolhe sozinho o que estudar e escolhe mal | Estuda tópico irrelevante; é o problema que motiva o projeto | Entrega 4 (cenário) |
| Erro da contribuição técnica do TCC | O modelo infere tópicos incorretos ou incompletos | A trilha está errada na origem | Escopo do TCC; para IHC importa **como isso é comunicado** |
| Erro de interpretação da interface | A trilha está correta, mas o aluno entende a ordem, o escopo ou a fonte de outro modo | O aluno estuda a coisa certa da maneira errada, ou desiste achando que não entendeu | Entregas 5, 10 e 13 |
| Erro de confiança | O aluno aceita como verdade uma trilha incorreta por não ter repertório para contestá-la (H06) | Combina os dois anteriores e é o mais difícil de detectar | Entregas 7, 8 e 14 |

[?] Q05 - Não sabemos qual a consequência pedagógica real de cada um desses erros para um aluno iniciante — se ele reconhece o erro depois, se abandona a trilha, se volta ao método antigo. Investigar nas Entregas 7 e 14.

---


# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

[F] **Pelas tags do próprio juiz online.** O Codeforces associa a cada questão rótulos temáticos e os mantém ocultos durante competição. *Fonte:* Seções I e IV.A do TCC; inspeção direta de codeforces.com em 26/08/2026. **O que é fato é que a plataforma funciona assim.** Que o aluno efetivamente use as tags para decidir o que estudar é hipótese — ver H17.

[H] H17 - O aluno consulta as tags da questão e tenta inferir sozinho o que estudar a partir delas.

[H] H18 - O aluno procura editoriais, soluções comentadas ou discussões de outros competidores em fóruns.

[H] H19 - O aluno cola o enunciado em um chatbot de propósito geral (ChatGPT, Claude) e pede explicação.

[F] **O modelo do TCC, hoje, só é acessível por via técnica.** O modelo é publicado no Hugging Face e os resultados de inferência são salvos em JSON; não existe nenhuma via de acesso não técnica. *Fonte:* Seção VI.C.1 do TCC.

> H17, H18 e H19 descrevem comportamentos plausíveis do aluno que a equipe **não observou**. Eram apresentados como fato na versão anterior. A Entrega 7 deverá verificar quais desses caminhos são efetivamente usados e em que ordem.


## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

| Dificuldade | Natureza | Status/evidência |
|---|---|---|
| Não existe via de acesso não técnica ao modelo: usá-lo exige ambiente, Python e Hugging Face | Barreira de acesso à contribuição do TCC | [F] Seção VI.C.1 do TCC. *É fato que a barreira existe; que ela seja vivida como "confusa" pelo aluno é hipótese, ver H20* |
| A tag do juiz online nomeia o tópico, mas não indica ordem de estudo nem pré-requisitos | Falta de orientação | [F] Seção I do TCC e inspeção da plataforma |
| O resultado atual da ferramenta é uma lista de tópicos sem dependências entre eles e sem indicar a fonte pedagógica | Falta de estrutura e de lastro | [F] a Seção VII.C do TCC declara exatamente essas duas lacunas |
| O modelo erra com frequência mensurável e não sinaliza quando está incerto | Risco | [F] F1 Macro de 0,5820 e caso de alucinação registrado (Seção VII.B do TCC) |

[H] H20 - Para um aluno iniciante, localizar e executar o modelo seria percebido como confuso e inviável.


## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

> **Revisão após feedback.** A resposta anterior ("saber ler e escrever") descrevia uma habilidade do usuário, não a informação interpretada durante a atividade. A pergunta correta é: **quais sinais o aluno observa hoje, quando trava, para decidir qual é o próximo passo de estudo?**

[?] Q06 - **Esta é a principal lacuna de conhecimento da entrega.** A equipe não sabe quais informações o aluno realmente usa nesse momento de decisão. Candidatos plausíveis, a verificar:

- o enunciado e as palavras que ele reconhece ou não reconhece nele;
- as tags da questão, quando visíveis;
- o *rating* de dificuldade da questão;
- quantas pessoas resolveram a questão;
- o que ele já tentou e falhou;
- o vocabulário de um editorial ou de uma resposta de fórum;
- a recomendação de um colega ou tutor.

A investigação precisa descobrir **quais desses sinais o iniciante compreende, quais não compreende e em que ponto exato ele deixa de saber como continuar**. Método previsto: entrevista e observação na Entrega 7, alimentando o cenário da Entrega 4 e a análise de tarefas da Entrega 5.

Essa lacuna é decisiva porque define o que a interface precisa efetivamente comunicar — e não deve ser respondida deduzindo a partir da solução já imaginada.


## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

Ver a tabela de tipos de erro em 3.4. Resumidamente:

[H] H21 - O aluno estuda um tópico que não o aproxima da solução, perde tempo de treino e continua travado.

[H] H06 - Como ele não tem repertório para julgar a orientação recebida, pode não perceber que o caminho estava errado — o que torna o erro silencioso.

[?] Q05 - A consequência pedagógica de longo prazo (desmotivação, abandono, retorno ao método anterior) não é conhecida pela equipe.


## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

> **[H] Cenário hipotético.** A narrativa abaixo não foi observada nem relatada por um aluno real: foi construída pela equipe a partir do problema descrito na Seção I do TCC. Ela será substituída por um cenário sustentado em dados na Entrega 4, depois da investigação da Entrega 7.

Um aluno está treinando para uma competição de programação competitiva. Ele chega a uma questão e não sabe por onde começar, porque não identifica quais tópicos ela exige. Ele releia o enunciado, procura questões parecidas já resolvidas em fóruns e tenta encontrar o assunto em um livro didático por conta própria. Sem saber o nome do que precisa procurar, a busca é por tentativa e erro e consome o tempo que ele tinha reservado para treinar.

[?] Q07 - A versão anterior desta narrativa afirmava que o aluno "pode desistir da competição ou da modalidade". Essa é uma afirmação forte sobre evasão e a equipe não tem evidência dela. Fica registrada como lacuna a investigar, não como consequência conhecida.


## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| TCC da equipe — `GERAÇÃO_AUTOMÁTICA_DE_TRILHAS_DE_ESTUDO_PARA_PROGRAMAÇÃO_COMPETITIVA-1.pdf` (2026) | Objetivo e público-alvo declarados, arquitetura, F1 Macro de 0,5820, caso de alucinação e as duas lacunas do resultado atual (Seção VII.C) | Documento da própria equipe; não contém nenhum dado empírico sobre usuários |
| RIBEIRO, P.; GUERREIRO, P. *Early introduction of competitive programming*. Olympiads in Informatics, v. 2, 2008 | Benefício da prática e o abismo teoria–prática quando o aluno não domina o assunto | Estudo de 2008, contexto europeu, anterior aos LLMs; não trata de escolha de material de estudo |
| [Codeforces](https://codeforces.com/) — inspeção direta em 26/08/2026 | Que a identificação de conteúdo é feita por tags e que elas ficam ocultas durante competição | Observação de uma plataforma, sem registro sistemático; não diz nada sobre como o aluno usa essas tags |

**Evidência que a equipe não possui:** nenhum dado coletado com alunos — nenhuma entrevista, observação, questionário ou relato identificado. Por isso, **toda afirmação desta entrega sobre comportamento, preferência, frequência, dificuldade percebida ou consequência permanece `[H]` ou `[?]`**, mesmo quando parece óbvia para a equipe.

---


# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] H09 - A interação pode ocorrer com um aluno sozinho, fazendo uma consulta na ferramenta para estudo. **Este é o contexto prioritário adotado pela equipe**, e permanece como hipótese de trabalho.
[H] H10 - A interação pode ocorrer com um aluno acompanhado de um tutor, contando com o apoio dele para dúvidas mais específicas sobre o tópico.
[H] H11 - A interação pode ocorrer com um tutor sozinho, a fim de certificar-se de que a ferramenta é válida e correta.

[?] Q08 - **Treino ou competição?** A equipe adotou o treino individual como contexto, mas usa "competição" de forma ampla em vários trechos. São situações muito diferentes: em competição há pressão de tempo severa, as tags ficam ocultas e consultar material externo pode ser proibido pelo regulamento. Se o uso durante competição faz ou não parte do contexto pretendido é uma lacuna a esclarecer, não algo a presumir. Investigar na Entrega 3.


## 5.2 Em quais dispositivos/equipamentos?

[F] A aplicação é web e, tecnicamente, roda em qualquer dispositivo com navegador e conexão. *Fonte:* interface web prevista no TCC (0.5).

> Isso é uma **possibilidade técnica da Web**, não uma afirmação sobre a experiência de uso. Uma trilha representada como grafo de dependências pode ser legível em notebook e impraticável em celular.

[H] H22 - O uso predominante ocorre em notebook ou desktop, porque a questão está aberta em outra aba e o aluno está programando na mesma máquina.

[?] Q09 - Não sabemos qual dispositivo o aluno realmente usa ao treinar, nem se consultaria a ferramenta pelo celular. Investigar na Entrega 3; a resposta afeta diretamente a viabilidade da representação em grafo.


## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

> **Revisão após feedback.** A resposta anterior reduzia o contexto à conexão com a Internet. Contexto de uso em IHC envolve também momento, ambiente, recursos disponíveis, interrupções, pressão de tempo e experiência prévia.

| Dimensão de contexto | Situação considerada | Status |
|---|---|---|
| Conexão | Necessária; sem conexão não há consulta | [F] decorre da arquitetura web |
| Momento da atividade | Durante ou logo após uma tentativa frustrada de resolver a questão — o aluno chega à ferramenta já travado | [H] H23 |
| Pressão de tempo | Em treino, moderada; em competição, severa | [?] Q08 — depende de decidir se competição entra no contexto |
| Ambiente | Casa, laboratório da faculdade ou sala de treino de equipe | [?] Q10 |
| Interrupções e paralelismo | O aluno alterna entre enunciado, editor de código e ferramenta de consulta | [H] H24 |
| Recursos disponíveis | Acesso simultâneo ao juiz online, a uma IDE e possivelmente a livros | [H] H24 |
| Experiência prévia | Baixo conhecimento de domínio, alta familiaridade com ferramentas web | [H] H06 |
| Privacidade | Sem dado sensível; não há requisito identificado | [F] o conteúdo tratado são enunciados públicos |


## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[H] H25 - Se a ferramenta for usada por um tutor, caberia a ele conferir a correção do conteúdo antes de repassá-lo ao aluno. A versão anterior afirmava isso como fato; é uma **atribuição de responsabilidade que a equipe supôs**, sem ter conversado com nenhum tutor.

[?] Q11 - Não sabemos se existe alguma estrutura organizacional relevante em torno desse público — equipes de maratona com treinador, disciplinas eletivas, grupos de estudo informais — nem que papéis existiriam nelas. Investigar na Entrega 3.

[F] No contexto prioritário adotado (H09, aluno sozinho), não há aprovação, hierarquia nem responsabilidade profissional envolvida.


## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[F] **Não há requisito de auditoria ou conformidade.** Não se trata dado pessoal sensível, não há aprovação hierárquica nem exigência regulatória sobre o conteúdo gerado.

[?] Q12 - **A necessidade de histórico pessoal não foi investigada.** A resposta anterior era um "Não" categórico, e na seção 8 o histórico foi descartado por não estar previsto na implementação — que é um critério técnico, não um critério de IHC. O argumento a favor existe: uma trilha de estudo é consumida ao longo de dias, não de uma sessão, e sem histórico o aluno perderia o resultado ao fechar a aba. A decisão correta é manter a lacuna aberta até a Entrega 7 e decidir por necessidade do usuário, não por viabilidade.


## 5.6 Um erro pode produzir consequência relevante? Qual?

[H] H21 - O erro mais relevante é o aluno estudar tópicos não relacionados à questão e perder tempo de treino. Ver a tabela de tipos de erro em 3.4.

[F] O erro tem probabilidade concreta e conhecida do lado técnico: F1 Macro de 0,5820 na classificação de rótulos, com caso registrado de alucinação em inferência. *Fonte:* Seção VII.B do TCC.

[F] Não há consequência física, financeira, legal ou de segurança. A criticidade é **pedagógica e motivacional**.

[?] Q05 - O tamanho real dessa consequência para o aluno não é conhecido.

---


# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Juízes online e seus fóruns (ex.: Codeforces) | Alunos | Praticar, consultar questões e discutir soluções | [F] a plataforma existe e oferece isso (inspeção em 26/08/2026); [H] H17 e H18 quanto ao uso efetivo pelo aluno iniciante |
| Chatbots de propósito geral (ex.: ChatGPT) | Alunos | Pedir explicação sobre um enunciado | [H] H19 — plausível pela popularidade, não verificado neste público |
| Livros e materiais didáticos consolidados | Alunos e tutores | Estudar um assunto de forma estruturada | [F] existem e são a base pedagógica adotada pelo TCC; [H] H26 quanto ao uso pelo iniciante |


## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

[F] Sim. Foram examinados dois na Entrega 2: o juiz online Codeforces e o chatbot ChatGPT. Existem outros produtos das mesmas famílias (Beecrowd, LeetCode, Claude, Gemini), **mas a equipe não os examinou** e por isso não afirma nada sobre eles.


## 6.3 Quais interfaces profissionais esse público já conhece?

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

[H] H27 - O público já conhece juízes online, fóruns de programação, chatbots e IDEs. É plausível por se tratar de estudantes de computação, mas **quais ferramentas cada aluno realmente usa, e com que frequência, não foi levantado**. Investigar na Entrega 3.


## 6.4 O que essas soluções parecem fazer bem?

[F] O Codeforces mantém um acervo de questões com rótulos, filtros e histórico de competições, e devolve veredito automático das submissões. *Observado em codeforces.com em 26/08/2026 — ver Entrega 2, C01.*

[F] O ChatGPT concentra a ação inicial em uma caixa de texto única, com poucas opções concorrentes na tela. *Observado em chatgpt.com em 26/08/2026 — ver Entrega 2, C02.*

> Ambas são descrições do que foi observado nos produtos. Se essas características **funcionam bem para o aluno iniciante** é outra questão, ainda não investigada.


## 6.5 O que parecem fazer mal, dificultar ou não atender?

> **Revisão após feedback.** A versão anterior apresentava estas limitações como fatos de categorias inteiras ("fóruns entregam a solução pronta", "livros trazem a trilha correta"). A equipe examinou dois produtos. As afirmações foram limitadas ao que foi observado ou reclassificadas como hipótese.

| Alternativa | O que não atende | Status/evidência |
|---|---|---|
| Codeforces (examinado) | As tags nomeiam o tópico mas não apresentam ordem de estudo, pré-requisitos nem material de apoio | [F] observado em 26/08/2026 (Entrega 2, C01) |
| ChatGPT (examinado) | Na consulta observada, a resposta veio como texto corrido, sem representação de dependência entre tópicos e sem citar fonte pedagógica verificável | [F] limitado à consulta observada (Entrega 2, C02) — não é uma afirmação sobre o produto em todos os usos |
| Chatbots em geral | Suposição de que todos se comportam como o ChatGPT observado | [H] H28 — a equipe examinou um produto; não é base para concluir sobre a categoria |
| Fóruns e editoriais | Suposição de que entregam a solução pronta e por isso não constroem caminho de estudo | [H] H18 |
| Livros e materiais didáticos | Suposição de que trazem a trilha correta, mas organizada por assunto, de modo que o aluno travado não sabe em que capítulo procurar | [H] H26 |

A Entrega 2 aprofundou Codeforces e ChatGPT. As demais linhas seguem como hipótese até que haja observação sistemática.


## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

[H] H12 - Caixa de texto única com envio e resposta em fluxo de conversa, no padrão consolidado por ChatGPT e Claude.

[H] H13 - Listas de problemas com filtros por tag e dificuldade, e página de problema com enunciado + metadados, no padrão dos juízes online.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

O TCC prevê uma interface web. A interface web será utilizada como entrada de dados por parte do usuário com estilo de chat. Além disso a resposta também sera neste chat em um formato de grafo com nós de tópicos e arestas representando dependência. 

## 7.2 Qual perfil será priorizado no projeto de IHC?

Aluno iniciante em programação competitiva.

**Por que esse perfil foi escolhido?**

Por que o usuário principal da interface será o aluno fazendo uma consulta.

## 7.3 Qual objetivo desse usuário será priorizado?

Descobrir o que precisa saber para conseguir resolver, por conta própria, uma questão em que travou. (A01)

## 7.4 Que interface será explorada na disciplina?

**Para fins da disciplina de IHC, será projetada uma interface web que permita a um `aluno iniciante em programação competitiva` utilizar `a trilha de estudo gerada automaticamente a partir do enunciado de uma questão` para `descobrir o que estudar, em que ordem e em qual material, antes de tentar resolver a questão por conta própria`, no contexto de `treino individual em juízes online, com a questão aberta em outra aba e sem apoio de um tutor no momento`.**

## 7.5 Qual é a relação dessa interface com o TCC?

- [X] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra: —.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

> **Revisão após feedback.** A versão anterior descartou histórico e outros padrões por não estarem previstos na implementação. Viabilidade técnica não é critério de IHC. A pergunta correta é **"existe uma atividade ou objetivo do usuário que justifique este padrão?"**, e quando a equipe ainda não sabe a resposta, o estado correto é *em aberto*, não *não*.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | não | Nenhuma decisão de A01 depende de indicadores agregados. O aluno chega com uma questão específica, não com uma visão geral a monitorar. | — |
| Configuração/parametrização | em aberto | Escolher a fonte pedagógica preferida ou o nível de profundidade da trilha — **se** o aluno tiver essa preferência | [H] H14 |
| Entrada/upload/seleção de dados | sim | A01 — submeter o enunciado é o ato que inicia toda a atividade | [F] o sistema recebe o enunciado como entrada (Seção VI do TCC) |
| Acompanhamento de processamento | sim | A01 — a inferência do LLM tem latência perceptível; sem retorno, o aluno não distingue "processando" de "travou" | [F] restrição registrada em 9.3; reforçado pela RC02 da Entrega 2 |
| Relatório/resultados | sim | A01 — é o núcleo: os tópicos, a relação entre eles e a fonte de cada um | [F] as duas lacunas declaradas na Seção VII.C do TCC |
| Histórico com busca/filtros | em aberto | Retomar uma trilha em outra sessão, já que o estudo se estende por dias. **Descartado antes por critério técnico, o que estava errado.** | [?] Q12 — necessidade não investigada |
| Comparação de resultados | não | Comparar trilhas com e sem tags é atividade de pesquisa do TCC, não do aluno iniciante | [F] é objeto da Seção VII do TCC |
| Explicabilidade/detalhamento | sim | A01 e o erro de confiança (3.4) — saber por que um tópico foi indicado, de que fonte vem e o quanto o sistema está seguro | [F] F1 Macro 0,5820 e alucinação registrada (Seção VII.B do TCC); [H] H06 |
| Administração/configurações globais | não | Não há operação institucional nem parâmetro sob responsabilidade de um administrador no recorte escolhido. *A versão anterior justificava com "configurar elementos visuais", que é preferência de aparência e não caracteriza tela administrativa.* | — |
| Usuários/perfis/permissões | em aberto | Só se o histórico (Q12) exigir identificar o aluno entre sessões. Ainda assim o objetivo seria *recuperar minha trilha*, não *gerenciar usuários* | [?] Q12 |
| CRUD de entidade do domínio | não | Nenhuma atividade do aluno envolve criar, editar e excluir entidades do domínio | — |
| Auditoria/logs | não | Não há requisito de conformidade, aprovação ou responsabilização formal | [F] 5.5 |
| Alertas/ocorrências | não | O único aviso relevante — baixa confiança na classificação — pertence ao resultado e será tratado dentro de explicabilidade | [H] H06 |
| Ajuda/documentação | em aberto | Glossário dos termos algorítmicos, que chegam em jargão e em inglês a quem por definição ainda não os domina | [H] H05; [?] Q06 |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---


# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

> **Revisão após feedback.** A versão anterior descrevia o benefício como "tornar a capacidade do TCC utilizável sem conhecimento de IA, Python ou Hugging Face". Isso é um benefício de acesso à tecnologia, não o benefício humano que justifica o projeto — o aluno não quer deixar de usar Hugging Face, ele quer destravar e voltar a progredir.

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Sair de uma questão travada sabendo qual é o próximo passo de estudo | Hoje o aluno não identifica o que lhe falta saber e busca por tentativa e erro | Aluno iniciante | [F] problema descrito na Seção I do TCC; [H] H07 quanto ao objetivo do aluno |
| Chegar ao material certo sem precisar saber o nome do assunto de antemão | O aluno travado não sabe em que capítulo procurar | Aluno iniciante | [H] H26 |
| Conseguir avaliar o quanto confiar na orientação recebida antes de investir tempo nela | O iniciante não tem repertório para contestar uma orientação incorreta | Aluno iniciante | [H] H06; [F] F1 Macro 0,5820 (Seção VII.B do TCC) |
| *Efeito secundário:* tornar a contribuição do TCC utilizável sem preparo técnico | O modelo hoje só é acessível por linha de comando | Aluno e tutor | [F] Seção VI.C.1 do TCC. **É condição para os benefícios acima, não um benefício em si.** |

## 9.2 Que ações o usuário deverá conseguir realizar?

> Estas ações são **decisões preliminares de solução**, derivadas do objetivo A01. Elas serão revistas na Entrega 5, quando a tarefa real do usuário for decomposta. Como observou o feedback, a tarefa do aluno não começa em "colar o enunciado" — isso já é um passo da interface, não da atividade.

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Apresentar ao sistema a questão em que travou | A01 — iniciar a consulta sem preparo técnico | alta |
| F02 | Saber que a consulta está em processamento e que o sistema não travou | A01 — não abandonar a consulta no meio | alta |
| F03 | Compreender quais tópicos precisa estudar e em que ordem, incluindo o que depende do quê | A01 — saber por onde começar | alta |
| F04 | Chegar ao material de estudo que sustenta cada tópico | A01 — saber onde estudar | alta |
| F05 | Avaliar o quanto pode confiar no que recebeu | Reduzir o erro de confiança descrito em 3.4 | alta |

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| LLM Qwen3-4B-Instruct-2507 com ajuste fino | Equilíbrio entre capacidade de inferência semântica e custo computacional (Seção VI.B do TCC) | Inferência não é instantânea: exige feedback de progresso (F02) |
| F1 Macro de 0,5820 na classificação de rótulos | Resultado medido no TCC, abaixo do baseline de 0,79 de Souza et al. | O erro é frequente o bastante para ser regra de projeto, não exceção: sustenta F05 |
| Caso registrado de alucinação em inferência | Observado na segunda iteração de treinamento (Seção VII.B do TCC) | A interface precisa prever resposta incoerente e não exibi-la como trilha legítima |
| Modelo treinado sobre enunciados do Codeforces **em inglês**, com tags em inglês | A base de Dinu et al. é em inglês (Seção VII.A do TCC) | Possível barreira de vocabulário para um público brasileiro iniciante — relaciona-se a H05 e Q06 |
| Aplicação web dependente de conexão | Interface web prevista no TCC | Sem conexão não há consulta |
| Recuperação nas fontes pedagógicas ainda não implementada | Etapa planejada e não concluída (Seções VI e VII.C do TCC) | F04 será prototipado na disciplina mesmo sem a integração existir ainda no TCC |

---


# 10. Hipóteses e dúvidas prioritárias

> **Convenção e prioridade (revisão após feedback).** `Hnn` = hipótese; `Qnn` = lacuna de conhecimento. Cada linha indica, no início da coluna "Por que importa", se é **[CRÍTICA]** para o recorte de IHC, **[SECUNDÁRIA]** ou **[TÉCNICA DO TCC]** — esta última não pertence ao recorte de IHC e não deve ocupar o mesmo nível de análise.
>
> **`H04` foi mantida.** A numeração da versão anterior saltava de H03 para H05 porque H04 havia sido retirada de 2.3 por engano; ela foi restabelecida e a sequência H01–H14 está completa. Os IDs H05, H06, H08, H09, H12 e H13 foram **preservados**, sem renumeração, porque já são citados na Entrega 2 e no feedback do professor.

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Espera-se que as trilhas de estudo geradas sejam comparáveis às trilhas apresentadas nos livros-fonte. | **[TÉCNICA DO TCC]** É a validação científica do trabalho, não uma questão de interação. Para IHC importa apenas o reflexo: se a trilha pode errar, a interface precisa comunicar isso. | Avaliação experimental do TCC — comparação das trilhas geradas com trilhas de livros e currículos, pelas métricas já definidas na Seção VI.D do TCC. |
| H02 | Espera-se que a ferramenta seja bem recebida pelos usuários. | **[SECUNDÁRIA — a reformular]** Como está, não é investigável: "bem recebida" pode ser satisfação, confiança, utilidade percebida ou facilidade de decidir. Não será decomposta agora para não escolher uma métrica antes de conhecer a necessidade. | Primeiro decidir, a partir das Entregas 3 e 7, qual aspecto da experiência importa ao projeto; só então virará meta verificável na Entrega 8. |
| H03 | Pesquisadores teriam interesse em baixar o modelo, reproduzir os experimentos e analisar o processo de geração de trilhas. | **[FORA DO RECORTE]** Diz respeito ao artefato técnico do TCC, não à interface do aluno. Mantida apenas para registrar por que o perfil ficou fora. | Não será investigada na disciplina. Evidência eventual viria de downloads/citações do modelo no Hugging Face. |
| H04 | O pesquisador consome o modelo por linha de comando ou notebook, sem passar pela interface projetada. | **[FORA DO RECORTE]** Confirma que o pesquisador é stakeholder do TCC e não usuário da interface. | Não será investigada. Basta observar que o artefato publicado é um modelo, não uma aplicação. |
| H05 | A interação por parte do aluno exige que a linguagem seja compreensível para quem tem pouco conhecimento de programação competitiva. | **[CRÍTICA]** Determina vocabulário, rotulagem e necessidade de glossário em toda a interface. A Entrega 2 mostrou duas estratégias opostas de terminologia (Codeforces x ChatGPT) sem indicar qual serve ao iniciante. | Entrega 7: questionário e entrevista pedindo que alunos expliquem, com as próprias palavras, termos como `dp`, `greedy` e `pré-requisito`; observar em qual vocabulário eles descrevem o que não sabem. Evidência que enfraqueceria: iniciantes reconhecerem e preferirem o jargão original. |
| H06 | O aluno iniciante sabe operar uma interface web sem dificuldade, mas não tem repertório para julgar se a trilha recebida está correta. | **[CRÍTICA]** É a premissa que desloca o projeto de "operar" para "interpretar e confiar". Se confirmada, explicabilidade, fonte e sinalização de incerteza deixam de ser acessórios. | Entrega 7: apresentar a alunos duas trilhas para a mesma questão, uma correta e uma com tópico intruso, e observar se percebem a diferença e como justificam. Evidência que enfraqueceria: iniciantes detectarem o intruso com segurança. |
| H07 | O aluno está tentando destravar em uma questão e voltar a progredir no treino, sem receber a solução pronta. | **[CRÍTICA]** É o objetivo do usuário. Se ele na verdade quiser a solução, todo o recorte muda. | Entrega 7: perguntar o que o aluno faz ao travar e o que consideraria uma ajuda satisfatória. Entrega 4: construir o cenário a partir dessas respostas. |
| H08 | A atividade mais frequente é a consulta feita por um aluno para descobrir os tópicos de uma determinada questão. | **[CRÍTICA]** Define qual fluxo recebe prioridade de modelagem (Entrega 5), prototipação (Entrega 11) e avaliação (Entrega 14). | Entrega 7: questionário sobre com que frequência o aluno trava e o que faz em seguida; comparar com a frequência declarada por tutores. |
| H09 | A interação ocorre com um aluno sozinho, fazendo uma consulta na ferramenta para estudo. | **[CRÍTICA]** É o contexto de uso adotado; define o quanto a interface precisa ser autoexplicativa, já que não há ninguém para tirar dúvidas. | Entrega 3: levantamento de contexto — onde, quando e com quem o aluno treina. Ligado a Q08 (treino x competição). |
| H10 | A interação pode ocorrer com um aluno acompanhado de um tutor. | **[SECUNDÁRIA]** Geraria um segundo cenário na Entrega 4 e reduziria a exigência de autoexplicação. | Entrega 3 e Entrega 7, junto com H09. |
| H11 | A interação pode ocorrer com um tutor sozinho, para certificar-se de que a ferramenta é válida e correta. | **[SECUNDÁRIA]** Enquanto não for investigada, o tutor **não** influencia decisões da interface (ver 2.2). | Entrega 7: entrevista com treinadores de equipe de maratona, se houver acesso. |
| H12 | A caixa de texto única com envio e resposta em fluxo de conversa é um padrão familiar a esse público. | **[CRÍTICA]** Sustenta a entrada conversacional adotada em 7.4. A Entrega 2 mostrou que o padrão **existe** no ChatGPT; isso não demonstra que seja familiar ou adequado ao aluno iniciante. | Entrega 6: protótipo em papel com duas formas de entrada, observando qual o aluno usa sem instrução. Entrega 7: perguntar que ferramentas de chat ele já usa. |
| H13 | Listas de problemas com filtros por tag e dificuldade são um padrão familiar ao público, vindo dos juízes online. | **[SECUNDÁRIA]** O fluxo principal é uma consulta individual a partir de uma questão; ainda não há tarefa no projeto que exija lista com filtros. | Entrega 5: verificar se alguma tarefa decomposta realmente precisa desse padrão. Se nenhuma precisar, a hipótese sai do escopo. |
| H14 | O usuário teria interesse em escolher a fonte pedagógica preferida ou o nível de profundidade da trilha. | **[SECUNDÁRIA]** Decide se configuração vira tela ou se o caso se resolve por um bom padrão sem tela. | Entrega 7: perguntar se o aluno tem preferência de material e se saberia escolher entre fontes. |
| H15 | Uma trilha apresentada visualmente, como grafo de dependências ancorado em fontes, é compreendida melhor pelo aluno do que a mesma trilha em texto corrido. | **[CRÍTICA — hipótese de design]** Era parte da formulação de H07 e foi separada porque descreve a solução, não o objetivo. É a aposta central do recorte de 7.4: se for refutada, o formato do resultado muda. | Entrega 6: protótipo em papel comparando grafo e lista para a mesma questão, observando qual permite ao aluno dizer por onde começaria. Entrega 14: teste com usuários. |
| H16 | A atividade A01 é de alta criticidade porque o erro é silencioso: o aluno não percebe que a orientação estava errada. | **[CRÍTICA]** Define a severidade dos problemas na avaliação heurística (Entrega 13) e as metas de qualidade (Entrega 8). | Entrega 7 e Entrega 14, junto com H06. |
| H17 | O aluno consulta as tags da questão e tenta inferir sozinho o que estudar a partir delas. | **[CRÍTICA]** Descreve o processo atual. A Entrega 4 precisa desse dado para construir o cenário-problema. | Entrega 7: observação de alunos resolvendo uma questão desconhecida, registrando o que consultam e em que ordem. |
| H18 | O aluno procura editoriais, soluções comentadas ou discussões em fóruns, que entregam a solução pronta em vez de construir o caminho de estudo. | **[SECUNDÁRIA]** Se for o caminho dominante, o projeto compete com editoriais e não com tags. | Entrega 7, junto com H17. |
| H19 | O aluno cola o enunciado em um chatbot de propósito geral e pede explicação. | **[CRÍTICA]** Define quem é o concorrente real. A Entrega 2 examinou o ChatGPT justamente por essa suposição. | Entrega 7: perguntar diretamente se usa e para quê; pedir que mostre uma conversa real, se houver. |
| H20 | Para um aluno iniciante, localizar e executar o modelo no Hugging Face seria percebido como confuso e inviável. | **[SECUNDÁRIA]** Sustenta a existência de uma interface, mas não orienta nenhuma decisão de design. | Entrega 7, como pergunta de apoio. |
| H21 | O erro mais relevante é o aluno estudar tópicos não relacionados e perder tempo de treino. | **[CRÍTICA]** Define o que a interface precisa evitar e a severidade na Entrega 13. | Entregas 7 e 14. |
| H22 | O uso predominante ocorre em notebook ou desktop, porque a questão está aberta em outra aba. | **[CRÍTICA]** Decide a viabilidade da representação em grafo: o que é legível em notebook pode ser impraticável em celular. | Entrega 3: levantamento de dispositivo no contexto real de treino. |
| H23 | O aluno chega à ferramenta já travado, durante ou logo após uma tentativa frustrada. | **[CRÍTICA]** Define o estado emocional e cognitivo em que a interação começa e o que precisa estar visível na primeira tela. | Entregas 3 e 4. |
| H24 | O aluno alterna entre enunciado, editor de código e ferramenta de consulta, com interrupções. | **[SECUNDÁRIA]** Afeta retomada de contexto e reforça o argumento a favor do histórico (Q12). | Entrega 3. |
| H25 | Caberia ao tutor conferir a correção do conteúdo antes de repassá-lo ao aluno. | **[SECUNDÁRIA]** Atribuição de responsabilidade suposta pela equipe, sem conversa com nenhum tutor. | Entrega 7, junto com H11. |
| H26 | Livros e materiais consolidados trazem a trilha correta, mas organizada por assunto, de modo que o aluno travado não sabe em que capítulo procurar. | **[CRÍTICA]** É o que justifica ligar cada tópico a uma fonte específica (F04). | Entrega 2 (aprofundamento) e Entrega 7. |
| H27 | O público já conhece juízes online, fóruns, chatbots e IDEs. | **[SECUNDÁRIA]** Informa convenções, mas não decide nada sozinha. | Entrega 3: levantamento de ferramentas efetivamente usadas. |
| H28 | Chatbots de propósito geral, como categoria, comportam-se como o ChatGPT observado. | **[SECUNDÁRIA]** Generalização a partir de um produto examinado. Não sustenta conclusão de mercado. | Entrega 2 (ampliar a amostra) ou limitar a redação ao produto observado. |
| Q01 | Existe interesse institucional (professor, curso, equipe de maratona) em adotar a ferramenta? | **[SECUNDÁRIA]** Definiria um stakeholder adicional. | Entrega 3. |
| Q02 | O que significa concretamente "aluno iniciante" neste domínio? | **[CRÍTICA]** Sem isso, a persona da Entrega 3 será um estereótipo. | Entrega 3: levantamento de conhecimento prévio, tempo de prática, familiaridade com juízes online e vocabulário. |
| Q03 | Existe necessidade de acessibilidade específica nesse público? | **[CRÍTICA]** Define requisitos de contraste, teclado e alternativa textual ao grafo. | Entrega 3 e Entrega 8, com apoio da WCAG 2.2. |
| Q04 | Com que frequência um aluno realmente trava a ponto de buscar ajuda externa? | **[SECUNDÁRIA]** Complementa H08. | Entrega 7. |
| Q05 | Qual a consequência pedagógica real de cada tipo de erro descrito em 3.4? | **[CRÍTICA]** Calibra a severidade na Entrega 13 e as metas da Entrega 8. | Entregas 7 e 14. |
| Q06 | **Quais informações o aluno realmente interpreta, hoje, para decidir o que estudar quando trava?** | **[CRÍTICA — principal lacuna da entrega]** Define o que a interface precisa comunicar. Sem isso, o conteúdo da tela será deduzido da solução imaginada, e não da necessidade. | Entrega 7: observação de alunos travando em uma questão desconhecida, com protocolo *think-aloud*, registrando o que olham e o que dizem não entender. |
| Q07 | O aluno chega a abandonar a competição ou a modalidade por causa dessa dificuldade? | **[SECUNDÁRIA]** Afirmação forte sobre evasão, sem evidência. | Entrega 7, se houver acesso a alunos que pararam de praticar. |
| Q08 | O uso durante uma competição oficial faz parte do contexto pretendido? | **[CRÍTICA]** Em competição há pressão de tempo severa, tags ocultas e possível restrição de regulamento. Muda o recorte inteiro. | Entrega 3: decisão da equipe documentada, apoiada no regulamento das competições de referência. |
| Q09 | Que dispositivo o aluno usa ao treinar e consultaria a ferramenta? | **[CRÍTICA]** Afeta diretamente a viabilidade do grafo (H15, H22). | Entrega 3. |
| Q10 | Em que ambiente o treino acontece? | **[SECUNDÁRIA]** Complementa o contexto. | Entrega 3. |
| Q11 | Existe estrutura organizacional relevante em torno do público (equipe, treinador, disciplina)? | **[SECUNDÁRIA]** Definiria papéis e um possível segundo cenário. | Entrega 3. |
| Q12 | O aluno precisa recuperar uma trilha consultada anteriormente? | **[CRÍTICA]** Foi descartado antes por critério técnico, o que estava errado. Decide se histórico e identificação entram no escopo. | Entrega 7: perguntar em quantas sessões o aluno estuda um mesmo assunto e se voltaria a consultar. |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---


# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Gerar automaticamente, a partir do enunciado de uma questão de programação competitiva, uma trilha de estudo ordenada e ancorada em materiais didáticos consolidados. |
| O TCC já previa interface? | Sim, uma interface web — prevista, mas sem telas, fluxo ou forma de apresentação definidos. |
| Quem é o usuário prioritário de IHC? | Aluno iniciante em programação competitiva. Tutor é secundário e não influencia decisões enquanto H11 não for investigada; pesquisador está fora do recorte. |
| O que ele precisa alcançar? | A01 — destravar em uma questão e voltar a progredir no treino, descobrindo o que precisa estudar sem receber a solução pronta (H07). |
| Qual problema/atividade será estudado? | A decisão que o aluno toma quando trava: como ele identifica, hoje, o que lhe falta saber — e onde exatamente essa identificação falha (Q06). |
| Como isso acontece hoje? | Suposições a verificar: pelas tags do juiz online (H17), por editoriais e fóruns (H18) ou por chatbots generalistas (H19). O modelo do TCC, hoje, só é acessível por via técnica [F]. |
| Qual é o contexto de uso? | Treino individual, em navegador, com a questão aberta em outra aba e sem tutor presente (H09, H22, H23). Se competição entra no contexto é lacuna aberta (Q08). |
| Que interface/recorte será explorado? | O fluxo de interação descrito em 7.4: entrada conversacional e resultado estruturado com dependências entre tópicos e fonte pedagógica. É hipótese de trabalho, não decisão fechada (H12, H15). |
| Como a interface se relaciona ao TCC? | É o meio pelo qual o usuário acessa a contribuição do TCC. A disciplina aprofunda o fluxo, a apresentação e o tratamento de erro, que o TCC não especifica. |
| Quais pontos ainda são hipóteses? | H01–H28 e as lacunas Q01–Q12 (seção 10). As críticas para o recorte são H05, H06, H07, H08, H09, H12, H15, H16, H17, H19, H21, H22, H23, H26 e as lacunas Q02, Q03, Q05, Q06, Q08, Q09, Q12. |

### Delimitação

> **Revisão após feedback.** A versão anterior definia o escopo de IHC como "as telas da interface web". IHC não trata só de telas: o objeto é a **interação** entre a pessoa e o sistema — objetivos, atividade, contexto, comunicação, ações, respostas e experiência.

**Dentro do escopo de IHC:** o **processo de interação e de decisão** pelo qual o aluno, em contexto de estudo, chega travado a uma questão, apresenta essa questão ao sistema, acompanha o que o sistema faz, compreende o resultado, interpreta as relações entre os conteúdos indicados, avalia o quanto pode confiar neles, decide o que vai estudar e consegue retomar seu objetivo de resolver a questão. Isso inclui vocabulário, ordem da informação, respostas do sistema, tratamento de incerteza, rupturas de comunicação e recuperação de erro. As telas são a representação concreta dessa interação, não o escopo inteiro.

**Fora do escopo de IHC:** a construção técnica do modelo — ajuste fino, classificação de rótulos, mapeamento por similaridade de cosseno, métricas e avaliação experimental. **Exceção:** quando uma característica técnica produzir efeito perceptível para o usuário — latência, incerteza, resposta incoerente, vocabulário em inglês —, esse efeito **está** dentro do escopo de IHC, porque chega até a pessoa.

**Dentro do escopo formal do TCC:** classificação de tags, extração de características semânticas do enunciado, mapeamento para tópicos pedagógicos, recuperação nas fontes e construção da trilha, além da avaliação experimental desses resultados. A existência de uma interface web também está prevista, sem especificação.

**Interface da disciplina será implementada no TCC?** Não definido. O recorte foi projetado para ser compatível com o TCC e endereça duas lacunas que o próprio trabalho declara (Seção VII.C), mas a incorporação depende de decisão da equipe com o orientador.

---


# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** Um estudante iniciante trava em uma questão de programação competitiva e não descobre o que precisa estudar para resolvê-la.

2. **Contribuição técnica do TCC:** Um Grande Modelo de Linguagem ajustado lê o enunciado, infere os conceitos algorítmicos envolvidos e monta a partir deles uma trilha de estudo ancorada em livros didáticos consolidados.

3. **Como uma pessoa poderia utilizar essa contribuição:** O aluno cola o enunciado da questão em uma caixa de texto e recebe um mapa de estudo com os tópicos na ordem certa, o que depende do quê, onde estudar cada um e o quanto o sistema está confiante para então voltar à questão e resolvê-la por conta própria.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [X] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC. *(0.4, 0.5, 7.5 e Delimitação em 11)*
- [X] A equipe declarou se o TCC já previa interface. *(0.5)*
- [X] Se não previa, foi derivado um usuário plausível e um objetivo de uso. *(não se aplica — Caminho A; 7.2 e 7.3 explicitam perfil e objetivo)*
- [X] A interface de IHC não foi apresentada como obrigação automática do TCC. *(declaração em 7.5 e última linha de 11)*
- [X] A contribuição do TCC foi descrita sem começar por tecnologias de implementação. *(1.1 a 1.3; tecnologia só aparece em 9.3)*
- [X] Usuários diretos e stakeholders foram diferenciados. *(2.2 e 2.3, com decisão de recorte explícita)*
- [X] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente. *(2.2, 2.3 e as linhas "não" justificadas da seção 8)*
- [X] Objetivo do usuário não foi confundido com objetivo do projeto. *(3.1 revisada; 9.1 revisada)*
- [X] Processo/problema atual foi descrito antes da solução. *(seções 4 e 5, anteriores à 7)*
- [X] Existe situação concreta de uso/problema. *(4.5, explicitamente marcada como cenário hipotético)*
- [X] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados. *(5.1 a 5.6, com a tabela de dimensões em 5.3)*
- [X] Mercado/alternativas existentes foram levantados inicialmente. *(6.1 a 6.6; aprofundado na Entrega 2)*
- [X] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos. *(seção 8, agora com estado "em aberto" para o que não foi investigado)*
- [X] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la. *(coluna "Objetivo/tarefa que justificaria" na seção 8)*
- [X] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`. *(revisão sistemática de todos os `[F]` nesta versão)*
- [X] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade. *(H01–H28 e Q01–Q12 na seção 10 e em `../RASTREABILIDADE.md`)*
- [X] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre. *(um fluxo principal, cinco ações F01–F05, sem administração nem CRUD)*
- [X] A equipe consegue explicar problema humano → contribuição computacional → forma de uso. *(seção 13)*

---

# Histórico de revisões

## Revisão 1 — 16/09/2026, após feedback do professor sobre a Entrega 1

| # | Ponto do feedback | O que mudou |
|---|---|---|
| 1 | Classificação `[F]`/`[H]`/`[?]` inconsistente | Revisão sistemática de todos os `[F]`. Foram reclassificadas como hipótese ou lacuna as afirmações sobre: tutor como usuário direto (2.2), frequência e criticidade de A01/A02 (3.2, 3.3, 3.4), uso de fóruns e chatbots (4.1), dificuldade percebida do Hugging Face (4.2), a narrativa de 4.5, condições físicas (5.3), responsabilidade do tutor (5.4), necessidade de histórico (5.5), consequência do erro (5.6) e limitações de categorias inteiras de produtos (6.5). Os `[F]` mantidos passaram a indicar a origem: seção do TCC, referência bibliográfica ou data de inspeção da plataforma. |
| 2 | Problema humano misturado com solução tecnológica | 3.1 reformulada: H07 passou a descrever o objetivo do aluno (destravar e voltar a progredir); a parte "de forma visual e ancorada em fontes" virou a hipótese de design H15. 9.1 reescrita: o acesso sem Python/Hugging Face deixou de ser o benefício principal e passou a ser registrado como condição para os benefícios humanos. |
| 3 | 4.3 não respondia à pergunta | Reescrita. A resposta anterior ("saber ler e escrever") foi substituída pelo reconhecimento explícito da lacuna Q06, com a lista de sinais candidatos a investigar e o método previsto. |
| 4 | Papéis de aluno, tutor e pesquisador misturados | 2.2 ganhou a coluna "Papel no recorte de IHC" e uma decisão explícita: aluno é primário, tutor é secundário e não influencia decisões enquanto H11 não for investigada, pesquisador está fora do recorte. H04 foi restabelecida em 2.3. |
| 5 | Contexto de uso superficial e tratado como fato | 5.2 separou possibilidade técnica da Web de experiência de uso (H22, Q09). 5.3 ganhou tabela com momento, pressão de tempo, ambiente, interrupções, recursos e experiência. A distinção treino x competição virou a lacuna Q08. |
| 6 | Consequência do problema de confiança não incorporada | 3.4 ganhou a tabela que separa erro da atividade atual, erro da contribuição técnica, erro de interpretação da interface e erro de confiança, com a consequência e o destino de cada um. |
| 7 | Escopo de IHC definido apenas como "as telas" | Delimitação em 11 reescrita para o processo de interação e decisão, com a ressalva de que efeitos técnicos perceptíveis ao usuário (latência, incerteza, idioma) entram no escopo de IHC. |
| 8 | Hipóteses sem prioridade e sem caminho de investigação | Seção 10 refeita: cada linha marcada como **[CRÍTICA]**, **[SECUNDÁRIA]**, **[TÉCNICA DO TCC]** ou **[FORA DO RECORTE]**, e todo "A ser definido" substituído por método, momento e, nas hipóteses centrais, o tipo de evidência que confirmaria ou enfraqueceria a hipótese. H02 foi mantida vaga de propósito, com a justificativa registrada. |
| 9 | Alternativas tratadas como conclusões de mercado | 6.2, 6.4 e 6.5 limitadas ao que foi efetivamente observado (Codeforces e ChatGPT, com data), e as generalizações de categoria viraram H18, H26 e H28. |
| 10 | Consistência interna, checklist e rastreabilidade | H04 restabelecida e a sequência H01–H28 fechada sem saltos; a síntese passou a citar o intervalo correto; o histórico deixou de ser descartado como fato e virou Q12; o checklist foi preenchido com a referência da seção que sustenta cada item; `../RASTREABILIDADE.md` foi preenchido. |

---

## Referências

- RIBEIRO, P.; GUERREIRO, P. **Early introduction of competitive programming**. *Olympiads in Informatics*, v. 2, p. 149–162, 2008.
- SOUZA, B. V. D.; SILVESTRE, A. S. S.; LISBOA, V. H. F.; BORGES, V. R. P. **Pre-trained Language Models for Multi-Label Text Classification of Competitive Programming Problems**.
- DINU, I. G.; MIHĂESCU, M. C.; REBEDEA, T. **Domain Adaptation for Automated Tag Prediction in Competitive Programming**. In: *Artificial Intelligence Applications and Innovations (AIAI)*.
- CITTA, S.; CITTA, J. M. **Geração Automática de Trilhas de Estudo para Programação Competitiva**. Trabalho de Conclusão de Curso, Centro Universitário FEI, 2026. Arquivo `GERAÇÃO_AUTOMÁTICA_DE_TRILHAS_DE_ESTUDO_PARA_PROGRAMAÇÃO_COMPETITIVA-1.pdf` neste repositório.
- CODEFORCES TEAM. **Codeforces**. Disponível em: <https://codeforces.com/>. Acesso em: 26 ago. 2026.
- OPENAI. **ChatGPT**. Disponível em: <https://chatgpt.com/>. Acesso em: 26 ago. 2026.
