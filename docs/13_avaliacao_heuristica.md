# Entrega 13: Avaliação de IHC por inspeção heurística

**Data:** 18/11/2026  
**Status:** 🟩 concluída  
**Responsabilidade:** 1 avaliação completa por integrante, sobre todas as telas e estados relevantes do projeto.

## Objetivo da atividade

Encontrar problemas de usabilidade da Cittação inspecionando a interface com as **10 heurísticas de Nielsen**. Cada avaliador trabalha sozinho primeiro; depois a equipe consolida os problemas repetidos e define prioridades.

> Registramos apenas problemas reais. A matriz de cobertura mostra que as 10 heurísticas foram examinadas, e as heurísticas sem violação recebem um exemplo de boa prática.

## 1. Heurísticas adotadas

1. Visibilidade do status do sistema
2. Compatibilidade entre o sistema e o mundo real
3. Controle e liberdade do usuário
4. Consistência e padrões
5. Prevenção de erros
6. Reconhecimento em vez de memorização
7. Flexibilidade e eficiência de uso
8. Estética e design minimalista
9. Ajudar usuários a reconhecer, diagnosticar e recuperar-se de erros
10. Ajuda e documentação

## Cobertura especial para interfaces administrativas e analíticas

Quando existirem, não limite a avaliação às "telas principais". Inspecione também:

- dashboard em estados normal, vazio e erro;
- filtros sem resultado e filtros combinados;
- relatórios e exportação;
- histórico/listas longas;
- formulários CRUD (criação, edição, exclusão, validação);
- alteração de perfil/permissão;
- confirmações de ações destrutivas;
- processamento/loading/progresso;
- falha e recuperação;
- comparação de resultados;
- mensagens de termos técnicos, métricas e recomendações;
- ajuda/documentação contextual.

Em TCCs técnicos, observe especialmente se a interface comunica o estado do processamento e traduz informações técnicas para o vocabulário do usuário escolhido.

A Cittação não tem cadastro, exportação, permissões nem ações destrutivas, por isso esses estados não entram. Os estados de vazio, processamento, erro e filtro foram incluídos.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| Versão avaliada | aplicação em funcionamento em 17/11/2026 |
| Telas/estados | F01 a F11 e F02E da [Entrega 11](11_figma.md) |
| Estados especiais | vazio (F01), processamento (F02, F08), erro (F02E), filtro (F11), confirmação de avaliação (F07) |
| Fluxos | M01 (obter a trilha de estudo) e M02 (consultar o grafo de conhecimento) |
| Dispositivo/viewport | notebook, Chrome, 1920x1080 |
| Avaliadores | A01 Sebastian Citta, A02 Juan Manuel Citta |

**Fora do escopo:**
- a tela de login, que não faz parte dos fluxos M01 e M02;
- a qualidade das respostas do modelo, como a análise de complexidade ou o capítulo citado numa resposta. Avaliamos a interface, não o modelo.

## 3. Procedimento individual

Cada avaliador deve:

1. percorrer os fluxos/telas ao menos uma vez para familiarização;
2. inspecionar novamente aplicando sistematicamente H1 a H10;
3. registrar cada problema com evidência e contexto;
4. atribuir severidade **depois de compreender bem o problema**, justificando a decisão;
5. não discutir achados com os demais antes de terminar a inspeção individual, quando o objetivo for preservar independência.

### Escala de severidade (0 a 4)

| Grau | Interpretação |
|---:|---|
| 0 | não é considerado problema de usabilidade |
| 1 | problema cosmético; corrigir se houver tempo |
| 2 | problema menor; baixa prioridade |
| 3 | problema maior; alta prioridade |
| 4 | catástrofe de usabilidade; correção imperativa antes de disponibilizar |

Ao justificar, considere **frequência, impacto e persistência** do problema no contexto real de uso.

---

