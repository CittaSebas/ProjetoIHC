# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 09/09/2026 — revisada em 14/10/2026
**Status:** 🟨 em andamento — faltam os arquivos de imagem em `assets/03_personas/` (ver pendências na seção 1)
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| Aluno iniciante em programação competitiva | [F] como público-alvo; [?] Q02 quanto ao que "iniciante" significa | Público-alvo declarado na Seção II do TCC. **Nenhum dado sobre pessoas reais desse perfil.** | incorporar como **proto-persona primária** (P01), mantendo Q02 aberta |
| Tutor / treinador | [H] H11 — a equipe não tem evidência de que tutores usariam a ferramenta | Nenhuma. A Entrega 1 decidiu que o tutor **não influencia decisões de interface** enquanto H11 não for investigada | incorporar como **proto-persona secundária** (P02), sem poder de decisão sobre a interface |
| Pesquisador | [H] H03, H04 | Nenhuma | **descartar** — consome o artefato técnico do TCC, não a interface. Fora do recorte de IHC |

## 1. Personas

### Persona P01 — Alfreda Marta

**Autor(a):** Sebastian Citta — 24.123.068-9
**Tipo:** **primária** — é a persona que dirige as decisões de design do semestre
**Base de evidências:** **proto-persona** — construída a partir do público-alvo declarado no TCC e das hipóteses da Entrega 1. Nenhuma observação, entrevista ou questionário foi realizado.
**Hipóteses da Entrega 1 relacionadas:** H06, H07, H08, H09, H12, H17, H19, H21, H22, H23, H24 — e as lacunas Q02, Q06, Q08, Q09, Q12

<img width="1920" height="1080" alt="Proto-persona P01 — Alfreda Marta" src="assets/03_personas/MapaEmpatiaMulher" />


| Campo | Descrição | Status |
|---|---|---|
| Faixa etária / contexto relevante | 18 a 25 anos, graduação em andamento | [H] |
| Ocupação/papel | Estudante de Ciência da Computação | [H] |
| **Conhecimento de programação** | Moderado — já programa, conhece estruturas básicas e resolve questões fáceis sem ajuda | [H] |
| **Conhecimento do domínio (programação competitiva)** | **Baixo** — não reconhece pelo enunciado qual técnica algorítmica a questão exige, nem conhece os pré-requisitos de cada tópico | [H] H06 — *esta é a distinção que define a persona: saber programar não é saber programação competitiva* |
| Familiaridade com algoritmos | Conhece nomes de tópicos que já viu em disciplina; não domina os que ainda não estudou | [?] Q02 |
| Experiência com juízes online | Já submete soluções no Codeforces e entende o veredito | [H] H17 |
| Vocabulário | Lê inglês técnico, mas não necessariamente associa `dp`, `greedy` ou `constructive algorithms` a um conteúdo que saiba estudar | [?] Q02, [H] H05 |
| Experiência tecnológica | Alta — opera interfaces web sem dificuldade e usa LLMs no cotidiano | [H] H06, H19 |
| Objetivos | Destacar-se no curso e na profissão; progredir no treino de programação competitiva | [H] |
| Necessidades | Descobrir **o que lhe falta saber** para resolver a questão em que travou, sem receber a solução pronta | [H] H07 |
| Dores/frustrações | Trava numa questão e não sabe nem o nome do que precisa procurar; perde tempo de treino tentando por eliminação | [H] H21 — *é a dor, não o desejo de aprender* |
| Motivadores | Conseguir um bom emprego, aproveitar o curso, não ficar para trás da equipe | [H] |
| Restrições/acessibilidade | **Não investigado** — a equipe não sabe se há necessidade de contraste, navegação por teclado, leitor de tela ou alternativa textual a uma representação gráfica | [?] Q03 — *a versão anterior registrava "não se aplica", o que afirmava a ausência de uma necessidade sem tê-la verificado* |
| Dispositivo | Notebook ou desktop, porque o enunciado está em outra aba e o código na mesma máquina | [H] H22, [?] Q09 |
| Ambiente típico de uso | Treino individual, sozinho, sem tutor presente | [H] H09; [?] Q08 — se competição entra no contexto, ainda não foi decidido |
| Comportamentos relevantes | Alterna entre enunciado, editor de código e ferramenta de consulta; sofre interrupções | [H] H24 |
| Estado em que chega ao sistema | **Já travado e já frustrado**, durante ou logo após uma tentativa que falhou | [H] H23 — *condiciona o que precisa estar visível na primeira tela* |

