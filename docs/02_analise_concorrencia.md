# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026  
**Status:** 🟨 iniciada  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.


## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

> **Concorrente não precisa ser idêntico ao produto.** Pode atuar na mesma área, resolver objetivo semelhante ou disputar a mesma necessidade. Quando não houver concorrente direto, use produtos análogos e softwares que o público já utiliza.

### Para TCCs que não previam interface

Não procure apenas um “concorrente do algoritmo”. Investigue **interfaces profissionais que materializam atividades semelhantes** às que o usuário escolhido precisaria realizar.

Exemplos:

- TCC de banco de dados → consoles de administração, ferramentas para DBA, monitoramento e análise de consultas;
- TCC de LLM/ML → painéis de experimentos, gestão de modelos/datasets, comparação de métricas, revisão de resultados;
- TCC de análise de dados → dashboards, ferramentas de BI, filtros, relatórios e exploração;
- TCC de infraestrutura/API → portais administrativos, observabilidade, logs, gestão de credenciais e uso;
- TCC de cibersegurança → consoles de alertas, triagem, histórico e auditoria.

A pergunta é: **“que convenções esse perfil já conhece para executar tarefas equivalentes?”**

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Fórum de programação competitiva | ferramenta cotidiana | Porque é uma das formas tradicionais de aprender programação competitiva, com ajuda da comunidade e de colegas com mais experiência | F | analisar |
| Modelos de IA | ferramenta cotidiana | Por se tratar de uma ferramenta que pode ser usada para o aprendizado autônomo e pode ajudar a destrinchar conteúdo de livros didáticos | F | analisar |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

Alunos de programação competitiva

## 2. Concorrentes diretos/indiretos

### Análise C01 — Fórum de programação competitiva 

