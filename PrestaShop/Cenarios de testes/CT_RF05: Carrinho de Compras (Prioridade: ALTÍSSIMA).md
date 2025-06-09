# 🧪 Plano de Testes Manuais - Presta Shop 
> Funcionalidade: Busca de Produto (Prioridade: ALTA)  
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---

## Cenário 5.1: Visualizar carrinho com itens adicionados

### Caso de Teste 01: Listagem correta dos produtos no carrinho

| ID                     | Descrição                                                             |
| :--------------------- | :-------------------------------------------------------------------- |
| CART\_VIEW\_ITEMS\_001 | O usuário visualiza os produtos adicionados ao carrinho corretamente. |

| **Pré-condições**                            |
| :------------------------------------------- |
| Um ou mais produtos adicionados ao carrinho. |

| **Passos**                                                                                                                                        |
| :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **DADO** que o usuário adicionou produtos ao carrinho                                                                                             |
| **QUANDO** ele navega para a página do carrinho (clicando no ícone do carrinho e "Ver Carrinho")                                                  |
| **ENTÃO** todos os produtos adicionados devem ser listados com nome, imagem, variação (se houver), quantidade, preço unitário e subtotal por item |
| **E** o resumo do pedido (subtotal, frete, total) deve ser exibido corretamente                                                                   |

| **Critérios de aceitação**                                                                            |
| :---------------------------------------------------------------------------------------------------- |
| O sistema exibe corretamente os detalhes de todos os produtos adicionados e o resumo total do pedido. |

---

## Cenário 5.2: Atualizar quantidade de um item no carrinho

### Caso de Teste 01: Alterar quantidade e recalcular valores corretamente

| ID                     | Descrição                                                                             |
| :--------------------- | :------------------------------------------------------------------------------------ |
| CART\_QTY\_UPDATE\_001 | O usuário altera a quantidade de um produto no carrinho e os valores são atualizados. |

| **Pré-condições**                                      |
| :----------------------------------------------------- |
| Produto presente no carrinho com quantidade inicial 1. |

| **Passos**                                                                              |
| :-------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho com um item (Qtd: 1)                  |
| **QUANDO** ele aumenta a quantidade desse item para "3" (usando campo +/- ou digitando) |
| **ENTÃO** o subtotal do item deve ser recalculado (Preço Unitário \* 3)                 |
| **E** o total geral do carrinho deve ser recalculado e atualizado.                      |

| **Critérios de aceitação**                                                                               |
| :------------------------------------------------------------------------------------------------------- |
| O sistema atualiza subtotal do item e total geral do carrinho corretamente após alteração da quantidade. |

---

## Cenário 5.3: Remover item do carrinho

### Caso de Teste 01: Remover produto e atualizar valores do carrinho

| ID                      | Descrição                                                       |
| :---------------------- | :-------------------------------------------------------------- |
| CART\_ITEM\_REMOVE\_001 | O usuário remove um produto do carrinho e o total é atualizado. |

| **Pré-condições**                   |
| :---------------------------------- |
| Produto(s) presente(s) no carrinho. |

| **Passos**                                                              |
| :---------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho com um ou mais itens  |
| **QUANDO** ele clica no ícone "Remover" (lixeira) de um item específico |
| **ENTÃO** o item deve ser removido da lista do carrinho                 |
| **E** o total geral do carrinho deve ser recalculado e atualizado       |

| **Critérios de aceitação**                                                 |
| :------------------------------------------------------------------------- |
| O sistema remove o item e atualiza o total geral do carrinho corretamente. |

---

## Cenário 5.4: Aplicar cupom de desconto válido

### Caso de Teste 01: Aplicar cupom e calcular desconto corretamente

| ID                       | Descrição                                                           |
| :----------------------- | :------------------------------------------------------------------ |
| CART\_COUPON\_VALID\_001 | O usuário aplica um cupom válido e o desconto é refletido no total. |

| **Pré-condições**                                                              |
| :----------------------------------------------------------------------------- |
| Cupom de desconto válido e ativo; produto(s) no carrinho que atendem ao cupom. |

