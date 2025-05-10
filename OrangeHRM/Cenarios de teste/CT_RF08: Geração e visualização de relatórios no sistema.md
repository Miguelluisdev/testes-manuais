## Cenário 08: Geração e visualização de relatórios no sistema.

### Caso de Teste 01: Gerar relatório de presença com filtros válidos.

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C08-CT01 | O sistema deve gerar corretamente um relatório de presença com filtros aplicados. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo "Reports". |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Reports > Attendance Summary\" |
| **E** seleciona um funcionário válido e um intervalo de datas     |
| **QUANDO** clicar em \"View\"                                     |
| **ENTÃO** o relatório de presença deve ser exibido na tela        |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O relatório deve apresentar os dados corretos conforme os filtros aplicados. |

---

### Caso de Teste 02: Gerar relatório sem selecionar filtros obrigatórios.

| ID       | Descrição                                                                     |
| :------- | :------------------------------------------------------------------------------ |
| C08-CT02 | O sistema deve exibir mensagem de erro ao tentar gerar relatório sem filtros obrigatórios. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Reports > Attendance Summary\" |
| **E** não preenche os campos obrigatórios (como nome do funcionário) |
| **QUANDO** clicar em \"View\"                                     |
| **ENTÃO** o sistema deve exibir uma mensagem de erro solicitando o preenchimento dos filtros |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve bloquear a geração do relatório e exibir erro claro. |

---

### Caso de Teste 03: Exportar relatório gerado em PDF.

| ID       | Descrição                                                               |
| :------- | :---------------------------------------------------------------------- |
| C08-CT03 | O sistema deve permitir exportar um relatório gerado no formato PDF.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Um relatório deve ter sido gerado previamente.                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário visualiza um relatório na tela           |
| **QUANDO** clicar na opção \"Export to PDF\"                    |
| **ENTÃO** o relatório deve ser baixado em formato PDF           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O download do arquivo PDF deve ocorrer com os dados exibidos na tela. |