**Necessidades que P01 impõe ao projeto:**

| # | Necessidade da persona | Hipótese/lacuna que a sustenta | Consequência para o design |
|---|---|---|---|
| N01 | Começar a consulta sem precisar decidir nada antes, porque ela chega travada e sem repertório para escolher opções | H23, Q15 | A ação inicial precisa ser única — sustenta F01 e RC01 da Entrega 2 |
| N02 | Saber o que estudar **em que ordem**, não apenas quais são os assuntos | H07; [F] lacuna declarada na Seção VII.C do TCC | Sustenta F03 e a hipótese de design H15 |
| N03 | Chegar ao material de estudo sem já saber o nome do assunto | H26 | Sustenta F04 — e explica por que o padrão de filtro por tag do Codeforces **não** serve (H13) |
| N04 | Conseguir avaliar o quanto confiar no que recebeu, sem ter repertório para julgar o conteúdo | H06; [F] F1 Macro de 0,5820 (Seção VII.B do TCC) | Sustenta F05 — explicabilidade e sinalização de incerteza |
| N05 | Entender os termos da resposta, que chegam em jargão e em inglês | H05, Q02, Q06 | Mantém a ajuda contextual/glossário `em aberto`, e RC03 como provisória |
| N06 | Não ficar sem saber se o sistema está trabalhando, dada a latência do modelo | [F] latência do LLM (Entrega 1, 9.3) | Sustenta F02 |

### Persona P02 — José Carlos Trunchado

**Autor(a):** Juan Manuel Citta — 24.123.022-6
**Tipo:** **secundária** — registrada no mapa de perfis, mas **não dirige decisões de interface** nesta disciplina
**Base de evidências:** **proto-persona** — nenhuma conversa com professores ou treinadores foi realizada
**Hipóteses da Entrega 1 relacionadas:** H10, H11, H25 — e as lacunas Q01, Q11

<img width="1920" height="1080" alt="Proto-persona P02 — José Carlos Trunchado" src=assets/03_personas/MapaEmpatiaHomem.png />

| Campo | Descrição | Status |
|---|---|---|
| Faixa etária / contexto relevante | 30 a 60 anos | [H] |
| Ocupação/papel | Professor de faculdade; eventualmente treinador de equipe de maratona | [H] H11 |
| Conhecimento do domínio | Especialista — reconhece a técnica exigida lendo o enunciado | [H] |
| Experiência tecnológica | Extensa | [H] |
| Objetivos | Melhorar a experiência de aprendizagem dos alunos e o aproveitamento da própria aula | [H] |
| Necessidades | Ensino eficiente e **correto**; confiar no material antes de repassá-lo | [H] H25 |
| Dores/frustrações | Turmas grandes, pouco tempo de aula, dificuldade de atender individualmente quem travou | [H] |
| Motivadores | Reputação própria e da instituição; resultado dos alunos | [H] |
| Restrições/acessibilidade | Não investigado | [?] Q03 |
| Ambiente típico de uso | Sala de aula e preparação de treino | [H] — **contexto diferente do adotado no recorte** (H09: aluno sozinho, treino individual) |
| Comportamentos relevantes | Procura se manter atualizado; verifica fontes | [H] H25 |

**Por que P02 é secundária.** A Entrega 1, seção 2.2, decidiu que o tutor permanece no mapa de stakeholders mas **não influencia decisões de interface enquanto H11 não for investigada**. Três razões concretas:

