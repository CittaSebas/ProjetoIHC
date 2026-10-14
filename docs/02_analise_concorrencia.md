# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026 — revisada em 16/09/2026
**Status:** 🟦 revisada após feedback
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

## Como ler as afirmações desta entrega

A mesma convenção da Entrega 1 vale aqui, e é especialmente importante nesta atividade:

- **[F] observação** — algo que a equipe viu na interface, com produto e data de acesso identificados. Vale apenas para o produto e o estado observados.
- **[H] interpretação** — o que a equipe acredita que aquela observação significa para uma pessoa. Exige dado sobre pessoas para virar fato.
- **[?] lacuna** — o que ainda não foi observado nem investigado.

> **Distinção central desta entrega:** observar que uma característica **existe em um produto** não demonstra que o público-alvo **prefira, conheça ou esteja acostumado** com ela. A primeira afirmação é evidência de interface; a segunda é afirmação sobre pessoas e precisa de dado sobre pessoas.

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Juiz online / fórum de programação competitiva | ferramenta cotidiana | É a forma tradicional de praticar e de buscar ajuda da comunidade; é onde a questão que trava o aluno está hospedada | [H] H17, H18 | analisado — C01 (Codeforces) |
| Chatbot de propósito geral | concorrente direto do fluxo | É o caminho que o aluno plausivelmente já usa hoje para pedir explicação de um enunciado | [H] H19 | analisado — C02 (ChatGPT) |
| Livros e materiais didáticos consolidados | alternativa | São a base pedagógica que o TCC pretende usar como âncora | [H] H26 | **não analisado nesta entrega** — registrado como lacuna |

**Hipóteses da Entrega 1 que esta entrega deveria alimentar:** `H05` (linguagem compreensível), `H12` (padrão conversacional familiar), `H13` (listas e filtros familiares), `H19` (aluno usa chatbot generalista), `H26` (livros organizados por assunto). O resultado de cada uma está registrado na seção 6 e em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

**Aluno iniciante em programação competitiva**, conforme o recorte priorizado em 7.2 da Entrega 1: estudante que já resolve questões em juiz online mas ainda não domina o repertório algorítmico da modalidade.

A análise foi conduzida a partir do objetivo **A01 — descobrir o que precisa saber para conseguir resolver uma questão em que travou**. Cada interface foi examinada perguntando: *o que este produto oferece a alguém que acabou de travar numa questão e não sabe o que estudar?*

[?] Q02 — O que significa concretamente "iniciante" neste domínio (conhecimento prévio, tempo de prática, vocabulário) continua sendo lacuna da Entrega 1, a investigar na Entrega 3. Isso limita o alcance das conclusões desta entrega.

## 2. Concorrentes diretos/indiretos

> ### ⚠ Pendência de conformidade — prints locais
>
> O feedback da Entrega 2 apontou que `assets/02_concorrencia/` está vazio: os prints abaixo estão referenciados por URLs externas de anexo do GitHub, o que não cumpre o requisito de manter a evidência no repositório.
>
> **Ação necessária (a equipe precisa executar):** salvar cada print em `assets/02_concorrencia/` com os nomes indicados na coluna "Arquivo local" e trocar a referência externa pelo caminho relativo, no formato `![legenda](../assets/02_concorrencia/nome.png)`. Os estados marcados `A CAPTURAR` ainda não foram registrados.

### Análise C01 — Juiz online e fórum de programação competitiva

**Autor(a):** Juan Manuel Citta — 24.123.022-6
**Produto:** Codeforces
**Tipo:** indireto — não gera trilhas de estudo, mas é onde a atividade do aluno acontece
**Link oficial:** <https://codeforces.com/>
**Data de acesso:** 26/08/2026

#### Contexto e proposta

[F] É uma plataforma para praticar programação competitiva. O usuário procura questões, submete tentativas e recebe veredito automático da submissão, incluindo o tipo de erro (por exemplo, limite de tempo excedido). Também permite interagir com a comunidade por posts em formato de fórum e consultar competições passadas e ativas. *Observado em 26/08/2026.*

#### Tarefa observada

**Tarefa:** a partir de uma questão que o aluno não sabe resolver, descobrir o que precisa estudar usando apenas os recursos da plataforma.

