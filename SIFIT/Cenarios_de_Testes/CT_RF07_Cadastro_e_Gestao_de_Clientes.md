# CT_RF07_Cadastro_e_Gestao_de_Clientes.md

## Cenário 07: Gestão, consulta e cadastro de clientes da academia.

### Caso de Teste 01: Cadastrar um novo cliente com sucesso.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C07-CT01 | Inclusão de um novo aluno preenchendo os dados obrigatórios e pessoais. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O operador deve possuir permissão para gestão de clientes.   |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Clientes"                         |
| **E** clicamos no botão "Novo Cliente"                             |
| **E** preenchemos o nome, dados de contato, CPF e demais dados necessários        |
| **QUANDO** confirmarmos o salvamento do formulário                 |
| **ENTÃO** o novo cliente deve ser registado com sucesso e exibido na listagem principal |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O registo do cliente deve ser persistido na base de dados e listar na pesquisa. |

---

### Caso de Teste 02: Pesquisar e filtrar clientes por critérios múltiplos.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C07-CT02 | Validar a busca de clientes por Código, Nome, Estado, Situação e Plano. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem clientes previamente cadastrados no sistema.        |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Clientes"                         |
| **E** digitamos o nome do cliente no campo de busca                |
| **E** selecionamos o estado "Ativo" e a situação "Adimplente"      |
| **QUANDO** clicarmos no botão "Buscar"                             |
| **ENTÃO** a tabela deve filtrar e apresentar apenas os clientes que correspondem a todos os critérios aplicados |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os resultados listados devem respeitar exatamente os filtros aplicados. |

---

### Caso de Teste 03: Visualização dos indicadores de clientes nos cards operacionais.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C07-CT03 | Validar os contadores operacionais da tela de gestão de clientes.   |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Clientes".                     |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Clientes"                         |
| **QUANDO** a página for totalmente carregada                      |
| **ENTÃO** os cards superiores devem apresentar a contagem exata de "Clientes Cadastrados", "Clientes Ativos", "Sem Matrícula" e "Ausentes" |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os contadores dos cards devem corresponder ao somatório real dos dados na base do sistema. |