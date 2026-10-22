# CT_RF13_Gestao_Financeira_Avancada.md

## Cenário 13: Abertura e Fechamento de Caixas, Gestão do Gateway Pagar.me e Emissão de Relatórios.

### Caso de Teste 01: Executar abertura e fechamento do caixa diário.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C13-CT01 | Validar a abertura e o fechamento de caixa preenchendo os dados operacionais e buscando contas por período. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O operador deve possuir permissão para gestão de caixa e estar na tela de "Caixas". |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Caixas"                          |
| **E** clicamos no botão "Abrir Caixa"                              |
| **E** no modal "Abrir Caixa", confirmamos a Data, o Funcionário Cadastrante, selecionamos o Local de Contas (ex: "Caixa Academia") e clicamos em "Salvar" |
| **E** realizamos as movimentações operacionais do período         |
| **E** acionamos o botão de visualizar/fechamento de caixa                     |
| **E** no modal "Fechamento de Caixa", informamos o Usuário, Data Inicial, Data Final e o Local de Contas |
| **QUANDO** clicarmos no botão "Buscar Contas" e confirmarmos em "Salvar" |
| **ENTÃO** o sistema deve conferir os totais e encerrar o período do caixa |
| **E** o histórico do caixa deve ser registrado na lista de caixas |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os modais de abertura e fechamento devem permitir a busca e gravação correta dos dados e totais de movimentação do caixa. |

---

### Caso de Teste 02: Consultar saldo e recebíveis no Gateway de Pagamento (Pagar.me).

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C13-CT02 | Visualizar métricas de faturamento, saldo disponível para saque e repasses futuros. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| A integração com o gateway Pagar.me deve estar ativa no sistema. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Pagar.me"                |
| **QUANDO** a dashboard de integração for totalmente carregada     |
| **ENTÃO** o painel deve exibir o saldo disponível para saque, os recebíveis futuros e o resumo por método de pagamento |
| **E** o botão para solicitação de repasse deve ficar disponível caso haja saldo liberado |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| As informações de faturamento e saldos exibidos devem corresponder aos dados síncronos da conta no gateway. |

---

### Caso de Teste 03: Gerar e exportar relatórios consolidados do sistema em PDF.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C13-CT03 | Emitir relatório consolidado de movimentações (ex: Contas a Receber, Contas a Pagar, Caixas ou Clientes). |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Relatórios".                      |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Relatórios"                       |
| **E** selecionamos o tipo de relatório desejado (Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar ou Caixas) |
| **E** definimos o intervalo de datas       |
| **QUANDO** clicarmos no botão "Gerar Relatório"     |
| **ENTÃO** o sistema deve compilar os dados e disponibilizar o arquivo em PDF para visualização e download |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O arquivo PDF gerado deve conter todos os dados filtrados e consolidados no layout padrão de impressão. |