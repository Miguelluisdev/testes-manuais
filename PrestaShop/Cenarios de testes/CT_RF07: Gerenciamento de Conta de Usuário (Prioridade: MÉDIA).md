# 🧪 Plano de Testes Manuais - Presta Shop 
> Funcionalidade: Busca de Produto (Prioridade: ALTA)  
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---


## Cenário 07: Gestão da Conta do Usuário

### Caso de Teste 01: Visualizar histórico de pedidos

| ID                          | Descrição                                        |
| :-------------------------- | :----------------------------------------------- |
| MYACC\_ORDERHIST\_VIEW\_001 | Usuário visualiza a lista de pedidos anteriores. |

| **Pré-condições**                      |
| :------------------------------------- |
| Usuário logado com pedidos anteriores. |

| **Passos**                                                                 |
| :------------------------------------------------------------------------- |
| **DADO** que o usuário logado está no painel da sua conta                  |
| **QUANDO** ele clica em "Histórico de Pedidos" (ou similar)                |
| **ENTÃO** uma lista de seus pedidos anteriores deve ser exibida, contendo: |
| - Número do pedido                                                         |
| - Data                                                                     |
| - Total                                                                    |
| - Status                                                                   |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------- |
| O sistema deve listar corretamente os pedidos anteriores do usuário. |

---

### Caso de Teste 02: Visualizar detalhes de um pedido específico

| ID                            | Descrição                                           |
| :---------------------------- | :-------------------------------------------------- |
| MYACC\_ORDERDETAIL\_VIEW\_001 | Usuário visualiza detalhes de um pedido específico. |

| **Pré-condições**                                 |
| :------------------------------------------------ |
| Usuário logado na página de histórico de pedidos. |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que o usuário está visualizando seu histórico de pedidos        |
| **QUANDO** ele clica em "Detalhes" de um pedido específico               |
| **ENTÃO** os detalhes completos do pedido devem ser exibidos, incluindo: |
| - Itens                                                                  |
| - Preços                                                                 |
| - Endereços                                                              |

| **Critérios de aceitação**                                        |
| :---------------------------------------------------------------- |
| O sistema deve mostrar todas as informações detalhadas do pedido. |

---

### Caso de Teste 03: Adicionar um novo endereço

| ID                       | Descrição                                 |
| :----------------------- | :---------------------------------------- |
| MYACC\_ADDRESS\_ADD\_001 | Usuário adiciona um novo endereço válido. |

| **Pré-condições** |
| :---------------- |
| Usuário logado.   |

| **Passos**                                                                              |
| :-------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na seção "Meus Endereços"                                   |
| **QUANDO** ele clica em "Adicionar novo endereço" (ou similar)                          |
| **E** preenche todos os campos obrigatórios do formulário de endereço com dados válidos |
| **E** clica em "Salvar"                                                                 |
| **ENTÃO** o novo endereço deve ser salvo e listado na seção "Meus Endereços".           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve salvar o endereço e mostrar na lista atualizada. |

---

### Caso de Teste 04: Editar um endereço existente

| ID                        | Descrição                        |
| :------------------------ | :------------------------------- |
| MYACC\_ADDRESS\_EDIT\_001 | Usuário edita um endereço salvo. |

| **Pré-condições**                     |
| :------------------------------------ |
| Usuário logado com um endereço salvo. |

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que o usuário está na seção "Meus Endereços"                       |
| **QUANDO** ele clica em "Editar" em um endereço existente                   |
| **E** modifica um ou mais campos (ex: número da rua)                        |
| **E** clica em "Salvar"                                                     |
| **ENTÃO** as alterações no endereço devem ser salvas e refletidas na lista. |

| **Critérios de aceitação**                                   |
| :----------------------------------------------------------- |
| O sistema deve atualizar o endereço e mostrar as alterações. |

---

### Caso de Teste 05: Excluir um endereço existente

| ID                          | Descrição                         |
| :-------------------------- | :-------------------------------- |
| MYACC\_ADDRESS\_DELETE\_001 | Usuário exclui um endereço salvo. |

| **Pré-condições**                                                                |
| :------------------------------------------------------------------------------- |
| Usuário logado com pelo menos dois endereços salvos (para não ficar sem nenhum). |

| **Passos**                                                  |
| :---------------------------------------------------------- |
| **DADO** que o usuário está na seção "Meus Endereços"       |
| **QUANDO** ele clica em "Excluir" em um endereço            |
| **E** confirma a exclusão (se houver pop-up de confirmação) |
| **ENTÃO** o endereço deve ser removido da lista.            |

| **Critérios de aceitação**                                   |
| :----------------------------------------------------------- |
| O sistema deve remover o endereço da lista após confirmação. |

---

### Caso de Teste 06: Editar informações pessoais

| ID                             | Descrição                                |
| :----------------------------- | :--------------------------------------- |
| MYACC\_PERSONALINFO\_EDIT\_001 | Usuário edita suas informações pessoais. |

| **Pré-condições** |
| :---------------- |
| Usuário logado.   |

| **Passos**                                                            |
| :-------------------------------------------------------------------- |
| **DADO** que o usuário está na seção "Minhas Informações Pessoais"    |
| **QUANDO** ele altera seu sobrenome                                   |
| **E** insere a senha atual para confirmar (se exigido)                |
| **E** clica em "Salvar"                                               |
| **ENTÃO** as informações pessoais devem ser atualizadas corretamente. |

| **Critérios de aceitação**                                    |
| :------------------------------------------------------------ |
| O sistema deve atualizar as informações pessoais com sucesso. |