#### Telas e estados percorridos

| # | Tela/estado | O que foi observado | Arquivo local | Evidência atual |
|---|---|---|---|---|
| C01-1 | Home / aba *Catalog* (fórum) | Estrutura de fórum tradicional, com listagem de posts e tópicos | `c01_1_catalog.png` | <img width="1223" alt="Codeforces — aba Catalog" src="https://github.com/user-attachments/assets/5d521552-7d11-4280-bdd7-0cb57384b35e" /> |
| C01-2 | Aba *ProblemSet* | Tabela de questões com colunas de nome, tags, dificuldade e número de resolvedores; filtro lateral por tag e por faixa de dificuldade | `c01_2_problemset.png` | <img width="1263" alt="Codeforces — ProblemSet" src="https://github.com/user-attachments/assets/dcc28068-dddc-4d49-b847-b790b065c06d" /> |
| C01-3 | Aba *Contests* | Lista filtrável de competições passadas e ativas | `c01_3_contests.png` | <img width="1255" alt="Codeforces — Contests" src="https://github.com/user-attachments/assets/0804ef2f-a134-48bd-84b3-f9ac04d72ada" /> |
| C01-4 | Página de uma questão, com tags visíveis | `A CAPTURAR` — é o estado mais relevante para A01 e não foi registrado | `c01_4_questao_tags.png` | — |
| C01-5 | Veredito de submissão (aceito / erro) | `A CAPTURAR` — necessário para sustentar a afirmação sobre feedback na síntese | `c01_5_veredito.png` | — |

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência | Observação de IHC |
|---|---|---|---|
| Acessar o fórum | Aba *Catalog* na home | C01-1 | [F] Formato de fórum tradicional: lista de tópicos e comentários encadeados |
| Localizar questões | Aba *ProblemSet* | C01-2 | [F] Tabela densa com metadados por linha; a informação principal é a lista, não a questão |
| Filtrar por tag e dificuldade | Painel lateral da *ProblemSet* | C01-2 | [F] O refinamento exige que o usuário **já saiba o nome da tag** que procura |
| Consultar competições | Aba *Contests* | C01-3 | [F] Lista filtrável por período e tipo |
| Receber veredito de submissão | Envio de código na página da questão | C01-5 `A CAPTURAR` | [F] A plataforma devolve aprovação/reprovação e o tipo de erro. **Este é um tipo de feedback**, ainda que não seja feedback de processamento conversacional |

#### Experiência do usuário e opiniões

[?] **Lacuna não preenchida.** A equipe não levantou avaliações públicas, relatos identificados, estudos de usabilidade ou testes próprios sobre o Codeforces. A referência 1 (post do blog do Codeforces) está listada nas referências, mas a equipe ainda não extraiu dela nenhuma afirmação atribuível.

**Para fechar esta lacuna é necessário:** identificar ao menos uma fonte por produto — post de blog, thread de fórum, estudo acadêmico ou teste próprio documentado — e registrar quem disse, quando e o que exatamente foi dito. Enquanto isso não existir, nenhuma afirmação desta entrega sobre o que usuários *acham* das interfaces pode ser sustentada.

#### Preço/modelo de negócio

[F] Gratuito. Plataforma com patrocínio da fundação TON (The Open Network). *Observado em 26/08/2026.*

#### Padrões e tendências percebidos

[F] **No Codeforces observado:** a interface segue convenções visuais de fórum de gerações anteriores — densidade alta de links, pouca hierarquia tipográfica, navegação por abas no topo.

[H] H29 — Outros juízes online (Beecrowd, LeetCode) teriam interfaces de gerações diferentes. *A versão anterior afirmava que "fóruns de programação competitiva em sua maioria têm interface mais antiga". A equipe examinou um produto; isso não sustenta afirmação sobre a maioria da categoria.*

#### Pontos positivos, limitações e lições

