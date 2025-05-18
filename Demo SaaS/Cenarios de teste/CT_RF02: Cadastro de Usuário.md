# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Registro de novo usuário na plataforma  
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 02: Registro de novo usuário na plataforma

### Caso de Teste 01: Cadastro com todos os dados válidos (Happy Path)

| ID       | Descrição                                                                |
| :------- | :------------------------------------------------------------------------ |
| C02-CT01 | O sistema deve permitir o cadastro de um novo usuário com dados válidos. |

| **Pré-condições**                                                                   |
| :---------------------------------------------------------------------------------- |
| O usuário deve acessar a tela de cadastro ("Sign Up").                             |

| **Passos**                                                                          |
| :---------------------------------------------------------------------------------- |
| **DADO** que estamos na página de cadastro                                          |
| **E** preenchemos os campos obrigatórios com dados válidos (Nome, Sobrenome, Email, Senha) |
| **QUANDO** clicamos no botão "Cadastrar"                                           |
| **ENTÃO** o sistema deve criar a conta e redirecionar o usuário para o próximo passo (ex: criar organização) |

| **Critérios de aceitação**                                                          |
| :---------------------------------------------------------------------------------- |
| A conta deve ser criada e o usuário redirecionado corretamente.                    |

### Caso de Teste 02: Cadastro com dados inválidos (Teste Negativo)

| ID       | Descrição                                                                |
| :------- | :------------------------------------------------------------------------ |
| C02-CT02 | O sistema deve impedir o cadastro quando campos obrigatórios forem inválidos ou estiverem em branco. |

| **Pré-condições**                                                                   |
| :---------------------------------------------------------------------------------- |
| O usuário deve acessar a tela de cadastro.                                         |

| **Passos**                                                                          |
| :---------------------------------------------------------------------------------- |
| **DADO** que estamos na tela de cadastro                                            |
| **E** deixamos um ou mais campos obrigatórios em branco ou preenchidos de forma incorreta |
| **QUANDO** clicamos no botão "Cadastrar"                                           |
| **ENTÃO** o sistema deve exibir mensagens de erro claras e destacar os campos inválidos |

| **Critérios de aceitação**                                                          |
| :---------------------------------------------------------------------------------- |
| O sistema não deve permitir o cadastro até que todos os dados estejam válidos.     |

### Caso de Teste 03: Cadastro com senha no limite mínimo permitido (Valor Limite)

| ID       | Descrição                                                                |
| :------- | :------------------------------------------------------------------------ |
| C02-CT03 | O sistema deve aceitar senhas com exatamente 8 caracteres e 1 caractere especial. |

| **Pré-condições**                                                                   |
| :---------------------------------------------------------------------------------- |
| O usuário deve acessar a tela de cadastro.                                         |

| **Passos**                                                                          |
| :---------------------------------------------------------------------------------- |
| **DADO** que estamos na tela de cadastro                                            |
| **E** preenchemos todos os campos obrigatórios corretamente                         |
| **E** usamos uma senha com exatamente 8 caracteres, incluindo ao menos 1 caractere especial |
| **QUANDO** clicamos no botão "Cadastrar"                                           |
| **ENTÃO** o sistema deve criar a conta normalmente                                  |

| **Critérios de aceitação**                                                          |
| :---------------------------------------------------------------------------------- |
| O sistema deve aceitar senhas válidas no limite inferior de caracteres permitidos. |

### Caso de Teste 04: Cadastro utilizando conta do Google (Caminho Alternativo)

| ID       | Descrição                                                                |
| :------- | :------------------------------------------------------------------------ |
| C02-CT04 | O sistema deve permitir o cadastro através da conta do Google.           |

| **Pré-condições**                                                                   |
| :---------------------------------------------------------------------------------- |
| O botão "Cadastrar com Google" deve estar disponível e funcional.                  |

| **Passos**                                                                          |
| :---------------------------------------------------------------------------------- |
| **DADO** que estamos na página de cadastro                                          |
| **QUANDO** clicamos no botão "Cadastrar com Google"                                 |
| **E** escolhemos uma conta válida do Google                                         |
| **ENTÃO** o sistema deve concluir o cadastro e redirecionar o usuário              |

| **Critérios de aceitação**                                                          |
| :---------------------------------------------------------------------------------- |
| O sistema deve permitir cadastro com conta Google e redirecionar corretamente.     |

