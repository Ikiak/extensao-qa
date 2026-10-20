# CT_RF08_Gestao_de_Matriculas.md

## Cenário 08: Gestão de Matrículas, Contratos e Renovações.

### Caso de Teste 01: Registar nova matrícula para aluno existente.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C08-CT01 | Vincular um plano ativo a um aluno sem matrícula vigente.          |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O cliente deve estar previamente cadastrado no sistema.      |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Matrículas"                      |
| **E** clicamos no botão "Cadastrar Matrícula"                      |
| **E** selecionamos o aluno e a modalidade pretendida               |
| **QUANDO** efetuarmos a confirmação da matrícula                   |
| **ENTÃO** o sistema deve gerar as parcelas financeiras e ativar o contrato |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A matrícula deve assumir o estado "ATIVO" e gerar os devidos débitos em Contas a Receber. |

---

### Caso de Teste 02: Consulta e validação de contratos ativos no período.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C08-CT02 | Validar a listagem de matrículas ativas e métricas de desempenho. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Matrículas".                  |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Matrículas"                      |
| **QUANDO** o painel for totalmente carregado                      |
| **ENTÃO** os indicadores superiores devem exibir as métricas de "Matrículas Ativas", "Recorrentes", "Não Renovadas" e "Cadastradas no Mês" |
| **E** a tabela principal deve listar os contratos encontrados com opções de visualização, cancelamento e exclusão|

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os dados exibidos na tabela e nos cards de resumo devem corresponder aos registos atuais da base. |