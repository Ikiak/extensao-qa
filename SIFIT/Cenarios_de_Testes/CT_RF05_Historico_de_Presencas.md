# CT_RF05_Historico_de_Presencas.md

## Cenário 05: Consulta e filtragem do Histórico de Presenças.

### Caso de Teste 01: Filtrar presenças por intervalo de datas e cliente.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C05-CT01 | Validar a busca de registos de presença utilizando filtros de período e nome de cliente. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Existirem registos de presenças salvos na base de dados para o período selecionado. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos no menu "Presenças"                           |
| **E** preenchemos o nome do cliente no campo de busca              |
| **E** definimos os campos de data "De" e "Até"                    |
| **QUANDO** clicarmos no botão "Buscar"                             |
| **ENTÃO** a tabela deve listar apenas os registos correspondentes aos critérios informados |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A listagem de presenças deve refletir rigorosamente o período de datas e o cliente filtrado. |

---

### Caso de Teste 02: Utilização de atalhos rápidos de período (Hoje, Esta semana, Este mês).

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C05-CT02 | Validar o preenchimento automático dos filtros de data através dos botões de atalho. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Presenças".                     |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos no menu "Presenças"                           |
| **QUANDO** clicarmos no atalho "Esta semana" ou "Este mês"         |
| **ENTÃO** os campos de data "De" e "Até" devem ser preenchidos automaticamente com o intervalo correspondente |
| **E** a busca deve ser executada atualizando os indicadores do período (Total no período, Alunos distintos, Média por dia, Dias no período) |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os atalhos rápidos devem configurar as datas corretamente e recalcular as estatísticas exibidas nos cards superiores. |