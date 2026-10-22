# CT_RF18_Configuracoes_Gerais_e_Modelos_de_Ficha.md

## Cenário 18: Parametrização Global do Sistema e Gestão de Modelos de Ficha de Treino.

### Caso de Teste 01: Parametrizar Configurações Globais do Sistema em abas.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C18-CT01 | Ajustar parâmetros operacionais, integração biométrica, avaliações, mensagens, pagamentos e design. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Configurações".                    |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Configurações"                    |
| **E** na aba "Home", definimos as regras de acesso, presença, inatividade, cobrança de multa/juros e anamnese na matrícula |
| **E** na aba "Biometria", configuramos a marca/modelo do aparelho, dados de rede (IP, Porta) e credenciais da catraca |
| **E** na aba "Avaliação", parametrizamos a cobrança e o protocolo de teste físico (ex: Dobras) |
| **E** na aba "Aniversário", habilitamos os canais de envio (WhatsApp, SMS, E-mail) com variáveis personalizadas |
| **E** nas abas "Pagamento" e "Integrações", inserimos os tokens da Pagar.me e as credenciais do WhatsApp (Evolution API) |
| **E** na aba "Design", personalizamos as cores da interface e realizamos o upload do Logo e Capa |
| **QUANDO** clicarmos em "Salvar Configurações"                     |
| **ENTÃO** o sistema deve gravar os parâmetros e aplicá-los globalmente na plataforma |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Todas as configurações registradas nas abas operacionais e visuais devem ser mantidas e refletidas no sistema. |

---

### Caso de Teste 02: Cadastrar e gerenciar Modelos de Ficha de Treino.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C18-CT02 | Criar e consultar modelos padronizados de ficha de treino por personal responsável. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de "Modelos de Ficha".                 |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Modelos de Ficha"                 |
| **E** clicamos no botão "+"                  |
| **E** no modal "Novo Modelo de Ficha", preenchemos o Nome do Modelo (ex: "Hipertrofia — Nível Avançado") e selecionamos o Personal |
| **QUANDO** clicarmos no botão "Criar Modelo"                       |
| **ENTÃO** o modelo de ficha deve ser gravado e listado na tabela principal |
| **E** permitir a filtragem por Código, Título do modelo ou Criador |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O modelo de ficha deve ser salvo corretamente com seu personal associado e exibido na listagem. |

---

### Caso de Teste 03: Gerir comunicação e publicações no Aplicativo Mobile.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C18-CT03 | Disparar notificações push, publicar avisos na linha do tempo e moderar denúncias. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Aplicativo".    |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Aplicativo"        |
| **E** elaboramos uma notificação push e um aviso para a linha do tempo dos alunos |
| **E** revisamos o painel de moderação de denúncias da comunidade  |
| **QUANDO** enviarmos a comunicação                                 |
| **ENTÃO** o sistema deve disparar as notificações push para os dispositivos móveis |
| **E** publicar os avisos no feed do aplicativo dos alunos          |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| As notificações push e comunicados devem ser entregues aos utilizadores da aplicação móvel. |