| Ponto | Observação [F] | Interpretação [H] | Implicação para nosso projeto |
|---|---|---|---|
| Filtros de refinamento | C01-2 oferece filtro por tag e por faixa de dificuldade | [H] H13 — dá controle a quem já conhece o vocabulário do domínio | **Não transferível diretamente:** o filtro pressupõe saber o nome da tag, que é exatamente o que falta ao aluno em A01. Se algum padrão de filtro entrar no projeto, precisará operar sobre algo que o aluno já saiba nomear |
| Densidade de informação na home | A home concentra muitos blocos e links sem hierarquia evidente | [H] H30 — pode dificultar a alguém que chega com um objetivo único e específico | Sugere manter a primeira tela focada na ação inicial de A01. **Isso é hipótese**, não conclusão: não foi medido com usuários |
| Tags presentes, caminho de estudo ausente | C01-2 mostra as tags, mas nenhuma tela indica ordem de estudo ou pré-requisito | [F] a ausência é observável | É a lacuna que o projeto endereça. Sustenta F03 e F04 da Entrega 1 |
| Veredito de submissão | A plataforma responde à submissão com aprovação/reprovação e tipo de erro | [F] | **Existe feedback de resultado.** O que não existe é feedback de processamento durante uma consulta — distinção corrigida na síntese |
| Aparência datada | Convenções visuais de fórum antigo | [?] Q13 — se isso afeta a percepção do aluno iniciante não foi verificado | *A versão anterior concluía que "alunos mais jovens podem não estar acostumados ou não ter preferência pela interface" e derivava disso a decisão de "manter um visual moderno". Isso é afirmação sobre pessoas sem dado sobre pessoas.* |

### Análise C02 — Chatbot de propósito geral

**Autor(a):** Sebastian Citta — 24.123.068-9
**Produto:** ChatGPT
**Tipo:** direto — é o caminho que o aluno plausivelmente usa hoje para a mesma necessidade (H19)
**Link oficial:** <https://chatgpt.com/>
**Data de acesso:** 26/08/2026

#### Contexto e proposta

[F] É uma aplicação web de acesso a um modelo de linguagem generalista. O usuário escreve uma pergunta e pode anexar arquivos, com limites que variam conforme o plano, e recebe uma resposta em texto. A proposta é ser uma ferramenta de assistência geral. *Observado em 26/08/2026.*

#### Tarefa observada

**Tarefa:** submeter o enunciado de uma questão de programação competitiva e pedir orientação sobre o que estudar para resolvê-la.

#### Telas e estados percorridos

| # | Tela/estado | O que foi observado | Arquivo local | Evidência atual |
|---|---|---|---|---|
| C02-1 | Tela inicial com caixa de entrada | Caixa de texto única centralizada, com ícone de anexo e poucos controles concorrentes | `c02_1_entrada.png` | <img width="1916" alt="ChatGPT — tela de entrada" src="https://github.com/user-attachments/assets/20ca14c9-24cc-494d-95aa-6a4d0a7d0bad" /> |
| C02-2 | Resposta a um enunciado de programação competitiva | `A CAPTURAR` — é o estado que sustenta a comparação com a trilha estruturada | `c02_2_resposta.png` | — |
| C02-3 | Estado de processamento (resposta sendo gerada) | `A CAPTURAR` — **necessário para RC02** | `c02_3_processando.png` | — |
| C02-4 | Erro ou interrupção e mecanismo de nova tentativa | `A CAPTURAR` — **necessário para RC02** | `c02_4_erro_retry.png` | — |

> Os estados C02-3 e C02-4 são os que faltavam para que RC02 pudesse ser derivada de C02. Sem eles, RC02 permanece rebaixada a hipótese — ver seção 5.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência | Observação de IHC |
|---|---|---|---|
| Enviar pergunta | Clicando na caixa de texto e digitando | C02-1 | [F] A ação principal é única e ocupa o centro da tela |
| Anexar arquivo | Ícone ao lado da caixa | C02-1 | [F] Segunda entrada possível, visualmente subordinada à primeira |
| Acompanhar geração da resposta | Resposta aparece progressivamente | C02-3 `A CAPTURAR` | [F] a capturar |
| Reenviar / regenerar | Controle na própria mensagem | C02-4 `A CAPTURAR` | [F] a capturar |

#### Experiência do usuário e opiniões

