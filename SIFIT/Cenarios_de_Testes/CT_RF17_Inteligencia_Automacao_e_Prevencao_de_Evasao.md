# CT_RF17_Inteligencia_Automacao_e_Prevencao_de_Evasao.md

## Cenário 17: Motor de Automações, Algoritmo de Prevenção de Evasão e Métricas de IA.

### Caso de Teste 01: Monitorizar e disparar automações de comunicação.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C17-CT01 | Validar a execução automática de regras de mensagem (ex: WhatsApp de aniversariantes e avisos de cobrança). |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Inteligência & Automação".        |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Inteligência & Automação"           |
| **E** verificamos as regras ativas de envio automático             |
| **QUANDO** o gatilho parametrizado for acionado (ex: data de aniversário do aluno ou parcelas em aberto) |
| **ENTÃO** o sistema deve disparar automaticamente a mensagem configurada via WhatsApp |
| **E** registar a notificação no histórico de automações executadas |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| As mensagens devem ser enviadas aos destinatários conforme as regras e gatilhos de automação ativos. |

---

### Caso de Teste 02: Consultar dashboard e indicadores consolidados de IA.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C17-CT03 | Visualizar métricas operacionais do motor de inteligência artificial. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O utilizador deve estar na tela de "Resultados IA".            |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de "Resultados IA"                |
| **QUANDO** o painel for atualizado                                 |
| **ENTÃO** o sistema deve exibir o total de automações executadas, relatórios enviados, quantidade de alunos monitorizados e a taxa média de frequência |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os indicadores exibidos devem refletir com precisão as execuções e dados recolhidos pelo motor de inteligência. |