# Entrega 4 — Cenários de análise/problema

**Data:** 14/10/2002 
**Status:** 🟨 iniciada  
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

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | {{...}} | {{...}} | {{...}} |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

{{narrativa refinada}}

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | {{...}} |
| Objetivo(s) | {{...}} |
| Contexto | {{...}} |
| Recursos/informações | {{...}} |
| Ações | {{...}} |
| Problemas/rupturas | {{...}} |
| Consequências | {{...}} |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
