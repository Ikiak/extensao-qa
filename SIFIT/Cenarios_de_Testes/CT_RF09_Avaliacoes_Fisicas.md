# CT_RF09_Avaliacoes_Fisicas.md

## Cenário 09: Agendamento, Execução e Preenchimento de Avaliações Físicas.

### Caso de Teste 01: Agendamento inicial de avaliação física.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C09-CT01 | Agendar uma avaliação física registrando os dados básicos e gerando o status pendente. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O aluno e o personal trainer devem estar cadastrados no sistema. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Avaliações"              |
| **E** clicamos no botão "Cadastrar Avaliação"                           |
| **E** informamos o nome do aluno, o personal responsável, a data e o horário da avaliação |
| **QUANDO** confirmarmos o agendamento                              |
| **ENTÃO** o sistema deve criar um novo registro na tabela com o status "Pendente" |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A avaliação agendada deve ser exibida na listagem com o status "Pendente". |

---

### Caso de Teste 02: Execução e preenchimento dos dados antropométricos (Realizar Avaliação).

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C09-CT02 | Preencher os dados de IMC, Circunferências, Subcutâneas e Composição Corporal. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existir uma avaliação agendada com o status "Pendente".       |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Avaliações"              |
| **E** localizamos a avaliação pendente e clicamos no ícone da prancheta ("Realizar avaliação") |
| **E** na aba "IMC", informamos a Altura e o Peso para cálculo do Índice de Massa Corporal |
| **E** na aba "Circunferência", preenchemos as medidas de Pescoço, Ombro, Tórax, Braços, Antebraços, Abdômen, Cintura, Quadril, Coxas, Panturrilhas e Relação Cintura/Quadril |
| **E** na aba "Subcutâneas", informamos as dobras cutâneas (Bíceps, Triceptal, Subescapular, Axila, Supra Ilíaca, Tórax, Abdominal, Coxa e Panturrilha) |
| **E** na aba "Composição Corporal", validamos os dados calculados (% de Gordura, Peso da Gordura, Densidade Corporal, % Massa Magra, Peso da Massa Magra, Peso Ideal e Peso Excesso) |
| **QUANDO** clicarmos no botão "Salvar"                             |
| **ENTÃO** a avaliação deve ser concluída e o status atualizado na listagem |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Todas as abas devem permitir o correto preenchimento e salvamento das métricas corporais do aluno. |

---

### Caso de Teste 03: Filtrar e consultar avaliações físicas.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C09-CT03 | Consultar avaliações cadastradas utilizando os filtros de busca.  |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem avaliações físicas cadastradas na base de dados.   |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Avaliações"              |
| **E** digitamos o nome do aluno no campo de busca                |
| **E** selecionamos o status "Pendente" ou "Realizado"              |
| **QUANDO** clicarmos no botão "Buscar"                             |
| **ENTÃO** a tabela deve filtrar e apresentar apenas as avaliações correspondentes aos filtros aplicados |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A listagem deve atualizar dinamicamente exibindo apenas as avaliações filtradas. |