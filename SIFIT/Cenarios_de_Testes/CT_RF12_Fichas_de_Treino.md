# CT_RF12_Fichas_de_Treino.md

## Cenário 12: Prescrição de Fichas de Treino, Biblioteca de Exercícios e Parametrização.

### Caso de Teste 01: Criar e vincular nova ficha de treino para um aluno.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C12-CT01 | Elaborar e associar uma rotina de exercícios com período de validade a um aluno. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O aluno e o professor/personal devem estar cadastrados no sistema. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Fichas de Treino"                 |
| **E** clicamos no botão "Cadastrar Ficha"                               |
| **E** selecionamos o aluno destinatário, o personal, o objetivo do treino e o período de validade |
| **QUANDO** confirmarmos o salvamento                               |
| **ENTÃO** a nova ficha de treino deve ser gravada e vinculada ao perfil do aluno |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A ficha de treino deve ser armazenada com sucesso e ficar disponível para visualização.|

---

### Caso de Teste 02: Cadastrar novo exercício na biblioteca.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C12-CT02 | Incluir um novo movimento na biblioteca de exercícios categorizado por grupo muscular. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Exercícios".    |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Exercícios"                  |
| **E** clicamos no botão "Adicionar" no grupo muscular correspondente                  |
| **E** preenchemos o nome do exercício e as instruções de execução com mídias |
| **QUANDO** salvarmos o registo                                     |
| **ENTÃO** o exercício deve ser integrado à biblioteca e disponibilizado para montagem de fichas |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O exercício deve constar no catálogo geral e poder ser selecionado durante a prescrição de treinos. |

---

### Caso de Teste 03: Cadastrar e parametrizar um novo Grupo/Turma de Treino na agenda.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C12-CT03 | Criar um grupo de treino definindo dias, horários da agenda e parametrização de caixa. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Grupos ou Turmas de Treino".      |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Grupos ou Turmas de Treino"        |
| **E** clicamos no botão de criação de nova turma/grupo             |
| **E** informamos o nome do grupo (ex: Treino Livre, Personal, Turma dos Bodybuilders) |
| **E** definimos a agenda definindo os dias da semana e horários em que o treino ocorre |
| **QUANDO** confirmarmos o salvamento                               |
| **ENTÃO** o grupo de treino deve ser registrado na agenda operacional do sistema |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O grupo/turma de treino deve ser cadastrado com sua agenda e parâmetros de caixa devidamente configurados. |