## Avaliador A01: Sebastian Citta

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | F02, F05, F07, F08, F10 | sim | V01 | |
| H2 | F01, F04 | não | | "Antes, estude" e "Depois, este tema leva a" |
| H3 | F04, F06, F10, F11 | sim | V02 | |
| H4 | F03, F04, F09, F10 | não | | mesma fonte, cores e aparência na trilha e no grafo |
| H5 | F01, F02E | não | | aviso de que a IA pode errar |
| H6 | F03, F09 | não | | legenda e instrução do grafo |
| H7 | F01, F09 | não | | busca, zoom e "Ajustar à tela" |
| H8 | F01, F04, F09 | não | | painel do tópico em blocos curtos |
| H9 | F02E | não | | links de recuperação no erro |
| H10 | F01, F03 | não | | 3 passos no chat vazio |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 | F05, F10 | O nó do tópico selecionado e o nó de um tópico já estudado usam a mesma cor azul. Olhando o grafo, não dá para saber se o tópico está só selecionado ou se já foi estudado | [F05](../assets/11_figma/f05_topico_estudado.png), [F10](../assets/11_figma/f10_grafo_topico.png) | 2 | ocorre sempre que o aluno seleciona um tópico; ele pode achar que já estudou um tema que não estudou; a caixa "Já estudei este tópico" no painel reduz o impacto | usar uma cor própria para estudado (por exemplo verde com ícone de check) e apenas um contorno destacado para o selecionado |
| V02 | H3 | F04, F06 | "Perguntar sobre este tópico" envia sozinha uma pergunta pronta ("O que é Laços de repetição (for/while)?"). O aluno não consegue editar a pergunta nem escrever a dúvida dele | [F06](../assets/11_figma/f06_resposta_topico.png) | 3 | ocorre em todo uso do botão; o rótulo promete uma pergunta do aluno e entrega uma resposta genérica; para tirar a dúvida real é preciso descobrir o chat sozinho | ao clicar, preencher o campo com "Sobre Laços de repetição: " e deixar o aluno completar antes de enviar |

### 6. Boas práticas: heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H2 | "Antes, estude" e "Depois, este tema leva a" no painel do tópico | [F04](../assets/11_figma/f04_painel_topico.png) | usa a linguagem do aluno em vez de "pré-requisito" e "sucessor" |
| H4 | mesma fonte serifada nos títulos, mesma paleta (azul para ações, laranja para avisos da IA) e mesma aparência dos nós na trilha e no grafo de conhecimento | [F03](../assets/11_figma/f03_trilha_montada.png), [F09](../assets/11_figma/f09_grafo_completo.png) | o aluno reconhece os tópicos e as ações nos dois contextos sem reaprender |
| H5 | aviso "Respostas geradas por IA podem conter erros. Confira no livro." junto do campo | [F01](../assets/11_figma/f01_chat_vazio.png) | previne que o aluno confie cegamente na resposta |
| H6 | legenda do grafo e "Clique num tópico para ver o resumo e o trecho do livro" | [F09](../assets/11_figma/f09_grafo_completo.png) | as cores e as ações ficam visíveis, sem precisar lembrar |
| H7 | "Buscar tópico", zoom e "Ajustar à tela" | [F09](../assets/11_figma/f09_grafo_completo.png) | atalhos para quem já sabe o que procura |
| H8 | painel do tópico com explicação curta, capítulo e antes/depois em blocos separados | [F04](../assets/11_figma/f04_painel_topico.png) | mostra só o necessário para decidir o que estudar |
| H9 | links "Era um problema? Gerar a trilha" e "Era uma pergunta? Responder como pergunta" | [F02E](../assets/11_figma/f02e_falha_trilha.png) | oferecem um caminho de recuperação quando o sistema interpreta mal a entrada |
| H10 | os 3 passos no chat vazio | [F01](../assets/11_figma/f01_chat_vazio.png) | explicam o uso no primeiro contato |

---

## Avaliador A02: Juan Manuel Citta

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | F02, F07, F08 | não | | "Pensando...", "Carregando o grafo..." e "Obrigado pela avaliação" |
| H2 | F01, F04 | não | | "Tema de programação básica, sem capítulo no CLRS" |
| H3 | F04, F10, F11 | não | | fechar o painel e filtro "Todas" |
| H4 | F04, F09, F10 | sim | V03 | |
| H5 | F01, F02E | não | | aviso de que a IA pode errar |
| H6 | F03 | não | | trilha numerada com pré-requisitos visíveis |
| H7 | F01, F09 | não | | "Enter envia" e "Buscar tópico" |
| H8 | F04, F09, F11 | não | | filtro que mostra só os tópicos de uma área |
| H9 | F02E | não | | links de recuperação no erro |
| H10 | F03 | não | | "Como esta trilha foi feita" |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V03 | H4 | F09, F10, F11 | Não é possível arrastar o grafo segurando o botão esquerdo do mouse para percorrê-lo, como é comum em mapas e editores de grafo | [F09](../assets/11_figma/f09_grafo_completo.png) | 2 | ocorre sempre que o aluno explora o grafo; quebra um padrão que ele já conhece; o zoom e o "Ajustar à tela" permitem contornar | permitir arrastar o grafo com o botão esquerdo, com o cursor de mão indicando a ação |

