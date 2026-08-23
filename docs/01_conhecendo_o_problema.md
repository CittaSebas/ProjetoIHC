# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 13/08/2026  
**Status:** 🟩 concluída  
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

[H] H01 - Espera-se que as trilhas de estudo geradas sejam comparáveis as trilhas apresentadas nos livros-fonte.
[H] H02 - Espera-se que a recepção da ferramenta seja positiva por parte dos usuários.

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

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Aluno iniciante em programação competitiva | Usuário direto da interface | Submeter um enunciado e usar a trilha gerada para decidir o que estudar antes de tentar resolver a questão | F |
| Tutor | Usuário direto da interface | Gerar trilhas para montar plano de treino | F |
| Pesquisador | Usa a contribuição técnica (o modelo), não a interface projetada aqui | Baixar o modelo publicado no Hugging Face, reproduzir os experimentos e analisar o processo de geração de trilhas | H03 |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Pesquisador| Consome o modelo por linha de comando ou notebook, sem passar pela interface projetada na disciplina | não | F |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] H05 - A interação com a aplicação por parte de um aluno exige que a linguagem seja compreensível para indivíduos com pouco conhecimento em termos de programação competitiva.

[H] H06 - O aluno iniciante sabe operar uma interface web sem dificuldade, mas não tem repertório para julgar se a trilha recebida está correta.

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.


[H] H07 - O usuário está tentando aprender/ensinar o conteúdo de questões de programação competitiva de forma visual e consolidada em fontes confiáveis.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Descobrir o que precisa saber para conseguir resolver uma questão | Aluno | Alta frequência / Crítico | F |
| A02 | Montar um plano de estudo/treino a partir de um conjunto de questões | Tutor | Baixa frequência / Crítico | F |

## 3.3 Qual atividade parece mais frequente? Por quê?


[H] H08 - A atividade mais frequente parece ser uma consulta feita por um aluno para descobrir os tópicos de uma determinada questão.


## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[F] F - A atividade mais crítica é a feita por um aluno resolvendo uma questão de programação competitiva. A consequência de sua mal execução seria passar o conteúdo errado e causar mais dificuldades e confusão no aluno.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

[F] F - Pelas tags do próprio juiz online. O aluno abre a lista de rótulos da questão no Codeforces e tenta inferir sozinho o que estudar.

[F] F - Por fóruns. O aluno procura a solução comentada ou discussões de outros competidores.

[F] F - O aluno cola o enunciado no ChatGPT/Claude e pede explicação.

[F] F - Hoje os usuários poderiam baixar o modelo disponibilizado no HuggingFace e rodar localmente através da linha de comando ou alguma outra interface.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[F] F - O acesso a ferramenta pode ser confuso, pois requereria conhecimento em soluções de IA, assim como encontrar o modelo no fórum HuggingFace.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[F] F - Saber ler e escrever. É uma ferramenta destinada a iniciantes de programação competitiva.

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

[F] F - A consequência de um atividade mal executada seria passar o conteúdo errado e causar mais dificuldades e confusão no aluno.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

