# CT_RF01_Autenticacao_e_Acesso.md

## Cenário 01: Autenticação e Acesso ao Sistema SIFIT.

### Caso de Teste 01: Autenticação com credenciais válidas e opção de persistência de sessão.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C01-CT01 | Efetuar login com dados válidos e validar o redirecionamento para a página inicial. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve possuir credenciais ativas cadastradas no SIFIT. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de login do SIFIT                    |
| **E** preenchemos as credenciais nos campos "Login" e "Senha"     |
| **E** opcionalmente marcamos a caixa de seleção "Manter conectado" |
| **QUANDO** clicarmos no botão "Entrar"                             |
| **ENTÃO** o sistema deve autenticar o usuário e redirecionar para a Página Inicial |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A sessão deve ser iniciada e a Página Inicial carregada com sucesso. |

---

### Caso de Teste 02: Validação de erros na autenticação com credenciais inválidas ou campos vazios.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C01-CT02 | Garantir o bloqueio de acesso ao submeter credenciais incorretas ou formulário em branco. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de login do SIFIT.                   |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de login do SIFIT                    |
| **E** informamos credenciais inválidas ou deixamos os campos "Login" e "Senha" em branco |
| **QUANDO** clicarmos no botão "Entrar"                             |
| **ENTÃO** o acesso deve ser negado e uma mensagem de alerta exibida ao usuário |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O sistema deve proibir a autenticação e indicar a falha de credenciais ou preenchimento. |

---

### Caso de Teste 03: Redirecionamento para o fluxo de redefinição de senha.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C01-CT03 | Validar o atalho "Esqueci minha senha" para recuperação de acesso. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário deve estar na tela de login do SIFIT.                   |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de login do SIFIT                    |
| **QUANDO** clicarmos no link "Esqueci minha senha"                 |
| **ENTÃO** o sistema deve redirecionar para a tela de redefinição de credenciais |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A tela de recuperação de senha deve ser exibida corretamente. |