### 6. Boas práticas: heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 | "Pensando...", "Carregando o grafo..." e "Obrigado pela avaliação" | [F02](../assets/11_figma/f02_processando.png), [F08](../assets/11_figma/f08_carregando_grafo.png), [F07](../assets/11_figma/f07_avaliacao.png) | o aluno sabe que o sistema está trabalhando e que a ação foi registrada |
| H2 | "Tema de programação básica, sem capítulo no CLRS" no painel do tópico | [F04](../assets/11_figma/f04_painel_topico.png) | explica em linguagem simples por que não há referência no livro |
| H3 | fechar o painel do tópico e voltar ao grafo completo pelo filtro "Todas" | [F10](../assets/11_figma/f10_grafo_topico.png), [F11](../assets/11_figma/f11_grafo_filtrado.png) | o aluno sai de qualquer estado com um clique |
| H5 | aviso "Respostas geradas por IA podem conter erros. Confira no livro." junto do campo | [F01](../assets/11_figma/f01_chat_vazio.png) | previne que o aluno confie cegamente na resposta |
| H6 | trilha numerada, com os pré-requisitos ligados a cada tópico | [F03](../assets/11_figma/f03_trilha_montada.png) | a ordem de estudo fica visível, sem o aluno precisar lembrar |
| H7 | "Enter envia" no chat e "Buscar tópico" no grafo | [F01](../assets/11_figma/f01_chat_vazio.png), [F09](../assets/11_figma/f09_grafo_completo.png) | atalhos para quem já sabe o que quer |
| H8 | filtro por área no grafo de conhecimento | [F11](../assets/11_figma/f11_grafo_filtrado.png) | esconde os tópicos que não interessam e deixa o grafo mais limpo |
| H9 | links "Era um problema? Gerar a trilha" e "Era uma pergunta? Responder como pergunta" | [F02E](../assets/11_figma/f02e_falha_trilha.png) | oferecem um caminho de recuperação quando o sistema interpreta mal a entrada |
| H10 | "Como esta trilha foi feita" abaixo da trilha | [F03](../assets/11_figma/f03_trilha_montada.png) | explica como a trilha foi montada no momento em que o aluno a vê |

---

## 7. Consolidação da equipe

Problemas iguais ou muito semelhantes encontrados por avaliadores diferentes devem ser consolidados, preservando quem os encontrou.

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| HC01 | V02(A01) | H3 | "Perguntar sobre este tópico" envia uma pergunta pronta, sem deixar o aluno editar | 3 | alta | Sebastian Citta |
| HC02 | V01(A01) | H1 | tópico selecionado e tópico estudado usam a mesma cor azul | 2 | média | Juan Manuel Citta |
| HC03 | V03(A02) | H4 | não é possível arrastar o grafo com o mouse | 2 | média | Juan Manuel Citta |

Os dois avaliadores não encontraram o mesmo problema, então nenhum achado foi fundido. A severidade final é a do avaliador que encontrou o problema.

## 8. Síntese e plano de melhoria

- **Quantidade por heurística e severidade:** 3 problemas, um em H1 (severidade 2), um em H3 (severidade 3) e um em H4 (severidade 2). Nenhum de severidade 4.
- **Problemas graves:** HC01 é o único de severidade 3. Ele está no fluxo M01 (T01), então a QA06 da [Entrega 12](12_planejamento_avaliacao.md) não é atendida. Nenhum problema bloqueia o teste: o aluno ainda consegue tirar a dúvida pelo chat.
- **Padrões recorrentes:** dois dos três problemas (HC02 e HC03) estão na interação com o grafo, tanto no estado visual dos nós quanto na forma de navegar.
- **Correções antes da avaliação com usuários:** nenhuma correção será feita antes do teste. HC01 será observado na UT03 e o resultado será comparado na seção F da [Entrega 14](14_observacao_usuario.md). Depois do teste, a ordem de correção é HC01, HC02 e HC03.

## Checklist

- [x] Cada integrante fez uma inspeção completa e identificada.
- [x] Todas as telas/estados relevantes foram examinados.
- [x] Estados administrativos, filtros, relatórios, históricos, processamento e erros foram incluídos quando existentes.
- [x] A inspeção avaliou a interface/protótipo, não o mérito técnico do algoritmo/modelo.
- [x] H1 a H10 aparecem na matriz de cobertura de cada avaliador.
- [x] Parte de violações contém apenas violações, sem "forçar" exemplos.
- [x] Todo problema tem print/localização e contexto.
- [x] Severidade possui justificativa, não apenas número.
- [x] Recomendação resolve a causa ou reduz o impacto.
- [x] Achados duplicados foram consolidados ao final.
