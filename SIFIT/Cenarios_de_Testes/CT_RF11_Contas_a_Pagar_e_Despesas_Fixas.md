# CT_RF11_Contas_a_Pagar_e_Despesas_Fixas.md

## Cenário 11: Lançamento de Contas a Pagar e Controle de Despesas Fixas.

### Caso de Teste 01: Lançar nova conta a pagar.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C11-CT01 | Cadastrar uma nova obrigação financeira informando fornecedor, valor e vencimento. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Contas a Pagar".                  |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Contas a Pagar"                  |
| **E** clicamos no botão "Nova Conta"                               |
| **E** preenchemos a descrição da conta, o fornecedor, o valor, a data de vencimento e o local do pagamento |
| **QUANDO** confirmarmos o salvamento                               |
| **ENTÃO** o lançamento deve ser registrado com sucesso e exibido na listagem |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A conta a pagar deve ser salva na base de dados com as informações preenchidas. |

---

### Caso de Teste 02: Cadastrar despesa fixa com recorrência parametrizada.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C11-CT02 | Configurar uma nova despesa recorrente (Mensal, Diária ou Personalizada). |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Despesas Fixas".                 |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Despesas Fixas" |
| **E** clicamos no botão de "+"                       |
| **E** preenchemos o nome da despesa, o status ,o valor e o tipo de recorrência |
| **QUANDO** salvarmos a configuração                                |
| **ENTÃO** o sistema deve parametrizar a geração automática das parcelas futuras |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A despesa fixa recorrente deve constar no cadastro e gerar os lançamentos previstos nos períodos correspondentes. |

---

### Caso de Teste 03: Filtrar despesas por código, nome, status e tipo de recorrência.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C11-CT03 | Validar a busca e filtragem dos lançamentos de saída do sistema.   |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem contas a pagar e despesas cadastradas.             |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Contas a Pagar e Despesas Fixas" |
| **E** informamos o código ou nome da despesa no filtro de busca    |
| **E** selecionamos o status (Ativo/Inativo) e o tipo de recorrência desejado |
| **QUANDO** clicarmos no botão "Buscar"                             |
| **ENTÃO** a tabela deve atualizar exibindo apenas os lançamentos que atendem aos filtros |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os resultados listados na tabela devem corresponder exatamente aos parâmetros de pesquisa informados. |