1. **Não há evidência de que exista esse uso.** H11 ("tutores usariam a ferramenta para montar planos de treino e validar conteúdo") nunca foi verificada — a equipe não conversou com nenhum professor ou treinador.
2. **O contexto não é o mesmo.** P02 usaria a ferramenta em sala de aula ou em preparação de treino; o recorte adotado é o aluno sozinho, já travado, em treino individual (H09, H23). São momentos, pressões e necessidades diferentes.
3. **O conhecimento de domínio é oposto.** P01 não consegue julgar se a trilha está correta (H06); P02 consegue, e é justamente o que ele faria. Projetar para os dois ao mesmo tempo é o "usuário elástico": a mesma tela teria de explicar tudo para quem não sabe nada e não atrapalhar quem sabe tudo.

**O que P02 exigiria *se* H11 fosse sustentada** — registrado para rastreabilidade, **não aplicado agora**:

| Exigência | Hipótese | Observação |
|---|---|---|
| Fontes pedagógicas verificáveis por tópico | H25 | **Converge com N03/N04 de P01** — é a única exigência de P02 que já está no escopo, mas entra pelo aluno, não pelo professor |
| Verificar rapidamente várias questões em sequência | H11, H14 | Fora do escopo: o fluxo adotado é consulta individual |
| Exportar ou compartilhar uma trilha com a turma | [?] Q11 | Fora do escopo; nenhuma tarefa do aluno justifica |

### Síntese das personas

| | P01 — Alfreda Marta | P02 — José Carlos Trunchado |
|---|---|---|
| Papel | **Primária** | Secundária |
| Conhecimento do domínio | **Baixo** — não reconhece a técnica pelo enunciado | Alto — reconhece e valida |
| Objetivo | Destravar e voltar a progredir no próprio treino | Melhorar o aprendizado de uma turma |
| Relação com o resultado da ferramenta | **Consome e não consegue auditar** (H06) | Audita antes de repassar (H25) |
| Contexto | Sozinha, travada, em treino individual | Sala de aula ou preparação de treino |
| Pressão | Tempo de treino perdido | Tempo de aula e tamanho da turma |
| Influencia o design nesta disciplina? | **Sim, integralmente** | **Não**, até H11 ser investigada |

**As personas não são variações demográficas da mesma pessoa.** A diferença decisiva não é idade nem ocupação: é **a capacidade de julgar o resultado do sistema**. P01 recebe uma trilha e não tem como saber se ela está certa; P02 recebe a mesma trilha e detecta o erro imediatamente. Isso produz requisitos opostos — P01 precisa de explicação, fonte e sinalização de incerteza; P02 precisaria de densidade e velocidade.

**Persona prioritária: P01.** Pelo público-alvo declarado no TCC (Seção II), por ser o perfil com evidência documental de existência, por ser acessível à equipe para as Entregas 7 e 14, e por concentrar a tensão de IHC do projeto — alta competência tecnológica combinada com baixa competência de domínio.

[?] Q02 — Enquanto não se souber o que "iniciante" significa concretamente neste domínio, P01 permanece uma aposta. Um aluno de primeiro ano e um competidor de terceiro ano têm repertórios muito diferentes, e a persona atual pode estar descrevendo um ponto médio que não existe.

## 2. Mapa de empatia — equipe

**Persona escolhida:** P01
**Justificativa:** é a persona primária e o público-alvo declarado do TCC.

<img width="1920" height="1080" alt="Mapa de empatia — P01" src=assets/03_personas/MapaEmpatiaMulher.png />