[?] **Lacuna não preenchida**, pelo mesmo motivo registrado em C01. Nenhuma avaliação pública, relato identificado ou teste próprio documentado foi levantado sobre o uso do ChatGPT para esta tarefa específica.

#### Preço/modelo de negócio

[F] Assinatura. Há plano gratuito com limite de uso e planos pagos com mais capacidade e acesso a modelos adicionais. *Observado em 26/08/2026.*

#### Padrões e tendências percebidos

[F] **No ChatGPT observado:** a ação inicial é concentrada em uma caixa de texto única, com baixo ruído visual em volta.

[H] H28 — Outros produtos de LLM conversacional (DeepSeek, Claude, Gemini) seguiriam padrão semelhante. *A versão anterior afirmava isso como característica da maioria do mercado. A equipe examinou um produto. Para sustentar a afirmação seria preciso examinar os demais e registrar a evidência, ou limitar a redação ao ChatGPT — foi escolhida a segunda opção.*

#### Pontos positivos, limitações e lições

| Ponto | Observação [F] | Interpretação [H] | Implicação para nosso projeto |
|---|---|---|---|
| Entrada única e de baixo ruído | C02-1 mostra uma caixa central com poucos controles concorrentes | [H] H12 — reduzir escolhas concorrentes no momento inicial pode facilitar começar a tarefa | Sustenta RC01, **desde que justificada pela tarefa A01** e não pela semelhança com o concorrente |
| Resposta em texto corrido | Na consulta observada, a orientação veio como prosa sequencial | [H] H15 — texto corrido não representa dependência entre tópicos | Sustenta a aposta de resultado estruturado do recorte 7.4. Limitado à consulta observada |
| Sem fonte pedagógica verificável | Na consulta observada, a resposta não citou livro ou capítulo | [F] limitado à consulta observada | Sustenta F04 (fonte por tópico). Não é afirmação sobre o produto em todo e qualquer uso |
| Sem indicação de incerteza | Na consulta observada, a resposta foi apresentada com o mesmo tom independentemente da confiança | [H] H06 — o iniciante não tem como calibrar o quanto confiar | Sustenta F05. Reforçado pelo F1 Macro de 0,5820 do próprio TCC |

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

> **Revisão após feedback.** A versão anterior concluía desta seção que "o público-alvo prefere", "está acostumado com" ou "domina" determinadas convenções. Prints demonstram que a **característica existe no produto**; não demonstram preferência, familiaridade ou hábito de nenhuma pessoa. A coluna final foi separada em observação e hipótese.

| Software | Por que o público usaria | Padrão observado [F] | Prints | Hipótese sobre o usuário [H] |
|---|---|---|---|---|
| Codeforces | Procurar questões e discutir soluções | Fórum + tabelas densas + filtros | <img width="1542" alt="Codeforces — home" src="https://github.com/user-attachments/assets/29dd7d73-f867-406d-b59f-d6c14d29f3ee" /> | [H] H13 — listas com filtros seriam convenção conhecida por quem já usa juízes online |
| Stack Overflow | Fazer perguntas de programação em geral | Post com respostas votadas e comentários | <img width="1265" alt="Stack Overflow" src="https://github.com/user-attachments/assets/6896c782-2386-4a4c-85da-21bdb5e0a986" /> | [H] H31 — o formato pergunta/resposta seria familiar ao público de programação |
| ChatGPT | Pedir explicações pontuais | Chat com entrada única | <img width="1507" alt="ChatGPT" src="https://github.com/user-attachments/assets/4e28b680-68c7-4237-a819-42a8e634f951" /> | [H] H12 — a entrada conversacional seria familiar |
| VS Code e outras IDEs | Escrever código | Área de trabalho central, alta densidade de painéis, forte customização | <img width="1191" alt="VS Code" src="https://github.com/user-attachments/assets/19576140-d69b-4b12-9cee-0a4e660f7130" /> | [H] H32 — o público toleraria interfaces densas e customizáveis. *Antes afirmado como fato* |
| GitHub | Versionar e compartilhar código | Feed de atividade na página inicial | <img width="1890" alt="GitHub" src="https://github.com/user-attachments/assets/fa80e2e2-0f00-4aad-8dee-d81703e136d4" /> | [H] H33 — o público estaria habituado a feeds e a muitas opções na tela inicial. *Antes afirmado como fato* |

