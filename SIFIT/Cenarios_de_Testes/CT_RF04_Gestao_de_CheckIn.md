# CT_RF04_Gestao_de_CheckIn.md

## Cenário 04: Validação do fluxo de Check-in e Controle de Acesso em tempo real.

### Caso de Teste 01: Realizar check-in manual para aluno adimplente.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C04-CT01 | Registrar o acesso manual de um cliente ativo e sem pendências financeiras. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O cliente deve estar ativo e com a situação financeira em dia. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Check-in"                         |
| **E** digitamos o código do cliente ou efetuamos a leitura do QR Code na seção "Entrada rápida" |
| **QUANDO** clicarmos no botão "Realizar check-in"                  |
| **ENTÃO** o sistema deve confirmar o acesso com sucesso            |
| **E** a contagem de "Presentes agora" deve ser incrementada em tempo real |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O check-in deve ser concluído sem erros e o aluno adicionado à lista de presentes. |

---

### Caso de Teste 02: Bloqueio de acesso para cliente inadimplente.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C04-CT02 | Impedir a realização do check-in de um aluno com parcela em atraso superior ao limite de tolerância. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O cliente deve possuir parcela vencida há mais de 2 dias.    |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Check-in"                         |
| **E** informamos o código de um cliente com mensalidade vencida na "Entrada rápida" |
| **QUANDO** clicarmos no botão "Realizar check-in"                  |
| **ENTÃO** o sistema deve negar o acesso                             |
| **E** deve ser exibida uma mensagem de alerta informando a pendência financeira |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O check-in não deve ser efetuado e a catraca/sistema deve barrar a entrada do aluno. |

---

### Caso de Teste 03: Filtrar listagem de acessos por estado de presença.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C03-CT03 | Validar a alternância entre as abas de presença na tabela de check-ins. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem registros de acessos e faltas no dia corrente.     |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Check-in"                         |
| **QUANDO** alternarmos entre as abas "Todos", "Presentes agora", "Não compareceram" e "Check-in pendente" |
| **ENTÃO** a tabela deve filtrar e exibir apenas os clientes correspondentes à aba selecionada |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os dados exibidos na tabela devem atualizar dinamicamente de acordo com a aba selecionada. |

---

### Caso de Teste 04: Visualização das métricas de frequência e gráfico de pico de movimento.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C04-CT04 | Validar o carregamento dos indicadores de frequência diária e gráfico de horários de pico. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve acessar a tela de "Check-in".                     |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que acessamos o menu "Check-in"                           |
| **QUANDO** o painel for renderizado                                |
| **ENTÃO** os indicadores de "Check-ins hoje", "Presentes agora", "Meta do dia", "Média diária" e "Taxa de frequência" devem apresentar os valores computados |
| **E** o gráfico de "Pico de movimento" deve exibir o histograma por faixa horária |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os indicadores e o gráfico de movimento devem ser carregados corretamente e em tempo real. |