| **Passos**                                                             |
| :--------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho com itens            |
| **QUANDO** ele insere um código de cupom válido no campo apropriado    |
| **E** clica em "Aplicar"                                               |
| **ENTÃO** o desconto do cupom deve ser aplicado ao total do pedido     |
| **E** o valor do desconto e o novo total devem ser exibidos claramente |

| **Critérios de aceitação**                                                          |
| :---------------------------------------------------------------------------------- |
| O sistema aplica o desconto corretamente e exibe o valor atualizado para o usuário. |

---

## Cenário 5.5: Tentativa de aplicar cupom inválido ou expirado

### Caso de Teste 01: Exibir erro para cupom inválido e não aplicar desconto

| ID                         | Descrição                                                         |
| :------------------------- | :---------------------------------------------------------------- |
| CART\_COUPON\_INVALID\_001 | O usuário insere um cupom inválido e recebe uma mensagem de erro. |

| **Pré-condições**       |
| :---------------------- |
| Produto(s) no carrinho. |

| **Passos**                                                                       |
| :------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho com itens                      |
| **QUANDO** ele insere um código de cupom inválido ou expirado                    |
| **E** clica em "Aplicar"                                                         |
| **ENTÃO** uma mensagem de erro deve ser exibida indicando que o cupom é inválido |
| **E** nenhum desconto deve ser aplicado                                          |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| O sistema exibe mensagem de erro e não altera o total do pedido. |

---

## Cenário 5.6: Visualizar carrinho vazio

### Caso de Teste 01: Exibir mensagem de carrinho vazio e opção de continuar comprando

| ID                     | Descrição                                                          |
| :--------------------- | :----------------------------------------------------------------- |
| CART\_EMPTY\_VIEW\_001 | O usuário visualiza mensagem adequada ao acessar o carrinho vazio. |

| **Pré-condições**        |
| :----------------------- |
| Nenhum item no carrinho. |

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que o carrinho do usuário está vazio                               |
| **QUANDO** ele navega para a página do carrinho                             |
| **ENTÃO** uma mensagem indicando "Seu carrinho está vazio" deve ser exibida |
| **E** um link/botão para "Continuar comprando" deve estar presente          |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| O sistema exibe mensagem clara de carrinho vazio e opção para continuar. |

---

## Cenário 5.7: Clicar em "Continuar Comprando"

### Caso de Teste 01: Redirecionar para homepage ou categoria após clicar em continuar comprando

| ID                            | Descrição                                                                 |
| :---------------------------- | :------------------------------------------------------------------------ |
| CART\_CONTINUE\_SHOPPING\_001 | O usuário clica em "Continuar Comprando" e é redirecionado adequadamente. |

| **Pré-condições**                   |
| :---------------------------------- |
| Usuário está na página do carrinho. |

| **Passos**                                                                        |
| :-------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho                                 |
| **QUANDO** ele clica no botão/link "Continuar Comprando"                          |
| **ENTÃO** ele deve ser redirecionado para a homepage ou última categoria visitada |

| **Critérios de aceitação**                                             |
| :--------------------------------------------------------------------- |
| O sistema redireciona corretamente o usuário para continuar navegando. |

---

## Cenário 5.8: Clicar em "Proceder para o Checkout"

### Caso de Teste 01: Redirecionar para a primeira etapa do checkout

| ID                           | Descrição                                                   |
| :--------------------------- | :---------------------------------------------------------- |
| CART\_PROCEED\_CHECKOUT\_001 | O usuário inicia o processo de checkout ao clicar no botão. |

| **Pré-condições**            |
| :--------------------------- |
| Itens presentes no carrinho. |

| **Passos**                                                                         |
| :--------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página do carrinho com itens                        |
| **QUANDO** ele clica no botão "Proceder para o Checkout"                           |
| **ENTÃO** ele deve ser redirecionado para a primeira etapa do processo de checkout |

| **Critérios de aceitação**                                                     |
| :----------------------------------------------------------------------------- |
| O sistema inicia o processo de checkout redirecionando o usuário corretamente. |