[?] Q14 — Nenhuma dessas hipóteses sobre familiaridade foi verificada com alunos. Q02 (o que é "iniciante") precisa ser respondida antes: um aluno de primeiro ano e um competidor de terceiro ano podem ter repertórios de ferramenta muito diferentes. Investigar na Entrega 3.

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

> **Revisão após feedback.** A versão anterior decidia a adoção de padrões por critério técnico ("requer DB", "perder histórico e requer DB"). Viabilidade de implementação não responde se um padrão faz sentido em IHC. A pergunta correta é: **existe uma atividade ou objetivo do aluno que justifique este padrão?** A tabela foi refeita a partir dessa pergunta.

| Padrão observado | Produto(s) | Que tarefa do aluno justificaria | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| Entrada conversacional única | ChatGPT (C02-1) | A01 — apresentar a questão em que travou, sem preparo nem configuração prévia | Uma só decisão a tomar no início da tarefa | Não comunica o que o sistema é capaz de fazer nem o que espera receber | **sim** — adotado em 7.4; a familiaridade continua sendo H12, a investigar |
| Resposta estruturada com relações entre itens | nenhum dos analisados | A01 — saber em que ordem estudar e o que depende do quê | Torna visível a dependência entre tópicos, que é o que falta nas tags | Pode ser ilegível em tela pequena (Q09) e exigir aprendizado de leitura | **sim** — é a aposta central do recorte; hipótese H15 |
| Lista com filtros por tag e dificuldade | Codeforces (C01-2) | Nenhuma tarefa identificada até agora. O fluxo principal é uma consulta individual a partir de uma questão, não a exploração de um acervo | Controle fino para quem já conhece o vocabulário | **Pressupõe saber o nome da tag** — exatamente o que falta em A01 | **não, por ora** — H13 só entra se a Entrega 5 revelar uma tarefa que precise disso |
| Histórico de consultas | ChatGPT (barra lateral, C02-1) | Possivelmente: retomar em outra sessão uma trilha estudada ao longo de dias | Evita reprocessar e perder o resultado | Exige identificar o usuário entre sessões | **em aberto** — Q12. *Antes descartado por "requer DB", que é critério técnico, não de IHC* |
| Feedback de estado durante processamento | ChatGPT (C02-3, `A CAPTURAR`) | A01 — não abandonar a consulta achando que o sistema travou, dada a latência do LLM | Mantém a pessoa orientada durante a espera | Indicador permanente pode virar ruído | **sim** — F02; a evidência em C02 ainda precisa ser capturada |
| Administração / CRUD | — | Nenhuma tarefa do aluno iniciante identificada | — | Aumenta o número de telas sem objetivo rastreável | **não**. *A versão anterior marcava "talvez" para "todos os produtos", justificando por assinatura e postagens — nada disso pertence ao recorte do aluno* |
| Dashboard | — | Nenhuma tarefa identificada. *A versão anterior identificava "dashboard" no ChatGPT; o que existe ali é uma tela de entrada com histórico lateral, não um painel de indicadores* | — | — | **não** |

> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 — Codeforces | C02 — ChatGPT | Oportunidade para o projeto |
|---|---|---|---|
| Navegação | [F] Muitas opções simultâneas na home e nas listas, sem hierarquia evidente | [F] Navegação mínima na tela inicial; a ação principal é única | O aluno chega com um objetivo único e específico (A01). Manter poucas opções concorrentes **no momento de iniciar a consulta** parece apoiar essa tarefa — [H], a verificar na Entrega 6 |
| Feedback / estado | [F] **Tem feedback de resultado:** devolve veredito da submissão e o tipo de erro. **Não tem** feedback de processamento durante uma consulta de estudo | [F] Tem feedback de geração progressiva da resposta. Estados de erro e recuperação `A CAPTURAR` | São dois tipos distintos de feedback. Nosso projeto precisa do segundo, por causa da latência do LLM (F02). *Correção: a versão anterior registrava "Não tem" para o Codeforces, contradizendo a própria descrição de C01* |
| Prevenção / recuperação de erro | [?] Não observado | [F] Permite reenviar e regenerar a mensagem | Relevante para o caso em que a trilha gerada está incoerente (alucinação registrada no TCC). A evidência de C02 precisa ser capturada |
| Terminologia | [F] Vocabulário do domínio em inglês, sem definição na interface (`greedy`, `dp`, `constructive algorithms`) | [F] Linguagem geral, adaptada ao vocabulário da pergunta do usuário | São duas estratégias opostas. **Observar isso não indica qual serve ao aluno iniciante** — é exatamente a hipótese H05, que precisa de investigação na Entrega 7 |
| Acessibilidade | [F] Nenhum recurso de acessibilidade identificado **na inspeção realizada** — o que não permite concluir que o produto não seja acessível | [F] Oferece entrada por voz. Isso **pode** apoiar certos cenários, mas não torna a interface acessível de modo geral | Nenhuma conclusão é possível sem avaliação dedicada. Q03 da Entrega 1 (necessidade real de acessibilidade do público) precisa ser respondida antes; critérios WCAG 2.2 aplicáveis serão definidos na Entrega 8 |
| Eficiência | [F] Muita informação acessível por filtros e navegação em abas | [F] Poucas etapas entre abrir a página e enviar a primeira pergunta | *A versão anterior afirmava que o Codeforces "requer uso recorrente para se acostumar" e que o ChatGPT é "muito simples para o usuário médio". Ambas são afirmações sobre desempenho e aprendizado de pessoas, que não foram avaliadas.* O que se pode registrar é o número de passos observado, não o esforço percebido |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

> Cada recomendação segue a estrutura **evidência observada → implicação → relação com a tarefa do usuário**, e termina indicando seu estado: `adotada`, `provisória` ou `pendente de evidência`.

### RC01 — Concentrar a ação inicial em uma entrada única e de baixo ruído

- **Evidência observada:** C02-1 — a tela inicial do ChatGPT apresenta uma caixa de texto central com poucos controles concorrentes. [F], 26/08/2026.
- **Implicação:** quando há uma só ação possível no início, a pessoa não precisa decidir por onde começar antes de começar. [H]
- **Relação com a tarefa:** em A01 o aluno chega **já travado e com um objetivo único** — apresentar a questão em que empacou. Nesse momento, qualquer escolha adicional (selecionar fonte, nível, modo) é uma decisão que ele ainda não tem informação para tomar, porque não sabe nem o que precisa estudar. A recomendação vale por isso, **não porque o ChatGPT faz assim**.
- **O que precisa estar visível nesse momento:** [?] Q15 — a equipe ainda não sabe. Candidatos: o que o sistema aceita como entrada, o que ele vai devolver, quanto tempo leva. A investigar na Entrega 6.
- **Estado:** `adotada`, com Q15 em aberto. Origem: C02.

### RC02 — Dar retorno de estado durante operações cuja duração não é evidente

- **Evidência observada:** ⚠ **insuficiente.** A análise de C02 não registrou nenhum estado de carregamento, processamento, erro ou recuperação (C02-3 e C02-4 estão marcados `A CAPTURAR`). A versão anterior afirmava na síntese que o ChatGPT "mostra erros e mensagens de estado no processamento" sem print ou descrição que sustentasse.
- **Implicação:** sem retorno visível, a pessoa não distingue "processando" de "travou" e pode abandonar a operação. [H]
- **Relação com a tarefa:** a inferência do LLM do TCC tem latência perceptível (Entrega 1, seção 9.3), o que torna F02 necessário independentemente da concorrência. Mas **a Entrega 2 exige demonstrar o aprendizado obtido pela concorrência**, e isso ainda não foi feito.
- **Correção de redação:** o termo "sempre visível" da versão anterior foi retirado. A evidência disponível sustentaria, no máximo, feedback **durante operações cujo estado não é imediatamente óbvio** — não um indicador permanente na tela.
- **Estado:** `pendente de evidência`. Para promover a `adotada`, capturar C02-3 e C02-4 e descrever que informação o usuário recebe em cada um.

### RC03 — Tratar o equilíbrio de terminologia como questão em aberto, não como regra