| Quadrante | Conteúdo | Status |
|---|---|---|
| **O que vê** | O enunciado da questão, com uma narrativa que não indica a técnica necessária | [F] formato observado no Codeforces, 26/08/2026 |
| | Tags da questão — quando visíveis; em competição ficam ocultas | [F] Seções I e IV.A do TCC |
| | O *rating* de dificuldade e quantas pessoas resolveram | [F] observado em C01-2 (Entrega 2) |
| | Colegas de equipe resolvendo questões que ela não resolve | [H] |
| **O que ouve** | "Isso é só DP", "é um problema clássico de grafos" — explicações que pressupõem o conhecimento que ela não tem | [H] |
| | Recomendações genéricas de "resolver mais questões" | [H] |
| **O que diz e faz** | Relê o enunciado várias vezes procurando uma palavra que reconheça | [H] H17 |
| | Procura a questão em fóruns e editoriais | [H] H18 |
| | Cola o enunciado num chatbot e pede explicação | [H] H19 |
| | Abre um livro didático e não sabe em que capítulo procurar | [H] H26 |
| | Alterna entre enunciado, editor e aba de consulta | [H] H24 |
| **O que pensa e sente** | "Não sei nem o que pesquisar" | [H] H21 |
| | Insegurança sobre a própria capacidade, não necessariamente sobre o conteúdo | [H] |
| | Pressa: o tempo de treino está passando | [H] H23; [?] Q08 em competição |
| | Aceita a primeira explicação plausível, por não ter como contestá-la | [H] H06 |
| **Dores** | Não conhecer o nome do que precisa aprender — a busca vira tentativa e erro | [H] H21 |
| | Investir tempo num tópico que não a aproxima da solução | [H] H21 |
| | Receber a solução pronta e destravar a questão sem aprender o caminho | [H] H18 |
| | Não ter como saber se a orientação recebida está correta | [H] H06; [F] o modelo erra com frequência mensurável (F1 Macro 0,5820) |
| **Ganhos** | Sair da consulta sabendo qual é o próximo passo concreto de estudo | [H] H07 |
| | Chegar ao material certo sem já saber o nome do assunto | [H] H26 |
| | Resolver a questão **por conta própria** depois de estudar | [H] H07 |
| | Perceber que está construindo repertório, e não só fechando questões | [H] |

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Status | Implicação de design |
|---|---|---|---|
| Usuários | Aluno iniciante em programação competitiva (P01). Tutor (P02) registrado, sem influência nas decisões | [F] público-alvo do TCC; [?] Q02 quanto ao perfil concreto | Toda decisão de linguagem e explicação é calibrada para baixo conhecimento de domínio |
| Tarefas | A01 — descobrir o que precisa saber para resolver uma questão em que travou | [F] a atividade existe; [H] H08 quanto à frequência | Fluxo único e principal; sem exploração de acervo |
| Equipamentos | Notebook ou desktop, com o enunciado em outra aba | [H] H22; [?] Q09 | Condiciona a viabilidade de uma representação gráfica das dependências (H15). **Se o uso em celular for relevante, o formato precisa mudar** |
| Ambiente físico | Casa, laboratório da faculdade ou sala de treino | [?] Q10 | Nenhuma implicação derivada enquanto a lacuna estiver aberta |
| Momento e estado | O aluno chega **já travado e frustrado**, durante ou após uma tentativa que falhou | [H] H23 | A primeira tela precisa aceitar a questão imediatamente, sem etapa de configuração (N01) |
| Pressão de tempo | Em treino, moderada — o tempo de treino é finito. Em competição, severa | [H] H23; [?] Q08 | Não tem urgência na interface. A competição não será o foco principal da interface no momento. |
| Interrupções e paralelismo | Alterna entre enunciado, editor de código e ferramenta de consulta | [H] H24 | Reforça o argumento para retomada de contexto e para o histórico (Q12) |
| Ambiente social/organizacional | Estudo individual, sem tutor presente | [H] H09 | A interface precisa ser autoexplicativa: possivelmente o aluno esteja sozinho |
| | Pode existir equipe de maratona com treinador | [?] Q11 | Nenhuma consequência adotada |
| Papéis/permissões/governança | Nenhum papel previsto no recorte adotado | [F] decorre de H09 | Sem login, perfis ou permissões — ver Entrega 1, seção 8 |
| Acessibilidade | **Não investigado** | [?] Q03 | Requisitos serão definidos na Entrega 8. Uma alternativa textual à representação gráfica já se desenha como provável necessidade |
| Volume de dados/histórico | Uma trilha é consumida ao longo de dias, não de uma sessão | [?] Q12 | Histórico `em aberto` — a decisão virá da necessidade do usuário |
| Conexão | Necessária; sem conexão não há consulta | [F] arquitetura web | Reforça o valor de poder recuperar o que já foi obtido (Q12) |
| Idioma | O modelo foi treinado sobre enunciados em inglês e devolve tópicos em inglês | [F] Seção VII.A do TCC | Possível barreira de vocabulário (H05, N05); mantém RC03 provisória |

