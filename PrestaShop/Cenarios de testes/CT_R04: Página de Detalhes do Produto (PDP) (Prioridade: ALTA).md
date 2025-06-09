# 🧪 Plano de Testes Manuais - Presta Shop 
> Funcionalidade: Página de Detalhes do Produto (PDP) (Prioridade: ALTA) 
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---


---

## Cenário 04.1: Visualizar informações de um produto simples

### Caso de Teste 01: Exibir dados completos do produto simples na PDP

| ID                     | Descrição                                                                            |
| :--------------------- | :----------------------------------------------------------------------------------- |
| PDP\_VIEW\_SIMPLE\_001 | Visualizar informações (nome, descrição, preço, imagens, estoque) do produto simples |

| **Pré-condições**                                                |
| :--------------------------------------------------------------- |
| Usuário navegou para a PDP de um produto simples (sem variações) |

| **Passos**                                                                                        |
| :------------------------------------------------------------------------------------------------ |
| **DADO** que o usuário está na PDP do produto simples                                             |
| **ENTÃO** devem ser exibidos corretamente: nome, descrição, preço, imagens e indicador de estoque |

| **Critérios de aceitação**                                        |
| :---------------------------------------------------------------- |
| Todas as informações do produto simples estão visíveis e corretas |

---

## Cenário 04.2: Selecionar variação de produto e verificar atualização

### Caso de Teste 02: Seleção de variações e atualização da PDP

| ID                    | Descrição                                                                            |
| :-------------------- | :----------------------------------------------------------------------------------- |
| PDP\_VAR\_SELECT\_001 | Selecionar variações (ex: cor, tamanho) e validar atualização das informações na PDP |

| **Pré-condições**                                                                          |
| :----------------------------------------------------------------------------------------- |
| Usuário navegou para a PDP de um produto com variações (ex: "Hummingbird Printed T-Shirt") |

| **Passos**                                                                                  |
| :------------------------------------------------------------------------------------------ |
| **DADO** que o usuário está na PDP do produto com variações                                 |
| **QUANDO** seleciona uma variação de Cor (ex: "Preto")                                      |
| **ENTÃO** a imagem principal do produto deve ser atualizada para refletir a cor selecionada |
| **E** o preço e disponibilidade de estoque podem ser atualizados conforme a variação        |
| **(Repetir para outras variações como Tamanho)**                                            |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| Imagem, preço e estoque refletem a variação selecionada |

---

## Cenário 04.3: Adicionar produto simples ao carrinho

### Caso de Teste 03: Adicionar quantidade específica do produto simples ao carrinho

| ID                    | Descrição                                                     |
| :-------------------- | :------------------------------------------------------------ |
| PDP\_ADD\_SIMPLE\_001 | Adicionar produto simples com quantidade definida ao carrinho |

| **Pré-condições**                                    |
| :--------------------------------------------------- |
| Usuário está na PDP de um produto simples em estoque |

| **Passos**                                                     |
| :------------------------------------------------------------- |
| **DADO** que o usuário está na PDP do produto simples          |
| **QUANDO** define quantidade desejada (ex: 2)                  |
| **E** clica no botão "Adicionar ao Carrinho"                   |
| **ENTÃO** 2 itens do produto devem ser adicionados ao carrinho |
| **E** mensagem de confirmação/pop-up é exibida                 |
| **E** ícone/contador do carrinho no cabeçalho é atualizado     |

| **Critérios de aceitação**                                                |
| :------------------------------------------------------------------------ |
| Produto adicionado em quantidade correta; mensagem e contador atualizados |

---

## Cenário 04.4: Adicionar produto com variações ao carrinho

### Caso de Teste 04: Adicionar produto com variações e quantidade ao carrinho

| ID                       | Descrição                                                |
| :----------------------- | :------------------------------------------------------- |
| PDP\_ADD\_VARIATION\_001 | Adicionar produto com variações selecionadas ao carrinho |

| **Pré-condições**                                          |
| :--------------------------------------------------------- |
| Usuário está na PDP de um produto com variações em estoque |

| **Passos**                                                                            |
| :------------------------------------------------------------------------------------ |
| **DADO** que o usuário está na PDP do produto com variações                           |
| **QUANDO** seleciona variações desejadas (ex: Cor "Branco", Tamanho "M")              |
| **E** define quantidade (ex: 1)                                                       |
| **E** clica em "Adicionar ao Carrinho"                                                |
| **ENTÃO** produto com as variações e quantidade selecionadas é adicionado ao carrinho |
| **E** mensagem de confirmação/pop-up é exibida                                        |
| **E** ícone/contador do carrinho é atualizado                                         |