- **Evidência observada:** C01 usa vocabulário do domínio em inglês sem definição na interface; C02 usa linguagem geral adaptada à pergunta. [F], ambos em 26/08/2026.
- **Implicação:** existem no mercado **duas estratégias opostas** de vocabulário para públicos que se sobrepõem. Isso é o que a observação demonstra.
- **Relação com a tarefa:** observar as duas estratégias **não indica qual serve ao aluno iniciante**. Essa é exatamente a hipótese H05 da Entrega 1 — "a linguagem precisa ser compreensível para quem tem pouco conhecimento de programação competitiva" — que permanece aberta. Há inclusive tensão real: o aluno precisa aprender o jargão em algum momento, já que é ele que aparece nas tags e nos livros; traduzir tudo pode atrapalhar essa transição.
- **Rastreabilidade:** observação da concorrência → refinamento de H05 → investigação na Entrega 7 → decisão de linguagem na Entrega 8.
- **Estado:** `provisória`. Não deve virar convenção da interface antes da Entrega 7.

## 6. O que esta entrega produziu para as hipóteses da Entrega 1

| Hipótese | O que esta entrega acrescentou | Estado após a Entrega 2 |
|---|---|---|
| H05 — linguagem compreensível | Mostrou duas estratégias opostas de terminologia no mercado (C01 x C02), mas nenhuma evidência sobre qual serve ao iniciante | **aberta, refinada** — a pergunta agora é *qual equilíbrio*, não *se importa* |
| H12 — entrada conversacional familiar | Confirmou que o padrão **existe** em uma ferramenta relevante (C02-1). Não confirmou familiaridade nem adequação ao público | **aberta** — evidência parcial: existência do padrão ≠ familiaridade |
| H13 — listas e filtros familiares | Confirmou que o padrão existe no Codeforces (C01-2) e revelou uma limitação: o filtro pressupõe saber o nome da tag, que é o que falta em A01 | **aberta, com evidência contrária à adoção** — nenhuma tarefa do projeto exige o padrão até agora |
| H19 — aluno usa chatbot generalista | Não investigada nesta entrega: a análise examinou o produto, não o comportamento do aluno | **aberta** — depende da Entrega 7 |
| H26 — livros organizados por assunto | Não analisada. Livros não entraram na amostra | **aberta** |
| H28 — chatbots como categoria | Criada nesta entrega, ao limitar a generalização sobre o mercado de LLMs ao produto observado | **aberta** |
| H29 — juízes online como categoria | Criada nesta entrega, pelo mesmo motivo | **aberta** |
| H30 a H33 — familiaridade do público com convenções | Criadas nesta entrega, ao converter em hipótese as afirmações sobre preferência e hábito do público-alvo | **abertas** |

Registrado em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## Referências

