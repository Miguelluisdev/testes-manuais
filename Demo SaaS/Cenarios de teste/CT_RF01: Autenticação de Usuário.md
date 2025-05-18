# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Autenticação de Usuário  
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 01: Autenticação de Usuário.

### Caso de Teste 01: Login com as credenciais válidas (Happy Path)

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C01-CT01 | O login será realizado com um email e uma senha válidos.              |

| **Pré-condições**                                                                |
| :------------------------------------------------------------------------------- |
| O usuário deve ter um cadastro ativo com email e senha válidos.                 |

| **Passos**                                                                       |
| :------------------------------------------------------------------------------- |
| **DADO** que estamos na página de login                                          |
| **E** preenchemos um email válido no campo de email                              |
| **E** preenchemos a senha correta no campo de senha                              |
| **QUANDO** clicarmos no botão "Login"                                            |
| **ENTÃO** o usuário deverá ser redirecionado para o Dashboard da aplicação       |

| **Critérios de aceitação**                                                       |
| :------------------------------------------------------------------------------- |
| O redirecionamento para o Dashboard deve ocorrer corretamente.                   |

### Caso de Teste 02: Login com credenciais inválidas (Teste Negativo)

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C01-CT02 | O sistema não deve permitir login com email ou senha inválidos.       |

| **Pré-condições**                                                                |
| :------------------------------------------------------------------------------- |
| O usuário deve estar na tela de login.                                           |

| **Passos**                                                                       |
| :------------------------------------------------------------------------------- |
| **DADO** que estamos na página de login                                          |
| **E** preenchemos um email inválido ou não cadastrado no campo de email         |
| **E** preenchemos uma senha incorreta                                            |
| **QUANDO** clicarmos no botão "Login"                                            |
| **ENTÃO** uma mensagem de erro clara deve ser exibida                            |

| **Critérios de aceitação**                                                       |
| :------------------------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro clara sem redirecionar o usuário.     |

### Caso de Teste 03: Login com valor limite nos campos (Valor Limite)

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C01-CT03 | O sistema deve validar os limites mínimos e máximos dos campos.        |

| **Pré-condições**                                                                |
| :------------------------------------------------------------------------------- |
| O usuário deve estar na tela de login.                                           |

| **Passos**                                                                       |
| :------------------------------------------------------------------------------- |
| **DADO** que estamos na página de login                                          |
| **E** inserimos um email com o menor número possível de caracteres válidos       |
| **E** inserimos uma senha com exatamente 8 caracteres válidos                    |
| **QUANDO** clicarmos em "Login"                                                  |
| **ENTÃO** o sistema deve permitir o acesso normalmente                           |

| **Critérios de aceitação**                                                       |
| :------------------------------------------------------------------------------- |
| O sistema deve aceitar entradas que respeitem os limites mínimos válidos.        |

### Caso de Teste 04: Login com conta Google (Caminho Alternativo)

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C01-CT04 | O sistema deve permitir login através da conta do Google.              |

| **Pré-condições**                                                                |
| :------------------------------------------------------------------------------- |
| O botão "Login com Google" deve estar disponível e configurado corretamente.     |

| **Passos**                                                                       |
| :------------------------------------------------------------------------------- |
| **DADO** que estamos na página de login                                          |
| **QUANDO** clicamos no botão "Login com Google"                                  |
| **E** escolhemos uma conta do Google válida                                      |
| **ENTÃO** o sistema deve autenticar e redirecionar para o Dashboard              |

| **Critérios de aceitação**                                                       |
| :------------------------------------------------------------------------------- |
| O sistema deve permitir autenticação via Google sem erros e redirecionar corretamente. |