## 4. Jornada do usuário — equipe

**Persona:** P01 — Alfreda Marta
**Objetivo da jornada:** resolver, por conta própria, uma questão de programação competitiva em que travou
**Início e fim da jornada:** começa **antes** do contato com a ferramenta, no momento em que ela escolhe a questão e tenta resolvê-la; termina **depois**, quando ela retorna à questão tendo estudado — ou desiste dela.

| Etapa | Fase | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|---|
| 1 | antes | Escolhe uma questão para treinar, pela dificuldade ou pela lista da competição | Progredir no treino | Confiança, expectativa | — | — | [H] |
| 2 | antes | Lê o enunciado e tenta identificar a abordagem | Entender o que a questão pede | Concentração | A narrativa do enunciado não indica a técnica necessária | — | [F] formato observado no Codeforces |
| 3 | antes | Tenta resolver e falha, ou não consegue nem começar | Resolver | Dúvida, depois frustração | Não sabe se o problema é a lógica ou um conteúdo que desconhece | — | [H] |
| 4 | antes | **Percebe que está travada** e que não vai sair sozinha | Decidir o que fazer | Frustração, urgência | Não existe um sinal claro de "você está travada por falta de conteúdo X" | É aqui que a necessidade do produto nasce | [?] **Q16 — não sabemos quando nem como ela percebe isso, nem quanto tempo passa antes** |
| 5 | antes | Decide buscar ajuda externa e escolhe onde: tags, editorial, fórum ou chatbot | Encontrar orientação | Esperança misturada com receio de ver a solução | Cada caminho tem um custo: a tag não ensina, o editorial entrega a resposta, o chatbot não cita fonte | Ser uma opção melhor que as três — orientação sem espoiler | [H] H17, H18, H19 |
| 6 | antes | Procura o assunto num livro e não sabe em que capítulo | Estudar o conteúdo certo | Desorientação | O material é organizado por assunto, e ela não sabe o nome do assunto | Ligar cada tópico a uma fonte específica (N03) | [H] H26 |
| 7 | **durante** | Apresenta a questão ao sistema | Iniciar a consulta | Alívio por haver um caminho simples | Qualquer decisão pedida aqui é uma decisão que ela não tem informação para tomar | Ação inicial única, sem configuração prévia (N01) | [H] H23; [?] Q15 |
| 8 | durante | Aguarda o processamento | Saber que está funcionando | Impaciência — ela já estava frustrada antes de chegar | Sem retorno, não distingue "processando" de "travou" | Feedback de estado (N06) | [F] latência do LLM (Entrega 1, 9.3) |
| 9 | durante | Recebe a trilha e tenta entendê-la | Saber o que estudar e em que ordem | Expectativa, depois possível sobrecarga | Uma lista de tópicos sem ordem nem relação não diz por onde começar | Tornar visível a dependência entre tópicos (N02) | [F] lacuna declarada na Seção VII.C do TCC; [H] H15 |
| 10 | durante | Encontra termos que não reconhece | Compreender o que foi indicado | Insegurança | Jargão em inglês para quem por definição ainda não domina o assunto | Ajuda contextual — `em aberto` (N05) | [H] H05; [F] rótulos em inglês (Tabela II do TCC) |
| 11 | durante | **Tenta avaliar se pode confiar na trilha** | Não perder tempo com orientação errada | Dúvida que ela não consegue resolver | Não tem repertório para contestar; tende a aceitar a primeira explicação plausível | Explicabilidade, fonte e sinalização de incerteza (N04) | [H] H06; [F] F1 Macro 0,5820 e alucinação registrada |
| 12 | durante | Decide por onde começar | Ter um próximo passo concreto | Alívio ou ainda dúvida | — | O resultado da consulta precisa terminar numa ação, não numa lista | [H] H07 |
| 13 | **depois** | Estuda o tópico no material indicado | Adquirir o conhecimento que faltava | Esforço, progresso | O material pode ser mais extenso do que o tempo disponível | Indicar o recorte do material, não só o livro | [H] H26 |
| 14 | depois | Volta à questão e tenta de novo | Resolver por conta própria | Determinação | Não sabe se já estudou o suficiente para tentar novamente | — | [?] **Q17 — não sabemos como ela decide que já sabe o bastante para voltar** |
| 15 | depois | **Caso resolva:** confirma que o caminho funcionou | Confiar na ferramenta na próxima vez | Satisfação, confiança | — | É o momento que constrói adoção | [H] |
| 16 | depois | **Caso não resolva:** reavalia se o problema era o conteúdo indicado ou a própria execução | Entender o que faltou | Desânimo | Pode concluir que é incapaz, quando a trilha estava errada | Permitir voltar e questionar a orientação recebida | [H] H06, H21; [?] Q07 |
| 17 | depois | Dias depois, retoma o estudo do mesmo assunto | Continuar a trilha | — | Se fechou a aba, perdeu o resultado e precisa reprocessar | Histórico — `em aberto` | [?] Q12 |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