[F] F - O aluno está treinando para uma competição de programação competitiva. O aluno chega em uma questão que não sabe por onde começar a resolvê-la, pois não conhece os tópicos necessários para tal. Ele pode tentar procurar questões similares resolvidas em fóruns de programação competitiva, ou tentar ler livros didáticos sobre o tema por sua conta. Caso não tenha sucesso ele pode desistir da competição ou da modalidade.  

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| RIBEIRO, P.; GUERREIRO, P. *Early introduction of competitive programming*. Olympiads in Informatics, v. 2, 2008 | Benefício da prática e o abismo teoria–prática quando o aluno não domina o assunto | Estudo de 2008, contexto europeu, anterior aos LLMs |
| [Codeforces](https://codeforces.com/) — inspeção direta da plataforma | Que a identificação de conteúdo é feita só por tags e que elas ficam ocultas em competição | Sem registro sistemático |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] H09 - A interação pode ocorrer com um aluno sozinho, fazendo uma consulta na ferramenta para estudo.
[H] H10 - A interação pode ocorrer com um aluno acompanhado de um tutor, fazendo uma consulta na ferramenta e contando com o apoio do tutor para dúvidas mais específicas sobre o tópico.
[H] H11 - A interação pode ocorrer com um tutor sozinho, fazendo uma consulta na ferramenta, a fim de certificar-se que a ferramenta é válida e correta.

## 5.2 Em quais dispositivos/equipamentos?

[F] F - Qualquer dispositivo com um browser e acesso a internet.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[F] F - A única condição relevante é a conexão a internet.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[F] F - Caso a ferramenta seja utilizada por tutores, é responsabilidade deles certificar-se de que ela apresenta conteúdo correto.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[F] F - Não.

## 5.6 Um erro pode produzir consequência relevante? Qual?

[F] F - O erro mais relevante seria o aluno perder seu tempo aprendendo temas não relacionados a questão.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Fórum de programação competitiva | Alunos | Para aprender a resolver questões | F |
| Modelos de IA  | Alunos e Tutores | Para auxílio no aprendizado e na tutoria | F |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

[F] F - Existem fóruns de programação competitiva e outros "Chatbots" no mercado.


## 6.3 Quais interfaces profissionais esse público já conhece?

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

[F] F - "Chatbots" e fóruns/juízes online.

## 6.4 O que essas soluções parecem fazer bem?

[F] F - Os juízes online servem como local para a comunidade praticar a modalidade.
[F] F - Os juízes online servem como repositório de questões de programação competitiva.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

| Alternativa | O que não atende | Status/evidência |
|---|---|---|
| Juízes online (Codeforces, Beecrowd, LeetCode) | A tag nomeia o tópico mas não dá ordem de estudo, pré-requisitos nem material de apoio | F |
| Fóruns | Entregam a solução pronta da questão específica. O aluno resolve aquele problema sem construir o caminho de estudo | F |
| ChatGPT, Claude (Chatbots) | Respondem em texto corrido, sem estrutura de dependência entre tópicos, sem fonte pedagógica verificável e sem indicação de incerteza | F |
| Livros e materiais didáticos consolidados | Trazem a trilha correta, porém organizada por assunto e não a partir de um enunciado concreto, o aluno travado não sabe em que capítulo procurar | F |

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

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | não | Nenhuma decisão do aluno depende de indicadores agregados nesta fase. | — |
| Configuração/parametrização | talvez | Escolher a fonte pedagógica preferida (qual livro) ou o nível de profundidade da trilha. | H14 |
| Entrada/upload/seleção de dados | sim | Colar o enunciado da questão. | F |
| Acompanhamento de processamento | sim | A inferência pode ter latência perceptível. | F |
| Relatório/resultados | sim | Trilha em grafo, a lista ordenada e a fonte de cada tópico. | F |
| Histórico com busca/filtros | não | A sessão do usuário não é uma funcionalidade prevista | - |
| Comparação de resultados | não | Comparar trilha com e sem tags não é uma atividade feita na interface | - |
| Explicabilidade/detalhamento | sim | Trilha tem que ter inforamações sobre a fonte | F |
| Administração/configurações globais | talvez | Configurar elementos visuais | F |
| Usuários/perfis/permissões | não | | - |
| CRUD de entidade do domínio | não | | — |
| Auditoria/logs | não | | - |
| Alertas/ocorrências | não |  | - |
| Ajuda/documentação | talvez | Glossário de tópicos e tags | F |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Tornar a capacidade do TCC utilizável sem conhecimento de IA, Python ou Hugging Face | Hoje o modelo só é acessível por via técnica | Aluno e tutor | F |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Submeter um enunciado colando o texto | Iniciar a consulta sem preparo técnico | alta |
| F02 | Saber que a consulta está em processamento | Não abandonar a consulta achando que travou | alta |
| F03 | Ver a trilha como grafo de tópicos com as dependências entre eles | Saber em que ordem estudar | alta |
| F04 | Abrir um tópico e ver a fonte pedagógica que o sustenta (livro/capítulo) | saber onde estudar | alta |

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| LLM Qwen3-4B-Instruct-2507 | Equilíbrio entre capacidade de inferência semântica e custo computacional | Inferência não é instantânea |
| Aplicação web dependente de conexão | Interface web prevista no TCC | Sem conexão não há consulta |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Espera-se que as trilhas de estudo geradas sejam comparáveis às trilhas apresentadas nos livros-fonte. | Se a trilha não corresponder ao que os livros ensinam, a interface estará apresentando um conteúdo sem base. | Avaliação experimental do próprio TCC |
| H02 | Espera-se que a recepção da ferramenta seja positiva por parte dos usuários. | Por que isso seria um dos pontos principais a serem avaliados da interface | A ser definido |
| H03 | Pesquisadores teriam interesse em baixar o modelo, reproduzir os experimentos e analisar o processo de geração de trilhas. | Define se esse perfil entra ou fica fora do escopo de IHC. | A ser definido |
| H05 | A interação por parte do aluno exige que a linguagem seja compreensível para quem tem pouco conhecimento de programação competitiva. | Determina o vocabulário, a rotulagem e a necessidade de glossário em toda a interface. | A ser definido |
| H06 | O aluno iniciante sabe operar uma interface web sem dificuldade, mas não tem repertório para julgar se a trilha recebida está correta. | Por que define a necessidade da trilha ser embasada e define o padrão da interface com qual ja está acostumado. | A ser definido |
| H07 | O usuário está tentando aprender/ensinar o conteúdo de questões de forma visual e consolidada em fontes confiáveis. | Sustenta apresentar a trilha como grafo com fonte por tópico, em vez de texto corrido. | A ser definido |
| H08 | A atividade mais frequente é a consulta feita por um aluno para descobrir os tópicos de uma determinada questão. | Define qual fluxo recebe prioridade de modelagem, prototipação e avaliação. | A ser definido |
| H09 | A interação pode ocorrer com um aluno sozinho, fazendo uma consulta na ferramenta para estudo. | Define o contexto de uso adotado nas personas e cenários e o quanto a interface precisa ser autoexplicativa. | A ser definido |
| H10 | A interação pode ocorrer com um aluno acompanhado de um tutor, que apoia dúvidas mais específicas sobre o tópico. | Pode gerar um segundo cenário de uso e muda o quanto a interface precisa explicar sozinha. | A ser definido |
| H11 | A interação pode ocorrer com um tutor sozinho, consultando a ferramenta para certificar-se de que ela é válida e correta. | Se sustentada, dá peso maior à explicabilidade e à indicação de fontes na interface. | A ser definido |
| H12 | A caixa de texto única com envio e resposta em fluxo de conversa é um padrão familiar a esse público. | Sustenta manter a entrada conversacional adotada | A ser definido |
| H13 | Listas de problemas com filtros por tag e dificuldade são um padrão familiar ao público, vindo dos juízes online. | Informa as convenções visuais e o vocabulário a adotar no protótipo. | A ser definido |
| H14 | O usuário teria interesse em escolher a fonte pedagógica preferida ou o nível de profundidade da trilha. | Decide se a tela de configuração/parametrização entra no escopo ou se o caso é resolvido por bons padrões, sem tela. | A ser definido |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Gerar automaticamente, a partir do enunciado de uma questão de programação competitiva, uma trilha de estudo ordenada e ancorada em materiais didáticos consolidados. |
| O TCC já previa interface? | Sim, uma interface web |
| Quem é o usuário prioritário de IHC? | Aluno iniciante em programação competitiva |
| O que ele precisa alcançar? | Descobrir o que estudar, em que ordem e em qual material, para resolver por conta própria uma questão em que travou |
| Qual problema/atividade será estudado? | A consulta feita quando o aluno trava em uma questão e não identifica os tópicos e pré-requisitos envolvidos. |
| Como isso acontece hoje? | Pelas tags do juiz online, fóruns e chatbots generalistas |
| Qual é o contexto de uso? | Treino individual, em navegador, com a questão aberta em outra aba. |
| Que interface/recorte será explorado? | Entrada conversacional com grafo de dependências entre tópicos e fonte pedagógica. |
| Como a interface se relaciona ao TCC? | É o meio da interação do usuário com a ferramenta. |
| Quais pontos ainda são hipóteses? | H01–H14 |

### Delimitação

**Dentro do escopo de IHC:** As telas da interface web que mostram o chatbot e resultado em grafo.

**Fora do escopo de IHC:** Fica de fora a parte técnica de criação do modelo que estará sendo acessado pela Interface.

**Dentro do escopo formal do TCC:** Classificação de tags, extração de caracteristicas semanticas da questão, construção da trilha de aprendizado.

**Interface da disciplina será implementada no TCC?** Provavelmente.

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

- [ ] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [ ] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [ ] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [ ] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [ ] Usuários diretos e stakeholders foram diferenciados.
- [ ] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [ ] Objetivo do usuário não foi confundido com objetivo do projeto.
- [ ] Processo/problema atual foi descrito antes da solução.
- [ ] Existe situação concreta de uso/problema.
- [ ] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [ ] Mercado/alternativas existentes foram levantados inicialmente.
- [ ] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [ ] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [ ] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [ ] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [ ] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [ ] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.