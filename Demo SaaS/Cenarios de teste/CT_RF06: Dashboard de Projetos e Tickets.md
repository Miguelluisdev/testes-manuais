# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Dashboard de Projetos e Tickets  
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 06: Visualizar e interagir com o dashboard de tickets

### Caso de Teste 01: Visualização de tickets com dados completos (Happy Path)

| ID       | Descrição                                                             |
| :------- | :-------------------------------------------------------------------- |
| C06-CT01 | O usuário deve visualizar uma lista de tickets com todos os dados esperados. |

| **Pré-condições**                                                                 |
| :-------------------------------------------------------------------------------- |
| O usuário deve estar autenticado e ter projetos/tickets cadastrados no sistema.   |

| **Passos**                                                                        |
| :-------------------------------------------------------------------------------- |
| **DADO** que estamos no dashboard do sistema                                      |
| **QUANDO** acessamos a seção de tickets                                           |
| **ENTÃO** devemos visualizar os seguintes dados por ticket:                      |
| - Email de quem reportou                                                         |
| - Título                                                                         |
| - Descrição                                                                      |
| - Status                                                                         |
| - Data de criação                                                                |

| **Critérios de aceitação**                                                        |
| :-------------------------------------------------------------------------------- |
| Todos os dados dos tickets devem ser exibidos corretamente em formato de tabela. |

### Caso de Teste 02: Falha ao carregar os tickets (Teste Negativo)

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C06-CT02 | O sistema deve exibir uma mensagem de erro se falhar ao carregar os tickets. |

| **Pré-condições**                                               |
| :-------------------------------------------------------------- |
| O usuário está autenticado.                                     |

| **Passos**                                                      |
| :-------------------------------------------------------------- |
| **DADO** que acessamos o dashboard                              |
| **E** ocorre um erro de servidor ou falha de conexão            |
| **QUANDO** os dados de tickets não forem carregados             |
| **ENTÃO** uma mensagem de erro deve ser exibida                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A interface deve exibir uma mensagem amigável e sugerir nova tentativa. |

### Caso de Teste 03: Verificar paginação com mínimo e máximo de registros (Valor Limite)

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C06-CT03 | A paginação deve funcionar corretamente com o número mínimo e máximo de tickets. |

| **Pré-condições**                                                    |
| :------------------------------------------------------------------- |
| O usuário está autenticado e há pelo menos 1 e no máximo 100 tickets criados. |

| **Passos**                                                           |
| :------------------------------------------------------------------- |
| **DADO** que temos tickets cadastrados no sistema                    |
| **QUANDO** navegamos entre páginas usando paginação                  |
| **ENTÃO** os registros devem ser carregados corretamente             |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------- |
| A funcionalidade de paginação deve carregar corretamente os registros, sem falhas ou repetições. |

### Caso de Teste 04: Buscar tickets usando palavra-chave (Caminho Alternativo)

| ID       | Descrição                                                               |
| :------- | :---------------------------------------------------------------------- |
| C06-CT04 | O usuário deve poder buscar um ticket usando palavras-chave.            |

| **Pré-condições**                                                     |
| :------------------------------------------------------------------ |
| O usuário está autenticado e há tickets com palavras-chave conhecidas. |

| **Passos**                                                           |
| :------------------------------------------------------------------ |
| **DADO** que estamos na lista de tickets                             |
| **QUANDO** digitamos uma palavra-chave no campo de busca             |
| **ENTÃO** apenas os tickets relevantes devem ser exibidos            |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------ |
| A busca deve retornar tickets correspondentes em tempo real (ou após clique em "Buscar"). |



