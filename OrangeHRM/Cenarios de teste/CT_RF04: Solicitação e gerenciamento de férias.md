## Cenário 04: Solicitação e gerenciamento de férias.

### Caso de Teste 01: Solicitação de férias com datas válidas.

| ID       | Descrição                                                               |
| :------- | :---------------------------------------------------------------------- |
| C04-CT01 | O usuário deve conseguir solicitar férias informando um período válido. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e com acesso ao módulo "Leave".   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Leave\"                   |
| **E** clica em \"Apply\"                                         |
| **E** seleciona um tipo de licença (ex: Annual Leave)            |
| **E** escolhe um período válido de início e fim                 |
| **QUANDO** clicar em \"Apply\"                                   |
| **ENTÃO** a solicitação deve ser registrada com sucesso          |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A solicitação deve aparecer listada em \"My Leave\".            |

---

### Caso de Teste 02: Tentativa de solicitar férias sem selecionar tipo de licença.

| ID       | Descrição                                                                         |
| :------- | :-------------------------------------------------------------------------------- |
| C04-CT02 | O sistema deve impedir a solicitação de férias sem o tipo de licença selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e acessar a tela de aplicação de licença. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Leave\"                   |
| **E** clica em \"Apply\"                                         |
| **E** deixa o campo \"Leave Type\" em branco                    |
| **E** seleciona um período de data válido                       |
| **QUANDO** clicar em \"Apply\"                                   |
| **ENTÃO** uma mensagem de erro deve ser exibida solicitando o preenchimento do tipo de licença |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A aplicação deve ser bloqueada e o erro deve ser exibido ao usuário. |

---

### Caso de Teste 03: Visualizar status das solicitações de férias.

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C04-CT03 | O sistema deve exibir corretamente o status das férias solicitadas.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve ter ao menos uma solicitação de férias registrada. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"My Leave\"                |
| **QUANDO** a lista de solicitações for exibida                  |
| **ENTÃO** o status de cada solicitação (Aprovado, Pendente, Rejeitado) deve estar visível |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os status devem refletir corretamente o estado da solicitação.  |
