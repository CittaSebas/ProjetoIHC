# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 09/09/2026  
**Status:** 🟨 iniciada  
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
| Aluno iniciante em programação competitiva | F | É o público-alvo da aplicação, pela funcionalidade específica da aplicação. | incorporar |
| Tutor | F | É um tipo de usuário relacionado diretamente com o público-alvo da aplicação, pela sua funcionalidade específica, mas não é o público principal. | investigar |
| Pesquisador | H03 | Nenhuma | descartar |

## 1. Personas

### Persona P01 — Alfreda Marta

**Autor(a):** Sebastian Citta - 24.123.068-9  
**Tipo:** Primária
**Base de evidências:** observação  
**Hipóteses da Entrega 1 relacionadas:** {{H01, H02 ou —}}

<img width="1920" height="1080" alt="Blue Yellow Simple Empathy Map Brainstorm" src="https://github.com/user-attachments/assets/88552e37-49e4-4822-a41e-be09648231af" />

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | [18,25] |
| Ocupação/papel | Estudante de ciência da computação |
| Conhecimento do domínio | Tem conhecimento moderado em programação  |
| Experiência tecnológica | Especialista |
| Objetivos | Se destacar no curso/profissão |
| Necessidades | Estudo eficiente |
| Dores/frustrações | Conteúdo excessivo e confuso  |
| Motivadores | Conseguir um bom emprego, aprender o máximo no curso |
| Restrições/acessibilidade | Não se aplica |
| Ambiente típico de uso | Online e sozinho |
| Comportamentos relevantes | Surfa internet, utiliza LLMs no cotidiano |

**Decisões de design influenciadas por P01:**

- Que tenha um estilo "Chat" de LLM.
- Detalhamento de parágrafo e tema nos nós do grafo de conhecimento.

### Persona P02 — José Carlos Trunchado

**Autor(a):** Juan Manuel Citta - 24.123.022-6
**Tipo:** primário  
**Base de evidências:** observação   
**Hipóteses da Entrega 1 relacionadas:** {{H01, H02 ou —}}

<img width="1920" height="1080" alt="Blue Yellow Simple Empathy Map Brainstorm (1)" src="https://github.com/user-attachments/assets/3e92701e-98da-4103-9cf5-ea44ad932df1" />


| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | [30,60] |
| Ocupação/papel | Professor de faculdade |
| Conhecimento do domínio | Especialista |
| Experiência tecnológica | Extensa |
| Objetivos | Melhorar a experiência dos alunos e dele em sua aula |
| Necessidades | Ensino eficiente e correto |
| Dores/frustrações | Salas grandes são difíceis, pouco tempo para lecionar |
| Motivadores | Manter sua reputação e da escola  |
| Restrições/acessibilidade | Não se aplica |
| Ambiente típico de uso | Em sala de aula |
| Comportamentos relevantes | Gosta de se manter atualizado |

**Decisões de design influenciadas por P02:**

- Precisa ter fontes confiáveis de conhecimento
- Precisa ser simples de usar

### Síntese das personas

Explique diferenças entre os perfis e qual persona é prioritária. Evite personas duplicadas que só mudam nome/foto.

## 2. Mapa de empatia — equipe

**Persona escolhida:** P01  
**Justificativa:** Porque é o público-alvo principal da aplicação.

<img width="1920" height="1080" alt="Blue Yellow Simple Empathy Map Brainstorm" src="https://github.com/user-attachments/assets/1e8ae664-4031-4be4-ba26-183971c094ce" />


Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | Estudantes de programação competitiva | Estilo "Chat" de LLM |
| Tarefas | Saber os tópicos de uma questão | Grafo de conhecimento com detalhes em cada nó |
| Equipamentos | Computador/Notebook | Página web |
| Ambiente físico | Salas de estudo/escritório em casa | Não tem urgência na interface |
| Ambiente social/organizacional | Ambiente de estudo | Nenhum |
| Papéis/permissões/governança | Não há papéis previstos na aplicação | Nenhum |
| Volume de dados/histórico | Ainda é uma possiblidade | Possível histórico de consultas |

## 4. Jornada do usuário — equipe

**Persona:** P01  
**Objetivo da jornada:** Sanar dúvida de questão de programação competitiva  
**Início e fim da jornada:** A jornada ocorre na página web

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | Encontra uma questão que não sabe resolver | Poder resolver a pergunta | Dúvida | Quer aumentar seu conhecimento em programação competitiva | "Chat" simples apenas para receber o enunciado da questão | H |
| 1 | Encontra uma questão que não sabe resolver | Poder resolver a pergunta | Dúvida | Quer aumentar seu conhecimento em programação competitiva | "Chat" simples apenas para receber o enunciado da questão | H |
| 1 | Encontra uma questão que não sabe resolver | Poder resolver a pergunta | Dúvida | Quer aumentar seu conhecimento em programação competitiva | "Chat" simples apenas para receber o enunciado da questão | H |
> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

Quais necessidades e objetivos devem obrigatoriamente aparecer nos cenários e nas tarefas seguintes?

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