**O que a jornada revelou:**

- **Das 17 etapas, 6 são "antes" do contato com a ferramenta** — e é onde estão as duas lacunas novas (Q16, Q17) e a principal lacuna do projeto (Q06). O produto só é útil se a etapa 4 for bem compreendida.
- **A etapa 11 é o ponto crítico.** É onde H06 e o F1 Macro de 0,5820 se encontram: o sistema erra com frequência conhecida e a usuária não tem como perceber. Nenhuma outra etapa concentra tanto risco.
- **A etapa 16 é a consequência real do erro**, e não "perder tempo": a aluna pode atribuir a si mesma uma falha que foi do sistema.

## Síntese

**Necessidades e objetivos que devem obrigatoriamente aparecer nos cenários (Entrega 4) e nas tarefas (Entrega 5):**

1. **O objetivo é destravar e voltar a resolver por conta própria** (H07, N02) — não "receber uma lista de tópicos" nem "usar o modelo". Um cenário que termine na entrega da trilha está incompleto: precisa ir até a etapa 14.
2. **A tarefa não começa em "colar o enunciado"** (etapas 1 a 6). A decomposição da Entrega 5 precisa incluir o que acontece antes do contato com o sistema, ou vai modelar a interface em vez da atividade.
3. **A incapacidade de julgar o resultado é a característica definidora da persona** (H06, etapa 11, N04). Qualquer cenário ou tarefa que suponha uma usuária capaz de validar a trilha está descrevendo P02, não P01.
4. **O estado de entrada é "já travada e frustrada"** (H23, N01), não neutro. Isso muda o que pode ser pedido dela na primeira interação.
5. **A ordem e a dependência entre tópicos são a necessidade, não o formato** (N02). Grafo é a hipótese H15 de como atendê-la, a testar na Entrega 6.
6. **A fonte pedagógica por tópico resolve uma dor específica** (N03, H26): ela não sabe o nome do assunto, logo não sabe onde procurar.
7. **O vocabulário é um obstáculo em si** (N05, H05, Q02), não um detalhe de redação.

## Checklist

