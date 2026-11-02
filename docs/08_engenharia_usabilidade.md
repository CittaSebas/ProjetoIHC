# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 28/10/2026  
**Status:** 🟩 concluída  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | Modelo Qwen3-4B-Instruct-2507 com ajuste fino, que classifica os rótulos do enunciado, mapeia para tópicos pedagógicos e monta a trilha | desempenho técnico não é substituído pelo teste de IHC |
| camada de interação da disciplina | Interface web usada por dois perfis. **Aluno (P01):** apresentar a questão, acompanhar o processamento e ver a trilha com a ordem e a dependência entre tópicos e a fonte de cada um (F01–F05; tarefa T01). **Professor (P02):** ver de que fonte veio cada tópico da trilha, hoje o livro do Cormen (*Introduction to Algorithms*), para confiar no material antes de repassá-lo aos alunos (tarefa T02) | compreensão, eficácia, eficiência, satisfação, erros, acessibilidade etc. |
| integrações/dados simulados | A inferência é real, feita pelo modelo do TCC hospedado no Hugging Face.  | Os testes avaliam como as fontes são apresentadas, não se a recuperação está correta. As trilhas exibidas podem conter erros reais do modelo, o que precisa ser considerado ao analisar MU01 |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Aplicação web acessada pelo navegador. A inferência usa o modelo do TCC hospedado no Hugging Face | O aluno não instala nada nem precisa de ambiente Python, barreira registrada na Entrega 1. A interface pode seguir convenções de páginas web que o público já usa (H12, H27) |
| Hardware/dispositivos | Do lado do aluno, notebook ou desktop, com o enunciado aberto em outra aba (H22, a confirmar pelas perguntas 9 e 10 do questionário da Entrega 7). Do lado do professor, computador usado na preparação de aula ou de treino (P02, hipótese). Do lado do sistema, servidor do Hugging Face | A trilha precisa caber ao lado do enunciado numa tela de notebook. Se a Entrega 7 mostrar uso de celular, o resultado precisa de uma versão em lista. Para o professor, a fonte de cada tópico precisa ser legível sem esconder a trilha |
| Capacidades | Colar textos longos da área de transferência: permite enviar o enunciado inteiro (T01, 1.1)<br>Desenhar grafos interativos, com zoom e destaque: permite mostrar a ordem e a dependência entre tópicos (F03)<br>Abrir links externos: permite levar o aluno e o professor à fonte de cada tópico (F04, T02)<br>Recursos de acessibilidade do próprio navegador (teclado, zoom, leitor de tela): permitem atender a Q03 sem software adicional<br>Inferência em menos de 10 s: permite que o aluno espere sem abandonar a tarefa | Entrada única por colagem, sem configuração prévia (N01, RC01); grafo com zoom e caminho recomendado destacado (Entrega 5); um indicador simples de processamento é suficiente |
| Restrições | O modelo pode errar na atribuição de tópico para o enunciado dado<br>O modelo não devolve grau de confiança por tópico<br>Os tópicos saem em inglês<br>Grafos ficam ilegíveis em telas pequenas | Como não há confiança por tópico, a trilha vem com o aviso padrão de que a IA pode cometer erros. Os termos precisam de explicação em português (H05, N05) |
| Conectividade/latência | Exige conexão com a internet. Se o serviço do Hugging Face estiver inativo, a primeira requisição pode demorar mais que o normal | Sem conexão não há consulta, e a interface deve dizer isso claramente em vez de parecer travada. Uma primeira resposta lenta precisa de mensagem de aviso própria |
| Segurança/privacidade | O aluno envia enunciados públicos de juízes online; O enunciado é processado em serviço externo (Kaggle) | Com a implementação histórico do usuário (Q12) ou sistema de contas implementados, o grupo terá de seguir a LGPD. |
| Volume de dados/histórico | Cada consulta gera uma trilha para uma única questão. A necessidade de guardar trilhas anteriores está em aberto (Q12, investigada na Entrega 7) | Não há volume que justifique busca, filtros ou paginação. Se Q12 for sustentada, basta uma lista simples das consultas anteriores |
| Tempo de processamento | Menos de 10 s por inferência | Indicador de que a consulta está sendo processada (F02, RC02). Nesse tempo não é preciso barra de progresso nem botão de cancelar |
| Papéis/permissões | Dois papéis: aluno (P01) e professor (P02). O professor só consulta a fonte da trilha; não altera trilhas nem fontes. Não há administrador | Como nenhum dos dois altera dados, não é preciso controle de permissões: a diferença entre os papéis está na tarefa, não no acesso. A prevenção de erros fica na entrada: avisar quando o texto enviado está vazio ou não parece um enunciado |

## 2. Princípios gerais do projeto