1. CODEFORCES TEAM. **Codeforces**. Disponível em: <https://codeforces.com/>. Acesso em: 26 ago. 2026.
2. OPENAI. **ChatGPT**. Disponível em: <https://chatgpt.com/>. Acesso em: 26 ago. 2026.
3. HALIM, S.; HALIM, F.; EFENDY, S. **Competitive Programming 4**. 2020. Prefácio de Brian Christopher Dean. *(Fonte pedagógica de referência do TCC; não analisada como interface nesta entrega.)*
4. RIBEIRO, P.; GUERREIRO, P. **Early introduction of competitive programming**. *Olympiads in Informatics*, v. 2, p. 149–162, 2008.
5. [Discussão de usuários sobre programação competitiva no blog do Codeforces, entry 75742](https://codeforces.com/blog/entry/75742). [?] **Fonte listada mas ainda não explorada** — nenhuma afirmação desta entrega se apoia nela. Ver a lacuna em "Experiência do usuário e opiniões".

## Checklist

- [X] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado. *(tabela de entrada obrigatória; livros permanecem não analisados e isso está registrado)*
- [X] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências. *(seção 6 e `../RASTREABILIDADE.md`)*
- [X] Há pelo menos uma análise completa por integrante. *(C01 — Juan Manuel Citta; C02 — Sebastian Citta, com a mesma estrutura de critérios)*
- [ ] Cada análise contém prints legíveis da interface. — **prints existem, mas hospedados externamente; faltam os arquivos em `assets/02_concorrencia/`**
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage. — **os estados C01-4, C01-5, C02-2, C02-3 e C02-4 ainda não foram capturados**
- [X] Foram analisados concorrentes e/ou interfaces representativas ao público. *(Codeforces, ChatGPT e cinco softwares cotidianos)*
- [X] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido. *(não se aplica — o TCC prevê interface)*
- [X] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos. *(seção 3.1 refeita pela pergunta da tarefa)*
- [ ] Opiniões de UX têm fonte. — **a subseção "Experiência do usuário e opiniões" continua sem fonte identificada nos dois produtos**
- [X] A síntese compara critérios comuns e produz recomendações. *(seções 4 e 5)*
- [X] Não há “copiar porque o concorrente faz”; há justificativa de adequação ao público/contexto. *(RC01 rejustificada pela tarefa; RC02 rebaixada; RC03 mantida provisória)*

> Os três itens desmarcados dependem de captura de prints e de levantamento de fontes de opinião — trabalho de coleta que a equipe precisa executar. Estão registrados como pendências, e não marcados, para que o estado da entrega seja honesto.

---

# Histórico de revisões

## Revisão 1 — 16/09/2026, após feedback do professor sobre a Entrega 2

| # | Ponto do feedback | O que mudou |
|---|---|---|
| 1 | `assets/02_concorrencia/` vazio | Adicionado aviso de pendência no início da seção 2, com o nome de arquivo esperado para cada print e a marcação `A CAPTURAR` nos estados que nunca foram registrados. **A pendência não foi resolvida** — depende de a equipe salvar os arquivos. |
| 2 | Profundidade desigual entre C01 e C02 | As duas análises foram reestruturadas com a mesma sequência: contexto, tarefa observada, telas e estados percorridos, funcionalidades, experiência do usuário, preço, padrões, pontos e lições. A subseção de experiência/opiniões deixou de estar em branco e passou a declarar explicitamente a lacuna e o que é preciso para fechá-la. |
| 3 | RC01 justificada por semelhança com o concorrente | Reescrita no formato evidência → implicação → relação com a tarefa. A justificativa passou a ser o estado em que o aluno chega em A01, não a aparência do ChatGPT. |
| 4 | RC02 sem evidência na análise | Rebaixada a `pendente de evidência`. O termo "sempre visível" foi retirado. Os estados C02-3 e C02-4 foram identificados como o que falta capturar para promovê-la. |
| 5 | RC03 tratada como regra | Rebaixada a `provisória`, com a cadeia de rastreabilidade explícita até H05 e a tensão real do problema registrada. |
| 6 | Contradição sobre o feedback do Codeforces | Corrigida na síntese: o Codeforces **tem** feedback de resultado (veredito de submissão) e **não tem** feedback de processamento de consulta. São tipos distintos. |
| 7 | Generalizações de mercado sem amostra | "Fóruns em sua maioria" e "LLMs em sua maioria" viraram H29 e H28, com a observação limitada ao produto examinado. |
| 8 | Afirmações sobre preferência do público | A seção 3 separou observação da interface de hipótese sobre o usuário; "o público prefere/está acostumado" virou H12, H13, H31, H32, H33 e a lacuna Q14. |
| 9 | Padrões decididos por critério técnico | Seção 3.1 refeita pela pergunta "que tarefa do aluno justificaria este padrão?". Histórico deixou de ser descartado por "requer DB" e passou a `em aberto` (Q12); dashboard e CRUD foram descartados por ausência de tarefa. |
| 10 | Acessibilidade e eficiência categóricas | Reescritas como características observáveis, com a ressalva de que ausência de recurso observado não permite concluir ausência de acessibilidade, e de que esforço percebido não foi medido. |
| 11 | Rastreabilidade não atualizada | Criada a seção 6, que registra o que esta entrega acrescentou a H05, H12, H13, H19 e H26, e `../RASTREABILIDADE.md` foi preenchido. |
| 12 | Checklist desmarcado apesar do status "concluída" | Preenchido item a item com a referência que o sustenta. Três itens permanecem **desmarcados de propósito**, porque dependem de coleta ainda não feita. |
