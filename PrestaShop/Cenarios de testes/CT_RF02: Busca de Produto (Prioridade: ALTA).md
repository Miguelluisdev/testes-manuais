# 🧪 Plano de Testes Manuais - Presta Shop 
> Funcionalidade: Busca de Produto (Prioridade: ALTA)  
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---

## Cenário 02.1: Busca por nome exato do produto

### Caso de Teste 01: Busca com nome exato do produto

| ID                | Descrição                                                 |
| :---------------- | :-------------------------------------------------------- |
| SEARCH\_NAME\_001 | Busca realizada com o nome exato de um produto existente. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve conhecer o nome exato de um produto existente. |

| **Passos**                                                                                       |
| :----------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está em qualquer página com o campo de busca visível                      |
| **QUANDO** ele digita o nome exato de um produto existente no campo de busca                     |
| **E** pressiona Enter ou clica no botão de busca                                                 |
| **ENTÃO** a página de resultados deve ser exibida                                                |
| **E** o produto buscado deve estar listado entre os primeiros resultados (idealmente o primeiro) |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A busca retorna o produto correto entre os primeiros resultados |

---

## Cenário 02.2: Busca por termo parcial do produto

### Caso de Teste 02: Busca com termo parcial no nome do produto

| ID                   | Descrição                                                  |
| :------------------- | :--------------------------------------------------------- |
| SEARCH\_PARTIAL\_001 | Busca realizada com parte do nome de um produto existente. |

| **Pré-condições**                 |
| :-------------------------------- |
| O usuário está no campo de busca. |

| **Passos**                                                                                         |
| :------------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está no campo de busca                                                      |
| **QUANDO** ele digita uma parte do nome do produto (ex: "Mug")                                     |
| **E** submete a busca                                                                              |
| **ENTÃO** a página de resultados exibe produtos que contenham o termo parcial no nome ou descrição |

| **Critérios de aceitação**                                   |
| :----------------------------------------------------------- |
| Resultados exibem produtos que correspondem ao termo parcial |

---

## Cenário 02.3: Busca por SKU (se aplicável)

### Caso de Teste 03: Busca com SKU do produto

| ID               | Descrição                                                 |
| :--------------- | :-------------------------------------------------------- |
| SEARCH\_SKU\_001 | Busca realizada utilizando o SKU de um produto existente. |

| **Pré-condições**                            |
| :------------------------------------------- |
| O usuário deve conhecer o SKU de um produto. |

| **Passos**                                                 |
| :--------------------------------------------------------- |
| **DADO** que o usuário está no campo de busca              |
| **QUANDO** ele digita o SKU do produto                     |
| **E** submete a busca                                      |
| **ENTÃO** o produto correspondente ao SKU deve ser exibido |

| **Critérios de aceitação**                     |
| :--------------------------------------------- |
| O produto correto é exibido ao buscar pelo SKU |

---

## Cenário 02.4: Busca por termo inexistente

### Caso de Teste 04: Busca com termo sem correspondência

| ID                       | Descrição                                                      |
| :----------------------- | :------------------------------------------------------------- |
| SEARCH\_NONEXISTENT\_001 | Busca realizada com termo que não corresponde a nenhum produto |

| **Pré-condições**                 |
| :-------------------------------- |
| O usuário está no campo de busca. |

| **Passos**                                                                                     |
| :--------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está no campo de busca                                                  |
| **QUANDO** ele digita um termo inexistente (ex: "asdfghjkl")                                   |
| **E** submete a busca                                                                          |
| **ENTÃO** uma mensagem amigável "Nenhum resultado encontrado para '\[termo]'" deve ser exibida |

| **Critérios de aceitação**                                  |
| :---------------------------------------------------------- |
| Exibição de mensagem clara informando que não há resultados |

---

## Cenário 02.5: Busca com sugestões (Autocomplete) - se implementado

### Caso de Teste 05: Sugestões de busca enquanto digita

| ID                        | Descrição                                                   |
| :------------------------ | :---------------------------------------------------------- |
| SEARCH\_AUTOCOMPLETE\_001 | Sugestões de produtos exibidas ao digitar no campo de busca |

| **Pré-condições**                 |
| :-------------------------------- |
| O usuário está no campo de busca. |

| **Passos**                                                           |
| :------------------------------------------------------------------- |
| **DADO** que o usuário está no campo de busca                        |
| **QUANDO** ele começa a digitar o nome de um produto (ex: "Humming") |
| **ENTÃO** uma lista de sugestões contendo o termo deve aparecer      |
| **E** clicar em uma sugestão leva à PDP do produto ou executa busca  |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------- |
| As sugestões são relevantes e clicáveis, levando ao produto ou busca |

---

## Cenário 02.6: Busca vazia

### Caso de Teste 06: Busca sem digitar termo

| ID                 | Descrição                                              |
| :----------------- | :----------------------------------------------------- |
| SEARCH\_EMPTY\_001 | Submissão da busca sem digitar termo no campo de busca |

| **Pré-condições**                 |
| :-------------------------------- |
| O usuário está no campo de busca. |

| **Passos**                                                                                                                                       |
| :----------------------------------------------------------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está no campo de busca                                                                                                    |
| **QUANDO** ele clica no botão de busca sem digitar termo                                                                                         |
| **ENTÃO** o sistema exibe todos os produtos, ou uma mensagem solicitando termo, ou permanece na página atual (depende do comportamento definido) |

| **Critérios de aceitação**                                        |
| :---------------------------------------------------------------- |
| Sistema responde conforme comportamento esperado para busca vazia |
