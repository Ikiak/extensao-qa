# CT_RF14_Modulo_Comercial.md

## Cenário 14: CRM de Prospecção de Leads, Gestão de Planos, Modelos de Contrato e Formas de Pagamento.

### Caso de Teste 01: Adicionar e gerenciar Lead na listagem de Prospecção (CRM).

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C14-CT01 | Cadastrar um novo lead através do modal e consultar/atualizar seu estágio na tabela de prospecção. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Prospecção".                |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Prospecção"                 |
| **E** clicamos no botão "Adicionar Lead"                           |
| **E** no modal "Adicionar Lead", preenchemos os dados do lead (Nome, Estágio, E-mail, Telefone e Observação) e clicamos em "Salvar Lead" |
| **QUANDO** consultarmos a tabela de Prospecção ou utilizarmos os filtros de busca por nome/estágio |
| **ENTÃO** o novo lead deve ser exibido na tabela com seu respectivo estágio e data de criação |
| **E** deve permitir a visualização de detalhes e atualização das informações do lead |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O lead deve ser gravado com sucesso e constar na listagem da tabela conforme o estágio e os filtros aplicados. |

---

### Caso de Teste 02: Cadastrar e parametrizar um novo Plano comercial.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C14-CT02 | Criar e parametrizar um plano comercial informando dados, valores, equipe/dependentes e benefícios. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Planos".                         |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Planos"                           |
| **E** clicamos no botão "Novo Plano"                               |
| **E** no modal "Novo Plano", preenchemos os "Dados do Plano" (Código, Nome, Grupo, Status) |
| **E** preenchemos "Contrato e Valores" (Cobrança, Parcelas, Valor Mensal, Valor Matrícula) |
| **E** definimos os parâmetros de "Equipe e Dependentes" (Personal, Função dos Professores, Dependentes) e "Benefícios" |
| **E** opcionalmente acionamos a opção "Salvar também na Pagar.me"  |
| **QUANDO** clicarmos no botão "Salvar Plano"                       |
| **ENTÃO** o plano deve ser registrado e exibido na listagem de planos ativos |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O plano deve ser salvo com suas regras comerciais, limites de dependentes e integração parametrizada. |

---

### Caso de Teste 03: Criar e parametrizar Modelo de Contrato com variáveis dinâmicas.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C14-CT03 | Cadastrar uma minuta contratual inserindo variáveis de aluno, plano, academia e contrato. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Modelos de Contrato".             |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Modelos de Contrato"             |
| **E** clicamos na opção para adicionar modelo                     |
| **E** preenchemos o "Título do modelo" e confirmamos o Status "Ativo" |
| **E** elaboramos o "Texto do contrato" utilizando o editor de texto e inserindo as variáveis disponíveis (Dados do aluno, do plano, da academia e do contrato) |
| **E** validamos a estrutura do documento no quadro de "Pré-visualização do contrato" |
| **QUANDO** clicarmos em "Salvar modelo"                            |
| **ENTÃO** a minuta deve ser registrada e disponibilizada para emissão de contratos de alunos |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O modelo de contrato deve ser salvo com as variáveis dinâmicas configuradas para substituição no momento da impressão. |