**Autor(a):**  Juan Manuel Citta 24.123.022-6
**Tipo:** indireto  
**Link oficial:** [https://codeforces.com/](https://codeforces.com/) <br>
**Data de acesso:** 26/08/2026

### Análise C02 — Modelos de IA

**Autor(a):** Sebastian Citta 24.123.068-9  
**Tipo:** direto 
**Link oficial:** [ChatGPT](https://chatgpt.com/) <br>
**Data de acesso:** 26/08/2026

#### Contexto e proposta

C01 - É uma plataforma para praticar programação competitiva. Nela o usuário pode procurar questões, subir suas tentativas e recebe aprovação ou reprovação da tentativa, com uma análise do erro identificado, como o tempo límite estourado. Além de poder praticar, o usuário também pode interagir com a comunidade através de posts, no estilo de fórum com tópicos e pode procurar por questões ou competições inteiras já resolvidas.

C02 - É uma plataforma Web para acessar um modelo LLM generalista, onde o usuário pode fazer perguntas, subir arquivos (com límite de tamanho dependendo da assinatura) para receber uma resposta. A proposta do produto é ser uma ferramenta de assistência geral.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| C01-  Acessar fórum para fazer perguntas | Clickando na aba "Catalog" na Home do site | <img width="1223" height="898" alt="image" src="https://github.com/user-attachments/assets/5d521552-7d11-4280-bdd7-0cb57384b35e" />| É no modelo fórum tradicional |
 | C01 - Acessar lista de problemas | Clickando na aba "ProblemSet" na Home do site | <img width="1263" height="902" alt="image" src="https://github.com/user-attachments/assets/dcc28068-dddc-4d49-b847-b790b065c06d" />| É uma tabela com as informações relevantes |
 | C01 - Acessar lista de competições | Clickando na aba "Contests" na Home do site | <img width="1255" height="907" alt="image" src="https://github.com/user-attachments/assets/0804ef2f-a134-48bd-84b3-f9ac04d72ada" />| É uma lista filtrável de competições antigas e atualmente ativas |
 | C02 - Fazer prompt ou subir arquivos | Clickando na caixa texto ou no ícone de soma | <img width="1916" height="911" alt="image" src="https://github.com/user-attachments/assets/20ca14c9-24cc-494d-95aa-6a4d0a7d0bad" />| É uma interface simples com apenas duas opções de input e alguns botões de configuração e assinatura |

#### Experiência do usuário e opiniões

Use avaliações públicas, relatos, estudos, testes próprios ou outra fonte identificável. Não trate opinião isolada como verdade universal.

#### Preço/modelo de negócio

C01 - Grátis. É um fórum com patrocínio da fundação TON (The Open Network).
C02 - Modelo de subscrição. Tem plano grátis com um acesso de base limitado e tem opções de subscrições com acesso maior (mais tokens) e a outras funcionalidades como modelos LLM mais potentes.  

#### Padrões e tendências percebidos

C01 - Fóruns de programação competitiva em sua maioria, tem interface mais antiga, por se tratarem de sites com mais tempo no mercado. Além disso, a funcionalidade principal da página é o de fórum de posts, onde usuários interagem comentando em postagens feitas.

C02 - LLMs em sua maioria usam a interface no modelo chat. A maioria deles tem uma interface moderna com visuais limpos e sem muito conteúdo. A maioria dos serviços (Deepseek, Claude, Gemini) parecidos com o ChatGPT seguem o mesmo padrão. 

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| C01 - Interface antiga | Como vísivel nos prints a interface do CodeForces segue um estilo antigo de fórum clássico  | Alunos mais jovens podem não estar acostumados ou não ter preferência pela interface, por isso o nosso projeto buscará manter um visual moderno |
| C01 - Excesso de opções | Como vísivel no print da Home Page a interface do CodeForces apresenta muitas opções com pouca ligação entre eles  | No nosso projeto iremos procurar deixar opções parecidas em "compartimentos" para manter uma interface limpa e sem ser sobrecarregada de informações |
| C01 - Filtros completos | Como vísivel nos prints da página Contests e da página Problem Set, a interface do CodeForces permite a filtragem avançada das informações da tela  | Pessoas com conhecimento prévio da página tem um alto controle da informação mostrada na tela. No nosso projeto podemos adicionar filtragem avançada nos grafos de conhecimento. |
| C02 - Interface simples | Como vísivel no print da Home Page a interface do ChatGPT apresenta uma quantidade baixa de opções, com pouco ruído na tela  | No projeto planejamos fazer uma interface simples e parecida com o padrão vísivel dos diferentes proveedores de LLMs do mercado, que tem aparência similar. |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| CodeForces | Para procurar perguntas e repostas de programação competitiva | Estilo fórum | {{link local}} | A abundância de informações e filtros é algo positivo da ferramenta, mesmo requerendo mais uso da ferramenta para masterizar |
| Stackoverflow | Para fazer perguntas de programação em geral | Estilo fórum | <img width="1265" height="904" alt="image" src="https://github.com/user-attachments/assets/6896c782-2386-4a4c-85da-21bdb5e0a986" />| O formato de post/comentários é prevalente nos usuários de programação |
| ChatGPT | Complementar ao Stackoverflow para receber respostas a perguntas especifícas | Chat | <img width="1507" height="711" alt="image" src="https://github.com/user-attachments/assets/4e28b680-68c7-4237-a819-42a8e634f951" />| O público-alvo prefere o foco da tela ser o conteúdo sendo editado |
| Visual Studio Code e outras IDEs | Para escrever código | Espaço de trabalho claro no centro. Altamente customizável | <img width="1191" height="794" alt="image" src="https://github.com/user-attachments/assets/19576140-d69b-4b12-9cee-0a4e660f7130" />| O público-alvo está acostumado com ferramentas customisáveis e com aparência mais complexa no início |
 | Github | Para versionamento e compartilhamento do código | Feed com atualizações gerais da plataforma e de mudanças em repositórios de contatos | <img width="1890" height="856" alt="image" src="https://github.com/user-attachments/assets/fa80e2e2-0f00-4aad-8dee-d81703e136d4" />| Público alvo está acostumado com feed de noticias e abundante quantidade de opções na página inicial |

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| dashboard | ChatGPT | Garante o acesso a ferramenta | Permite customização | Pode sobrecarregar usuário | talvez |
| histórico + filtros | CodeForces, StackOverflow, Github | Para rever questões/perguntas antigas | Melhora a usabilidade recorrente da ferramenta | Perder histórico e requer DB | não |
| administração/CRUD | Todos | Atrelar configurações/subscrições/postagens a um usuário | Customização da ferramenta | Requer um DB | talvez |

> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 | C02 | Oportunidade para o projeto |
|---|---|---|---|---|
| Navegação | Sobrecarregada de opções | Pouca navegação, apenas para opções | Manter o padrão da ferramenta mais parecida, pois terá as funcionalidades parecidas (ChatGPT) |  
| Feedback/estado | Não tem | Mostra erros e mensagens de estado no processamento | O projeto tem a necessidade de fornecer feedback ao usuário |  
| Prevenção/recuperação de erro | Não tem | Permite reenviar mensagens | Utilizar recuperação de erro para melhorar usabilidade |  
| Terminologia | Repleto de terminologia de programação competitiva de diferentes niveís | Apenas linguagem simples | É importante manter um balanço entre terminologia da modalidade e manter a resposta intelegível para todos os usuários |  
| Acessibilidade | Não tem | Tem entrada por voz | Pode ser considerado para o projeto em estágios mais avançados |  
| Eficiência | Requer uso recorrente para se acostumar, porém tem muita informação escondida atrás de filtros e navegação | É muito simples para o usuário médio acessar todas as funcionalidades | O escopo do projeto se encaixa melhor na simplicidade do ChatGPT |  

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** Navegação simples derivada de C02.
- **RC02:** Feedback/estado da aplicação deve estar sempre visível derivda de C02.
- **RC03:** A terminologia deve estar balanceada entre termos de programação competitiva e linguagem simples derivada de C01 e C02.

## Referências

{{fontes dos produtos, avaliações e literatura}}

1.Avaliação de usuário sobre programação competitiva no [CodeForces](https://codeforces.com/blog/entry/75742).

2.Competitive Programming 4 (CP4) de Steven Halim, Felix Halim e Suhendry Efendy (2020), Prefácio de Brian Christopher Dean

3.[Early Introduction of Competitive Programming](https://www.researchgate.net/publication/228411471_Early_introduction_of_competitive_programming), escrito por Pedro Ribeiro e Pedro Guerreiro (2008)

4.[ChatGPT](https://chatgpt.com/)

5.[CodeForces](https://codeforces.com/)

## Checklist

- [ ] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [ ] Há pelo menos uma análise completa por integrante.
- [ ] Cada análise contém prints legíveis da interface.
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage.
- [ ] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [ ] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido.
- [ ] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [ ] Opiniões de UX têm fonte.
- [ ] A síntese compara critérios comuns e produz recomendações.
- [ ] Não há “copiar porque o concorrente faz”; há justificativa de adequação ao público/contexto.
