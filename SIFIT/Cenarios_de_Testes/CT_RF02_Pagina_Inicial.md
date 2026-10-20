# CT_RF02_Pagina_Inicial.md

## Cenário 02: Navegação e visualização de métricas na Página Inicial.

### Caso de Teste 01: Visualização dos cards operacionais e métricas de alunos.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C02-CT01 | Validar a exibição das métricas operacionais e resumo diário da academia na Página Inicial. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar autenticado no SIFIT e na Página Inicial. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na Página Inicial do SIFIT                    |
| **QUANDO** o painel principal for carregado                        |
| **ENTÃO** os cards de "Alunos em risco de evasão", "Valores em aberto", "Pico de movimento" e "Avaliações pendentes" devem ser exibidos com suas respectivas métricas |
| **E** os indicadores de "Clientes Ativos", "Clientes Ausentes", "Sem Matrículas", "Personais", "Matrículas no Período", "Desistências no Período" e "Renovações" devem apresentar seus valores |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Todos os widgets de resumo da academia devem ser carregados e exibidos sem erros de renderização. |

---

### Caso de Teste 02: Interação com o painel de Ações Recomendadas e Mensalidades Pendentes.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C02-CT02 | Validar o funcionamento das ações recomendadas do dia e atalho de cobrança. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na Página Inicial do sistema.           |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na Página Inicial do SIFIT                    |
| **E** visualizamos a seção de "Ações recomendadas para hoje" e "Mensalidades pendentes" |
| **QUANDO** clicarmos no botão "Cobrar todos no WhatsApp" ou nas ações de comunicação |
| **ENTÃO** o sistema deve iniciar o fluxo de cobrança/comunicação direcionado aos alunos pendentes |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os botões de ação devem ser interativos e direcionar para as rotinas de comunicação/cobrança correspondentes. |

---

### Caso de Teste 03: Visualização da Saúde da Academia e Inteligência de Retenção.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C02-CT03 | Validar a exibição do indicador de saúde da academia e classificação de risco. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O sistema deve possuir dados consolidados sobre a frequência dos alunos. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na Página Inicial do SIFIT                    |
| **QUANDO** analisarmos o bloco "Inteligência de Retenção" e "Saúde da Academia" |
| **ENTÃO** o medidor de retenção deve indicar o status geral da academia (ex: "Boa") |
| **E** a distribuição de alunos em "Alto risco", "Médio risco" e "Baixo risco" deve ser exibida |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O medidor gráfico e a classificação de risco de retenção devem refletir os dados computados pelo sistema. |

---

### Caso de Teste 04: Visualização das últimas entradas na academia.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C02-CT04 | Validar a listagem cronológica dos últimos acessos registrados na catraca/recepção. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem registros prévios de entrada de alunos no sistema. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na Página Inicial do SIFIT                    |
| **QUANDO** rolarmos a página até a seção "Últimas entradas na academia" |
| **ENTÃO** a tabela deve listar o nome do cliente, unidade e data/hora do acesso |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A lista de últimas entradas deve apresentar os registros em ordem cronológica de acesso. |