Inclua apenas normas, leis, padrões e princípios realmente relevantes, explicando **como** afetam o projeto. Não transforme esta seção em lista de links.

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso | Aluno iniciante em programação competitiva (P01), sozinho, em treino individual, no notebook, com o enunciado em outra aba; chega à ferramenta já travado e frustrado; não domina o vocabulário do domínio, que está em inglês; depende de conexão.<br>Professor (P02), especialista no domínio, prepara aula ou treino com pouco tempo e quer verificar a fonte do material antes de repassá-lo aos alunos (H25; cenário C02) | Aluno: a primeira tela aceita a questão sem nenhuma configuração (N01); a interface precisa ser autoexplicativa; a linguagem é calibrada para baixo conhecimento de domínio (H05).<br>Professor: a fonte de cada tópico (livro e capítulo) fica visível e verificável a partir da própria trilha, sem passos extras | Entregas 1/3/4 |
| LGPD, se aplicável | No recorte adotado, a interface não coleta dado pessoal: o aluno envia enunciados públicos, sem login. A lei passa a se aplicar se o histórico (Q12) exigir identificar o aluno, e já se aplica à coleta de dados da Entrega 7 | Sem login nem armazenamento de dado pessoal por padrão. Se o histórico entrar no escopo, guardar o mínimo necessário, informar a finalidade e permitir apagar | Lei nº 13.709/2018 — <https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm> |
| Acessibilidade | O resultado central é um grafo, que por padrão não é acessível a leitor de tela nem navegável por teclado. A necessidade específica do público ainda é desconhecida (Q03) | Alternativa textual do grafo como lista ordenada de tópicos (critério 1.1.1); todos os tópicos e links alcançáveis por teclado (2.1.1); dependência entre tópicos não indicada só por cor (1.4.1) | WCAG 2.2 (W3C) — <https://www.w3.org/TR/WCAG22/> |

## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreender por qual tópico começar e o que depende do quê | P01 / T01 | Ao ver a trilha, o aluno diz com as próprias palavras por onde começaria e por quê | N02, F03, H15 |
| Saber onde estudar cada tópico | P01 / T01 | O aluno aponta a fonte indicada para um tópico sem ajuda | N03, F04, H26 |
| Identificar de que fonte veio cada tópico e julgar se pode repassá-lo | P02 / T02 | O professor aponta o livro e o capítulo de um tópico e diz se repassaria aquele material aos alunos | H25; cenário C02: o professor quer confiar na fonte antes de repassá-la |
| Distinguir "processando" de "travou" | P01 / T01 | O aluno não reenvia a questão nem fecha a página durante o processamento | N06, F02, RC02 |
| Entender os termos da trilha ou saber onde consultar na fonte | P01 / T01 | O aluno não para diante de um termo sem saber o que fazer | N05, H05 |
| Não sentir que recebeu a solução pronta | P01 / T01 | O aluno diz que ainda vai resolver a questão sozinho | H07 |

### 3.2 Metas quantitativas

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | eficácia | taxa de conclusão sem ajuda | T01 | ≥ 50% | teste observado | Concluir é dizer, sem ajuda, por qual tópico começaria e por quê (H37). |
| MU02 | eficiência | tempo mediano | T01 | ≤ 3 min | cronômetro/log | Do abrir a página até dizer por onde começaria: inclui colar o enunciado, a inferência (menos de 10 s) e a leitura da trilha. O aluno chega já travado e com o tempo de treino correndo (H23) |
| MU03 | satisfação | escala pós-tarefa | T01–T02 | ≥ 5,5 | questionário | Single Ease Question (escala de 1 a 7) aplicada após cada tarefa, ao aluno em T01 e ao professor em T02; 5,5 é a média de referência da escala |
| MU04 | eficácia | taxa de conclusão sem ajuda | T02 | ≥ 50% | teste observado | Concluir significa o professor apontar, sem ajuda, o livro e o capítulo de onde veio um tópico da trilha. Mesmo critério de MU01 |
| MU05 | eficiência | tempo mediano | T02 | ≤ 1 min | cronômetro/log | Da trilha exibida até o professor chegar à fonte de um tópico. O professor tem pouco tempo de preparação (C02), e a verificação da fonte não pode virar uma tarefa à parte |

### 3.3 Priorização das metas (se exigida na disciplina)

Se o professor solicitar porcentagens que somem 100%, trate-as como **peso de prioridade**, não como métrica de usabilidade.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 | 30% | É o objetivo de A01: sair sabendo o que estudar. O aluno é o fluxo central, e sem eficácia as outras metas perdem o sentido |
| MU02 | 25% | O aluno chega travado e com pouco tempo (H23); se a consulta for lenta, ele volta às alternativas que já usa (H17–H19) |
| MU03 | 25% | A ferramenta concorre com chatbots e editoriais que o aluno já conhece, e o professor só a recomenda se a verificação for confortável |
| MU04 | 10% | Se o professor não encontra a fonte, ele não confia no material e não o repassa (H25) |
| MU05 | 10% | A verificação precisa caber no pouco tempo de preparação do professor (cenário C02) |
| **Total** | **100%** | |

## 4. Como o ciclo será iterado

Explique que artefatos serão revisitados após protótipos e avaliações.

- Após a análise dos dados da Entrega 7: revisar as hipóteses da Entrega 1 e na `RASTREABILIDADE.md`, as personas P01 e P02 (Entrega 3), os cenários C01 e C02 (Entrega 4) e as tarefas T01 e T02 (Entrega 5). Nesta entrega, revisar dispositivo e histórico na tabela da plataforma e os valores de MU01 a MU05.
- Será revisitado a interface já feita, dependendo do resultado obtido nas metas definidas acima, além da observação que será feita na Entrega 6.
## Checklist

- [ ] Capacidades e restrições têm impacto de IHC explicitado.
- [ ] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [ ] Resultados/processamento simulados no protótipo foram explicitados.
- [ ] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [ ] Normas/princípios estão contextualizados, não apenas copiados.
- [ ] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [ ] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [ ] Metas poderão ser verificadas nas Entregas 12–14.