- [X] Existe pelo menos uma persona por integrante. *(P01 — Sebastian Citta; P02 — Juan Manuel Citta)*
- [X] As personas não são apenas diferenças demográficas superficiais. *(a diferença decisiva é a capacidade de auditar o resultado do sistema — ver Síntese das personas)*
- [X] Está claro o que é dado real e o que é hipótese/proto-persona. *(aviso no início, campo "Base de evidências" e coluna "Status" em todas as tabelas)*
- [X] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência. *(Q02 permanece aberta e registrada como limite da persona)*
- [X] Objetivos e dores têm consequência para o design. *(tabela N01–N06, com a hipótese que sustenta cada necessidade)*
- [X] Contexto de uso está coerente com a Entrega 1. *(seção 3 realinhada às hipóteses H09, H22, H23, H24 e às lacunas Q03, Q08, Q09, Q10, Q12)*
- [X] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica. *(não se aplica — o TCC prevê interface; ainda assim N02 e N04 derivam de lacunas e métricas declaradas no TCC)*
- [X] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes. *(pesquisador descartado; tutor mantido como secundário e sem influência, com as três razões registradas)*
- [X] Jornada possui etapas, dores e oportunidades e não é apenas wireflow. *(17 etapas em antes/durante/depois, com 6 anteriores ao contato com o sistema)*
- [X] IDs das personas foram adicionados à rastreabilidade. *(P01 na coluna Persona das linhas R01–R05, seção 3; a reclassificação de P02 registrada na seção 5)*
- [ ] Artefatos visuais salvos em `assets/03_personas/`. — **pendente: as três imagens continuam hospedadas externamente e os arquivos locais são placeholders do template**

---

# Histórico de revisões

## Revisão 1 — 14/10/2026

Revisão motivada pela leitura cruzada com a Entrega 1 revisada e com os dois feedbacks do professor, que já havia apontado os mesmos padrões de erro nas entregas anteriores.

| # | Problema | O que mudou |
|---|---|---|
| 1 | "Base de evidências: observação" nas duas personas, sem que houvesse observação | Ambas passaram a **proto-persona**, com aviso explícito no início da entrega de que nenhum dado foi coletado com usuários |
| 2 | P02 marcada como primária, sendo um professor em sala de aula | **P02 passou a secundária**, com as três razões registradas (ausência de evidência para H11, contexto diferente do adotado, conhecimento de domínio oposto). Suas exigências foram registradas como condicionais a H11 e **não aplicadas** |
| 3 | P01 contradizia H06 ao declarar conhecimento de domínio "moderado" | O campo foi desdobrado em **conhecimento de programação** (moderado) e **conhecimento do domínio — programação competitiva** (baixo), que é a distinção que define a persona |
| 4 | Campos exigidos pelo feedback ausentes em P01 | Acrescentados familiaridade com algoritmos, experiência com juízes online, vocabulário, dispositivo e estado de entrada |
| 5 | "Restrições/acessibilidade: não se aplica" | Trocado por `[?]` Q03 nas duas personas — a ausência da necessidade nunca foi verificada |
| 6 | Decisão de design derivada da solução ("que tenha um estilo Chat de LLM") | Substituída pela tabela de necessidades N01–N06, cada uma com a hipótese que a sustenta. Chat e grafo voltaram a ser as hipóteses de design H12 e H15, a testar na Entrega 6 |
| 7 | Hipóteses relacionadas em branco (`{{...}}`) | Preenchidas nas duas personas |
| 8 | Síntese das personas vazia | Escrita, com tabela comparativa, a justificativa da prioridade e o limite imposto por Q02 |
| 9 | Mapa de empatia só como imagem | Documentado em texto nos seis quadrantes, com status por linha e a ressalva de que "o que vê" lista o que está na tela, não o que ela usa (Q06) |
| 10 | Contexto de uso afirmado como fato e mais raso que a Entrega 1 | Realinhado: acrescentados momento e estado, pressão de tempo, interrupções, idioma e conexão; "não tem urgência" foi qualificado; ambiente virou Q10 |
| 11 | Jornada com uma única etapa repetida três vezes | Reconstruída com 17 etapas em antes/durante/depois. Surgiram duas lacunas novas: **Q16** (como percebe que travou) e **Q17** (como decide que já estudou o suficiente) |
| 12 | Síntese final vazia | Escrita como sete necessidades obrigatórias para as Entregas 4 e 5, mais a lista de lacunas a fechar antes da Entrega 5 |
| 13 | Checklist desmarcado | Preenchido com a referência que sustenta cada item. Acrescentado um item sobre os artefatos locais, **desmarcado** porque a pendência é real |
| 14 | Personas ausentes da rastreabilidade | P01 e P02 registradas em `../RASTREABILIDADE.md` |
