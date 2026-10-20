# CT_RF10_Contas_a_Receber.md

## Cenário 10: Gestão, Filtro e Baixa de Contas a Receber.

### Caso de Teste 01: Filtrar lançamentos financeiros por período e situação.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C10-CT01 | Validar a busca de títulos a receber utilizando filtros de data, status e cliente. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar autenticado e na tela de "Contas a Receber". |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Contas a Receber"                |
| **E** selecionamos a situação do título (ex: "Pendente", "Recebido" ou "Cancelado") |
| **E** informamos o intervalo de datas nos campos "Data Inicial" e "Data Final"      |
| **QUANDO** clicarmos no botão "Buscar"                             |
| **ENTÃO** a tabela deve listar apenas os lançamentos que correspondem aos filtros aplicados |
| **E** os cards devem recalcular os valores com base no filtro |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A listagem e os totais financeiros exibidos nos cards devem refletir exatamente o resultado do filtro aplicado. |

---

### Caso de Teste 02: Registrar recebimento/baixa manual de parcela.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C10-CT02 | Executar a baixa de uma mensalidade pendente informando o método de pagamento. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existir pelo menos uma conta pendente listada para o cliente. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Contas a Receber"                |
| **E** localizamos um título pendente na tabela                    |
| **E** clicamos no botão "Visualizar"                               |
| **E** clicamos no botão "Efetuar Recebimento"                     |
| **E** selecionamos o tipo de pagamento e o local do recebimento |
| **QUANDO** clicarmos em salvar                                     |
| **ENTÃO** a situação do título deve alterar para "Recebido"        |
| **E** o valor deve ser somado ao total recebido do dia/período     |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O título deve ser liquidado com sucesso e o histórico de pagamento devidamente registrado. |