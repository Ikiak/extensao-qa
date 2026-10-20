## Cenário 01: Autenticação na plataforma SIFIT.

### Caso de Teste 01: Login com credenciais válidas.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C01-CT01 | O login será realizado com um nome de usuário e uma senha válidos. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| As credenciais fornecidas (usuário e senha) devem ser válidas. |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **E** preenchemos um usuário válido no campo "Login"               |
| **E** preenchemos uma senha válida no campo "Senha"               |
| **QUANDO** clicarmos no botão "Entrar"                             |
| **ENTÃO** seremos redirecionados para a Página Inicial do sistema  |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| O redirecionamento para a Página Inicial deve ocorrer com sucesso. |

---

### Caso de Teste 02: Tentativa de login com senha incorreta.

| ID        | Descrição                                                  |
| :-------- | :--------------------------------------------------------- |
| C01-CT02 | O login falhará quando a senha for inválida ou incorreta. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| O usuário informado deve existir no banco de dados do SIFIT.  |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **E** preenchemos um usuário válido no campo "Login"               |
| **E** preenchemos "senha_incorreta" no campo "Senha"               |
| **QUANDO** clicarmos no botão "Entrar"                             |
| **ENTÃO** uma mensagem de erro indicando credenciais inválidas será exibida |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A mensagem de erro de autenticação deve ser exibida ao usuário. |

---

### Caso de Teste 03: Tentativa de login com campos em branco.

| ID        | Descrição                                                          |
| :-------- | :----------------------------------------------------------------- |
| C01-CT03 | O login falhará quando os campos obrigatórios estiverem em branco. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Nenhuma.                                                     |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **E** deixamos os campos "Login" e "Senha" em branco               |
| **QUANDO** clicarmos no botão "Entrar"                             |
| **ENTÃO** A mensagem de erro de autenticação deve ser exibida ao usuário |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| Os campos obrigatórios devem indicar a necessidade de preenchimento. |

---

### Caso de Teste 04: Funcionalidade de recuperação de senha.

| ID        | Descrição                                                         |
| :-------- | :---------------------------------------------------------------- |
| C01-CT04 | Validação do fluxo do link "Esqueci minha senha" na tela de login. |

| **Pré-condições**                                              |
| :----------------------------------------------------------- |
| Nenhuma.                                                     |

| **Passos**                                                         |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **QUANDO** clicarmos no link "Esqueci minha senha"                |
| **ENTÃO** seremos redirecionados para a tela de redefinição/recuperação de credenciais |

| **Critérios de aceitação**                                       |
| :-------------------------------------------------------------- |
| A tela de redefinição de senha deve ser carregada corretamente. |