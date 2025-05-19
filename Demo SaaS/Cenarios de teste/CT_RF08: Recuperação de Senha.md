# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Recuperação de Senha 
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 08: Recuperação de senha pelo email cadastrado

### Caso de Teste 01: Solicitar recuperação de senha com email válido (Happy Path)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C08-CT01 | O sistema deve permitir solicitar recuperação de senha com email cadastrado. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário está na tela de login do sistema.                              |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela de login                                 |
| **E** clicamos em "Esqueceu a senha?"                                 |
| **E** inserimos um email válido cadastrado no campo de email          |
| **QUANDO** clicamos em "Enviar"                                       |
| **ENTÃO** o sistema envia email com instruções para redefinir a senha |
| **E** exibe mensagem confirmando envio do email                      |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Email com instruções é enviado e mensagem de confirmação é exibida.    |

---

### Caso de Teste 02: Solicitar recuperação de senha com email não cadastrado (Teste Negativo)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C08-CT02 | O sistema deve mostrar mensagem de erro quando o email não existir. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário está na tela de recuperação de senha.                         |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela "Esqueceu a senha?"                     |
| **E** inserimos um email que não está cadastrado                     |
| **QUANDO** clicamos em "Enviar"                                       |
| **ENTÃO** o sistema exibe mensagem de erro informando que email não existe |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Mensagem clara de erro sobre email inválido é exibida.                  |

---

### Caso de Teste 03: Inserção de email com tamanho máximo permitido (Valor Limite)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C08-CT03 | O sistema deve aceitar emails com o tamanho máximo permitido.      |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário está na tela de recuperação de senha.                         |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela "Esqueceu a senha?"                     |
| **E** inserimos um email com o comprimento máximo suportado pelo sistema |
| **QUANDO** clicamos em "Enviar"                                       |
| **ENTÃO** o sistema processa a solicitação normalmente e envia email   |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Email é aceito e email de recuperação é enviado normalmente.           |

---

### Caso de Teste 04: Cancelar recuperação de senha e retornar à tela de login (Caminho Alternativo)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C08-CT04 | O sistema deve permitir ao usuário cancelar a recuperação e voltar à tela de login. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário está na tela "Esqueceu a senha?".                            |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela "Esqueceu a senha?"                     |
| **E** clicamos no botão "Cancelar"                                   |
| **QUANDO** o sistema retorna para a tela de login                     |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Tela de login é exibida e nenhuma ação de recuperação é realizada.     |

