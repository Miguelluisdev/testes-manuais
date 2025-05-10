## Cenário 10: Funcionalidade de Manutenção do Sistema.

### Caso de Teste 01: Verificar acesso ao sistema durante manutenção programada.

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C10-CT01 | O sistema deve informar ao usuário sobre a manutenção programada e impedir o acesso. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O sistema deve estar em modo de manutenção programada.        |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o sistema está em modo de manutenção programada    |
| **E** o usuário tenta acessar qualquer funcionalidade           |
| **QUANDO** o usuário tentar acessar o sistema                   |
| **ENTÃO** o sistema deve exibir uma mensagem informando que está em manutenção |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir uma mensagem clara de manutenção e bloquear o acesso às funcionalidades. |

---

### Caso de Teste 02: Acessar o sistema após término da manutenção.

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C10-CT02 | O sistema deve permitir o acesso normalmente após o término da manutenção. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O sistema deve ter concluído a manutenção programada.         |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o sistema não está mais em manutenção              |
| **E** o usuário tenta acessar a página inicial do sistema       |
| **QUANDO** o usuário tentar acessar o sistema                   |
| **ENTÃO** o sistema deve permitir o acesso normal, sem mensagens de manutenção |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O usuário deve ser capaz de acessar o sistema normalmente.      |

---

### Caso de Teste 03: Exibir status de manutenção em caso de falha inesperada.

| ID       | Descrição                                                               |
| :------- | :------------------------------------------------------------------------ |
| C10-CT03 | O sistema deve exibir uma mensagem de manutenção caso haja uma falha inesperada no sistema. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O sistema deve estar em modo de operação com falha.           |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que ocorre uma falha inesperada no sistema              |
| **E** o usuário tenta acessar o sistema                          |
| **QUANDO** o usuário acessar a página inicial                   |
| **ENTÃO** o sistema deve exibir uma mensagem de falha inesperada, informando sobre a manutenção |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir uma mensagem clara de falha e manutenção, informando que o sistema está indisponível. |
