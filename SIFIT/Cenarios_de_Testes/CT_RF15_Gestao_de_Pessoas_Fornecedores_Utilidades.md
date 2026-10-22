# CT_RF15_Gestao_de_Pessoas_Fornecedores_Utilidades.md

## Cenário 15: Gestão de Colaboradores, Funções, Fornecedores, Tipos de Documentos, Atividades, Produtos e Enquetes.

### Caso de Teste 01: Cadastrar novo Colaborador e gerenciar Funções.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C15-CT01 | Inserir colaborador com dados pessoais, documentos, login e endereço, e gerenciar/visualizar funções. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Cadastrar Colaborador" ou "Funções". |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de cadastrar colaborador              |
| **E** definimos a permissão de Login (Admin, Normal, Sem login) e a indicação de Avaliador (Sim/Não) |
| **E** preenchemos os Dados Principais (Código, Nome, Status, Data de Nascimento, Sexo, Tipo Sanguíneo), Documentos (CPF, RG, CREF), Cadastro de Login, Dados para Contato e Endereço |
| **E** salvamos o colaborador                                       |
| **E** acessamos a tela de "Funções" para criar uma "Nova Função" (definindo Nome, Tipo de Funcionário, Personal e Avaliador) |
| **QUANDO** clicarmos na lupa de ações de uma colaborador listado        |
| **ENTÃO** o sistema deve abrir o modal "Função" exibindo em modo leitura os dados cadastrados (Código, Nome, Tipo do Funcionário, Avaliador e Personal) |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O colaborador deve ser salvo com suas credenciais e a função visualizada corretamente no modal de detalhes. |

---

### Caso de Teste 02: Cadastrar Fornecedor e gerenciar Tipos de Documentos.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C15-CT02 | Mapear um novo fornecedor via modal e parametrizar a aplicação dos tipos de documentos no sistema. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Fornecedores" ou "Tipos de Documentos". |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Fornecedores"                     |
| **E** clicamos para adicionar um "Novo Fornecedor"                 |
| **E** no modal, definimos o Tipo de Pessoa (Física/Jurídica), Dados Principais (Nome, Status), Documentos (CNPJ/CPF), Contato, Endereço e Observação |
| **E** salvamos o fornecedor                                        |
| **QUANDO** acessarmos a tela de "Tipos de Documentos"              |
| **ENTÃO** o sistema deve listar os documentos cadastrados exibindo a tag de Aplicação (ex: "Colaborador" ou "Conta / Fornecedor") |
| **E** permitir a filtragem por Código, Nome ou Aplicação           |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O fornecedor deve ser cadastrado e os tipos de documento devidamente associados à sua aplicação operacional. |

---

### Caso de Teste 03: Cadastrar Atividades, Produtos (Venda/Pontuação) e Enquetes.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C15-CT03 | Gerenciar a tabela de Atividades com pontuação, cadastrar Produtos por modal e monitorar Enquetes. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar nas telas de "Atividades", "Produtos" ou "Enquetes". |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Atividades"                       |
| **E** cadastramos e consultamos as tarefas definindo Nome, Descrição e a Pontuação atribuída (ex: 100, 200, 300 pts) |
| **E** na tela de "Produtos", clicamos em "Novo"                    |
| **E** no modal "Produto", preenchemos Código, Nome, Status, Descrição, Tipo (Venda ou Pontuação), Preço/Pontos e realizamos o upload da Imagem |
| **E** salvamos o produto                                           |
| **QUANDO** acessarmos a tela de "Enquetes"                         |
| **ENTÃO** a tabela deve listar as pesquisas registradas exibindo Código, Nome, Pergunta e Status (Ativo/Inativo) |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| As atividades com pontos, os produtos para venda/resgate e as enquetes devem ser devidamente gravados e apresentados nas tabelas operacionais. |