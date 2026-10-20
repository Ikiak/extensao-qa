# CT_RF03_Dashboard_Analitico.md

## Cenário 03: Visualização e análise de indicadores gráficos no Dashboard.

### Caso de Teste 01: Visualização dos gráficos de perfil demográfico dos clientes.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C03-CT01 | Validar a renderização dos gráficos de Frequência, Idade e Sexo dos clientes. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar autenticado e acessar a tela "Dashboard". |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que navegamos para o menu "Dashboard"                     |
| **QUANDO** o bloco superior da página for carregado                |
| **ENTÃO** o gráfico de linhas de "Frequência" deve ser exibido     |
| **E** o gráfico de barras por faixa de "Idade" (ex: 18 a 25, 26 a 40) deve apresentar a distribuição de alunos |
| **E** o gráfico em pizza proporcional por "Sexo" (Masculino e Feminino) deve ser renderizado |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os gráficos do perfil de clientes devem ser carregados sem inconsistências visuais ou dados corrompidos. |

---

### Caso de Teste 02: Análise de dados de Matrículas e Planos.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C03-CT02 | Validar a exibição dos indicadores gráficos de matrículas mensais e adesão por plano. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem registros de matrículas ativas e planos vinculados no sistema. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Dashboard"                        |
| **QUANDO** analisarmos a seção "Matrículas"                        |
| **ENTÃO** o gráfico de barras "Por Mês" deve apresentar o volume de contratos por período |
| **E** o gráfico circular "Por Plano" deve exibir a divisão percentual dos planos contratados pelos alunos |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| As informações de contratos e planos devem refletir fielmente o volume armazenado na base de dados. |

---

### Caso de Teste 03: Visualização do balanço de Contas a Receber no Dashboard.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C03-CT03 | Validar os gráficos financeiros de faturamento por método de pagamento e mês. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem lançamentos de recebimentos financeiros no sistema. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Dashboard"                        |
| **QUANDO** rolar a página até a seção "Contas a Receber"           |
| **ENTÃO** o gráfico "Por Método de Pagamento" deve apresentar a proporção entre débito, crédito e outros métodos |
| **E** o gráfico "Por Mês" deve exibir a evolução do faturamento em escala de valores |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os totais e divisões por forma de pagamento devem corresponder aos recebimentos consolidados no financeiro. |