| **Critérios de aceitação**                                                    |
| :---------------------------------------------------------------------------- |
| Produto com variações e quantidade corretas adicionados e confirmação exibida |

---

## Cenário 04.5: Tentativa de adicionar produto ao carrinho sem variação obrigatória

### Caso de Teste 05: Adicionar produto com variações sem selecionar variações obrigatórias

| ID                         | Descrição                                                                            |
| :------------------------- | :----------------------------------------------------------------------------------- |
| PDP\_ADD\_NOVARIATION\_001 | Validar erro ao tentar adicionar produto com variações obrigatórias não selecionadas |

| **Pré-condições**                                         |
| :-------------------------------------------------------- |
| Usuário está na PDP de produto com variações obrigatórias |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que o usuário está na PDP do produto com variações obrigatórias |
| **QUANDO** clica em "Adicionar ao Carrinho" sem selecionar as variações  |
| **ENTÃO** mensagem de erro é exibida solicitando a seleção das variações |
| **E** produto não é adicionado ao carrinho                               |

| **Critérios de aceitação**                                    |
| :------------------------------------------------------------ |
| Mensagem de erro exibida e produto não adicionado ao carrinho |

---

## Cenário 04.6: Tentar adicionar produto fora de estoque ao carrinho

### Caso de Teste 06: Bloquear ou avisar ao tentar adicionar produto fora de estoque

| ID                        | Descrição                                                                    |
| :------------------------ | :--------------------------------------------------------------------------- |
| PDP\_ADD\_OUTOFSTOCK\_001 | Verificar comportamento do botão ao tentar adicionar produto fora de estoque |

| **Pré-condições**                                 |
| :------------------------------------------------ |
| Usuário está na PDP de um produto fora de estoque |

| **Passos**                                                                                                                    |
| :---------------------------------------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na PDP do produto fora de estoque                                                                 |
| **ENTÃO** botão "Adicionar ao Carrinho" deve estar desabilitado ou, se clicado, mostrar mensagem informando indisponibilidade |

| **Critérios de aceitação**                         |
| :------------------------------------------------- |
| Botão desabilitado ou mensagem informativa exibida |

---

## Cenário 04.7: Alterar quantidade na PDP e adicionar ao carrinho

### Caso de Teste 07: Alterar quantidade e adicionar ao carrinho

| ID                    | Descrição                                         |
| :-------------------- | :------------------------------------------------ |
| PDP\_QTY\_CHANGE\_001 | Alterar quantidade na PDP e adicionar ao carrinho |

| **Pré-condições**                            |
| :------------------------------------------- |
| Usuário está na PDP de um produto em estoque |

| **Passos**                                                  |
| :---------------------------------------------------------- |
| **DADO** que o usuário está na PDP                          |
| **QUANDO** altera quantidade para "3"                       |
| **E** clica em "Adicionar ao Carrinho"                      |
| **ENTÃO** 3 unidades do produto são adicionadas ao carrinho |

| **Critérios de aceitação**                          |
| :-------------------------------------------------- |
| Quantidade correta adicionada e confirmação exibida |

---

## Cenário 04.8: Verificar informações nas abas adicionais (Data sheet, Reviews)

### Caso de Teste 08: Exibir informações técnicas e avaliações

| ID                   | Descrição                                                       |
| :------------------- | :-------------------------------------------------------------- |
| PDP\_TABS\_INFO\_001 | Visualizar informações das abas "Data sheet" e "Reviews" na PDP |

| **Pré-condições**              |
| :----------------------------- |
| Usuário está na PDP do produto |

| **Passos**                                                                                                   |
| :----------------------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na PDP                                                                           |
| **QUANDO** clica na aba "Data sheet"                                                                         |
| **ENTÃO** as informações técnicas do produto são exibidas                                                    |
| **QUANDO** clica na aba "Reviews"                                                                            |
| **ENTÃO** avaliações existentes são exibidas e formulário para nova avaliação está disponível (se permitido) |

| **Critérios de aceitação**                              |
| :------------------------------------------------------ |
| Informações técnicas e avaliações exibidas corretamente |

---

Quer que eu gere esse conteúdo num arquivo `.md` para você?
