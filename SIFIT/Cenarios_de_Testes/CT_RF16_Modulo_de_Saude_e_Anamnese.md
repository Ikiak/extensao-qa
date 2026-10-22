# CT_RF16_Modulo_de_Saude_e_Anamnese.md

## Cenário 16: Gestão de Fichas de Anamnese e Histórico de Saúde dos Alunos.

### Caso de Teste 01: Cadastrar modelo de ficha de anamnese e categorização.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C16-CT01 | Criar um modelo de questionário de saúde organizado por categorias. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Modelos de Anamnese".          |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Modelos de Anamnese"             |
| **E** clicamos no botão "Novo Modelo"                              |
| **E** informamos o nome do modelo e definimos a categoria |
| **QUANDO** salvarmos a estrutura do modelo                         |
| **ENTÃO** o modelo de anamnese deve ser registado e ficar disponível para aplicação |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O modelo deve ser gravado na base de dados com as suas respetivas categorias. |

---

### Caso de Teste 02: Configurar banco de perguntas com formatos de resposta variados.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C16-CT02 | Adicionar perguntas personalizadas e definir o tipo de resposta esperada. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Perguntas Anamnese".           |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Perguntas Anamnese"               |
| **E** clicamos no botão "Nova Pergunta"                            |
| **E** inserimos o nome, status e enunciado da questão |
| **E** definimos o tipo de resposta |
| **QUANDO** confirmarmos o salvamento                               |
| **ENTÃO** a pergunta deve ser integrada ao catálogo  |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A pergunta deve ser armazenada com o tipo de resposta parametrizado. |

---

### Caso de Teste 03: Aplicar ficha de anamnese no momento da matrícula do aluno.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C16-CT03 | Preencher e vincular o questionário de saúde ao registo do aluno.  |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O aluno deve estar com perfil ativo. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Visualizar Cliente"  |
| **E** selecionamos a opção de "Aplicar Anamnese" |
| **E** respondemos às questões apresentadas |
| **QUANDO** finalizarmos o preenchimento                            |
| **ENTÃO** a ficha de anamnese deve ser gravada e vinculada ao histórico do aluno |
| **E** os alertas de lesões ou restrições de saúde devem ficar visíveis no perfil |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| As respostas de saúde devem ser associadas permanentemente ao registo do aluno para consulta do avaliador/instrutor. |