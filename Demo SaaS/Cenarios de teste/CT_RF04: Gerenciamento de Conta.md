# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Gerenciar informações da conta do usuário 
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 04: Gerenciar informações da conta do usuário

### Caso de Teste 01: Atualizar nome e sobrenome com dados válidos (Happy Path)

| ID       | Descrição                                                             |
| :------- | :-------------------------------------------------------------------- |
| C04-CT01 | O usuário deve conseguir atualizar seu nome e sobrenome com sucesso. |

| **Pré-condições**                                                |
| :--------------------------------------------------------------- |
| O usuário deve estar autenticado e acessar a seção de perfil.    |

| **Passos**                                                       |
| :--------------------------------------------------------------- |
| **DADO** que estamos na seção de gerenciamento de conta          |
| **E** alteramos os campos "Nome" e "Sobrenome" com dados válidos |
| **QUANDO** clicamos em "Salvar alterações"                       |
| **ENTÃO** os dados devem ser atualizados com sucesso             |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de sucesso e refletir as alterações imediatamente. |

### Caso de Teste 02: Tentar alterar a senha com senha atual incorreta (Teste Negativo)

| ID       | Descrição                                                                     |
| :------- | :---------------------------------------------------------------------------- |
| C04-CT02 | O sistema deve impedir alteração de senha se a senha atual estiver incorreta. |

| **Pré-condições**                                                      |
| :--------------------------------------------------------------------- |
| O usuário deve estar autenticado e acessar a área de alteração de senha. |

| **Passos**                                                             |
| :--------------------------------------------------------------------- |
| **DADO** que estamos na seção de alteração de senha                    |
| **E** preenchemos a senha atual incorretamente                         |
| **E** inserimos nova senha e confirmação                              |
| **QUANDO** clicamos em "Alterar Senha"                                |
| **ENTÃO** o sistema deve exibir uma mensagem de erro e não permitir a alteração |

| **Critérios de aceitação**                                             |
| :--------------------------------------------------------------------- |
| A senha não deve ser alterada e o usuário deve ser informado claramente do erro. |

### Caso de Teste 03: Inserir nome com limite mínimo de caracteres (Valor Limite)

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C04-CT03 | O sistema deve permitir nomes com o mínimo de caracteres permitidos.      |

| **Pré-condições**                                                |
| :--------------------------------------------------------------- |
| O usuário deve estar autenticado e acessar a seção de perfil.    |

| **Passos**                                                       |
| :--------------------------------------------------------------- |
| **DADO** que estamos na seção de gerenciamento de conta          |
| **E** inserimos "A" no campo Nome e "B" no campo Sobrenome        |
| **QUANDO** clicamos em "Salvar alterações"                       |
| **ENTÃO** os dados devem ser atualizados normalmente             |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| O sistema deve aceitar valores no limite inferior permitido.     |

### Caso de Teste 04: Logout pelo gerenciamento de conta (Caminho Alternativo)

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C04-CT04 | O usuário deve conseguir realizar logout a partir da conta.   |

| **Pré-condições**                                                |
| :--------------------------------------------------------------- |
| O usuário deve estar autenticado e com sessão ativa.             |

| **Passos**                                                       |
| :--------------------------------------------------------------- |
| **DADO** que estamos na seção de gerenciamento de conta          |
| **QUANDO** clicamos no botão "Logout"                            |
| **ENTÃO** o sistema deve encerrar a sessão e redirecionar para a página de login |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| A sessão do usuário deve ser finalizada com segurança.           |

