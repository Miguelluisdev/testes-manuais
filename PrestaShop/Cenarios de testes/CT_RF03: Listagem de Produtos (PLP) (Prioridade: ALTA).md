# 🧪 Plano de Testes Manuais - Presta Shop
> Funcionalidade:  Listagem de Produtos (PLP) (Prioridade: ALTA)
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---

## Cenário 03.1: Navegar para uma página de categoria

### Caso de Teste 01: Navegar para página de categoria via menu principal

| ID            | Descrição                                                      |
| :------------ | :------------------------------------------------------------- |
| PLP\_NAV\_001 | Navegação para página de listagem de produtos a partir do menu |

| **Pré-condições**                                                      |
| :--------------------------------------------------------------------- |
| Usuário está na homepage ou qualquer página com menu principal visível |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que o usuário está na homepage ou página com menu principal     |
| **QUANDO** ele clica no link de uma categoria no menu (ex: "Clothes")    |
| **ENTÃO** a página de listagem de produtos para essa categoria é exibida |
| **E** os produtos daquela categoria são listados                         |
| **E** o breadcrumb reflete a navegação (ex: Home > Clothes)              |

| **Critérios de aceitação**                                                       |
| :------------------------------------------------------------------------------- |
| Página correta da categoria carregada com produtos visíveis e breadcrumb correto |

---

## Cenário 03.2: Aplicar filtro de atributo (ex: Cor)

### Caso de Teste 02: Aplicar filtro de atributo em PLP

| ID                     | Descrição                                                       |
| :--------------------- | :-------------------------------------------------------------- |
| PLP\_FILTER\_ATTR\_001 | Aplicação de filtro de atributo (ex: cor) na página de listagem |

| **Pré-condições**                                                  |
| :----------------------------------------------------------------- |
| Usuário está em uma PLP que possui filtros de atributo disponíveis |

| **Passos**                                                                                     |
| :--------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está em uma PLP                                                         |
| **QUANDO** ele seleciona um valor de filtro (ex: Cor "Branco")                                 |
| **ENTÃO** a lista de produtos é atualizada mostrando só os produtos que correspondem ao filtro |
| **E** o filtro aplicado é indicado visualmente                                                 |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| Produtos listados respeitam o filtro; indicação visual do filtro |

---

## Cenário 03.3: Aplicar múltiplos filtros combinados (ex: Cor e Tamanho)

### Caso de Teste 03: Aplicar filtros combinados em PLP

| ID                      | Descrição                                                     |
| :---------------------- | :------------------------------------------------------------ |
| PLP\_FILTER\_MULTI\_001 | Aplicação de múltiplos filtros combinados (ex: Cor + Tamanho) |

| **Pré-condições**                               |
| :---------------------------------------------- |
| Usuário está em uma PLP com filtros disponíveis |

| **Passos**                                                  |
| :---------------------------------------------------------- |
| **DADO** que o usuário está em uma PLP                      |
| **QUANDO** ele seleciona um filtro de Cor (ex: "Preto")     |
| **E** seleciona um filtro de Tamanho (ex: "M")              |
| **ENTÃO** a lista mostra produtos que são Preto E tamanho M |

| **Critérios de aceitação**                             |
| :----------------------------------------------------- |
| Produtos exibidos respeitam ambos os filtros aplicados |

---

## Cenário 03.4: Limpar/Resetar filtros aplicados

### Caso de Teste 04: Limpar filtros na PLP

| ID                      | Descrição                                                |
| :---------------------- | :------------------------------------------------------- |
| PLP\_FILTER\_CLEAR\_001 | Remoção de filtros aplicados e retorno da lista original |

| **Pré-condições**                                        |
| :------------------------------------------------------- |
| Usuário está em uma PLP com um ou mais filtros aplicados |

| **Passos**                                                                            |
| :------------------------------------------------------------------------------------ |
| **DADO** que filtros estão aplicados na PLP                                           |
| **QUANDO** o usuário clica em "Limpar filtros" ou desmarca filtros                    |
| **ENTÃO** todos os filtros são removidos                                              |
| **E** a lista de produtos retorna ao estado original (todos os produtos da categoria) |

| **Critérios de aceitação**                            |
| :---------------------------------------------------- |
| Filtros removidos; lista de produtos completa exibida |

---

## Cenário 03.5: Ordenar produtos por Preço (Crescente/Decrescente)

### Caso de Teste 05: Ordenar produtos por preço na PLP

| ID                    | Descrição                                                           |
| :-------------------- | :------------------------------------------------------------------ |
| PLP\_SORT\_PRICE\_001 | Ordenação dos produtos por preço do menor para o maior e vice-versa |

| **Pré-condições**                                           |
| :---------------------------------------------------------- |
| Usuário está em uma PLP com opções de ordenação disponíveis |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que o usuário está em uma PLP                              |
| **QUANDO** ele seleciona a opção "Preço: do menor para o maior"     |
| **ENTÃO** os produtos são ordenados do mais barato para o mais caro |
| **QUANDO** ele seleciona a opção "Preço: do maior para o menor"     |
| **ENTÃO** os produtos são ordenados do mais caro para o mais barato |

| **Critérios de aceitação**                                   |
| :----------------------------------------------------------- |
| Produtos exibidos na ordem correta de preço conforme seleção |

---

## Cenário 03.6: Paginação de produtos

### Caso de Teste 06: Navegação entre páginas da PLP

| ID                   | Descrição                                            |
| :------------------- | :--------------------------------------------------- |
| PLP\_PAGINATION\_001 | Paginação e navegação entre múltiplas páginas da PLP |

| **Pré-condições**                                      |
| :----------------------------------------------------- |
| Categoria contém mais produtos que o limite por página |

| **Passos**                                             |
| :----------------------------------------------------- |
| **DADO** que o usuário está na primeira página da PLP  |
| **QUANDO** ele clica em "Próxima página" ou número "2" |
| **ENTÃO** a segunda página de produtos é exibida       |
| **QUANDO** ele clica em "Página anterior" ou "1"       |
| **ENTÃO** retorna para a primeira página               |

| **Critérios de aceitação**                                              |
| :---------------------------------------------------------------------- |
| Navegação correta entre páginas e produtos carregados conforme a página |

---

## Cenário 03.7: "Adicionar ao Carrinho" rápido da PLP (se disponível)

### Caso de Teste 07: Adicionar produto simples ao carrinho direto na PLP

| ID                 | Descrição                                                |
| :----------------- | :------------------------------------------------------- |
| PLP\_QUICKADD\_001 | Adicionar produto simples diretamente ao carrinho da PLP |

| **Pré-condições**                                                            |
| :--------------------------------------------------------------------------- |
| Produto simples em estoque está disponível com botão "Adicionar ao Carrinho" |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que o usuário está em uma PLP                                   |
| **QUANDO** ele clica no botão "Adicionar ao Carrinho" do produto simples |
| **ENTÃO** o produto é adicionado ao carrinho                             |
| **E** uma notificação de sucesso é exibida                               |
| **E** o contador do mini-carrinho é atualizado                           |

| **Critérios de aceitação**                                                |
| :------------------------------------------------------------------------ |
| Produto adicionado corretamente; notificação exibida; contador atualizado |
