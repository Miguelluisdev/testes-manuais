# 🧪 Plano de Testes Manuais - Presta Shop 
> Funcionalidade: Busca de Produto (Prioridade: ALTA)  
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---

## Cenário 06: Checkout Completo

### Caso de Teste 01: Checkout como convidado - Preenchimento de endereço

| ID                            | Descrição                                                          |
| :---------------------------- | :----------------------------------------------------------------- |
| CHECKOUT\_GUEST\_ADDRESS\_001 | Usuário convidado preenche endereço de entrega válido no checkout. |

| **Pré-condições**                                                           |
| :-------------------------------------------------------------------------- |
| Itens no carrinho, usuário não logado, seleciona "Checkout como convidado". |

| **Passos**                                                                                |
| :---------------------------------------------------------------------------------------- |
| **DADO** que o usuário não logado está na etapa de "Endereços" do checkout                |
| **QUANDO** ele preenche todos os campos obrigatórios do formulário de endereço de entrega |
| (Opcional) Marca "Usar este endereço também para cobrança"                                |
| **E** clica em "Continuar"                                                                |
| **ENTÃO** ele deve avançar para a próxima etapa (Método de Envio).                        |

| **Critérios de aceitação**                                                                         |
| :------------------------------------------------------------------------------------------------- |
| O sistema deve validar os dados corretamente e avançar para a etapa de seleção do método de envio. |

---

### Caso de Teste 02: Checkout como convidado - Validação de campos obrigatórios no endereço

| ID                                      | Descrição                                                           |
| :-------------------------------------- | :------------------------------------------------------------------ |
| CHECKOUT\_GUEST\_ADDRESS\_VALIDATE\_001 | Tentativa de avançar no checkout sem preencher campos obrigatórios. |

| **Pré-condições**                                            |
| :----------------------------------------------------------- |
| Usuário não logado está na etapa de "Endereços" do checkout. |

| **Passos**                                                                                  |
| :------------------------------------------------------------------------------------------ |
| **DADO** que o usuário está na etapa de "Endereços" do checkout                             |
| **QUANDO** ele tenta continuar sem preencher um ou mais campos obrigatórios (ex: Nome, CEP) |
| **ENTÃO** mensagens de erro devem ser exibidas para cada campo obrigatório não preenchido   |
| **E** ele não deve avançar para a próxima etapa                                             |

| **Critérios de aceitação**                                                   |
| :--------------------------------------------------------------------------- |
| O sistema deve bloquear a navegação e mostrar mensagens de erro específicas. |

---

### Caso de Teste 03: Checkout como usuário logado - Selecionar endereço salvo

| ID                                    | Descrição                                            |
| :------------------------------------ | :--------------------------------------------------- |
| CHECKOUT\_LOGGED\_ADDRESS\_SAVED\_001 | Usuário logado seleciona endereço salvo no checkout. |

| **Pré-condições**                                        |
| :------------------------------------------------------- |
| Usuário logado com endereços salvos e itens no carrinho. |

| **Passos**                                                             |
| :--------------------------------------------------------------------- |
| **DADO** que o usuário logado está na etapa de "Endereços" do checkout |
| **QUANDO** ele seleciona um dos seus endereços salvos                  |
| **E** clica em "Continuar"                                             |
| **ENTÃO** ele deve avançar para a próxima etapa (Método de Envio).     |

| **Critérios de aceitação**                                         |
| :----------------------------------------------------------------- |
| O sistema deve permitir a seleção e avançar para a etapa seguinte. |

---

### Caso de Teste 04: Checkout - Seleção de Método de Envio

| ID                              | Descrição                                               |
| :------------------------------ | :------------------------------------------------------ |
| CHECKOUT\_SHIPPING\_SELECT\_001 | Usuário seleciona método de envio e avança no checkout. |

| **Pré-condições**                   |
| :---------------------------------- |
| Endereço preenchido ou selecionado. |

| **Passos**                                                                      |
| :------------------------------------------------------------------------------ |
| **DADO** que o usuário está na etapa de "Método de Envio"                       |
| **QUANDO** ele seleciona uma das opções de envio disponíveis (ex: "My Carrier") |
| (Opcional) Aceita os Termos de Serviço (se obrigatório)                         |
| **E** clica em "Continuar"                                                      |
| **ENTÃO** o custo do frete selecionado deve ser adicionado ao resumo do pedido  |
| **E** ele deve avançar para a próxima etapa (Pagamento).                        |

| **Critérios de aceitação**                                                             |
| :------------------------------------------------------------------------------------- |
| O sistema deve calcular e mostrar o frete corretamente e avançar no fluxo do checkout. |

---

### Caso de Teste 05: Checkout - Seleção de Método de Pagamento e Finalização (Demo)

| ID                                 | Descrição                                                        |
| :--------------------------------- | :--------------------------------------------------------------- |
| CHECKOUT\_PAYMENT\_PLACEORDER\_001 | Usuário seleciona método de pagamento e finaliza pedido no demo. |

| **Pré-condições**               |
| :------------------------------ |
| Método de envio já selecionado. |

| **Passos**                                                                      |
| :------------------------------------------------------------------------------ |
| **DADO** que o usuário está na etapa de "Pagamento"                             |
| **QUANDO** ele seleciona um método de pagamento disponível (ex: "Pay by Check") |
| **E** (se houver) aceita os termos e condições                                  |
| **E** clica no botão "Finalizar Pedido" (ou "Place Order")                      |
| **ENTÃO** o pedido deve ser processado com sucesso (no contexto do demo)        |
| **E** ele deve ser redirecionado para uma página de confirmação de pedido       |
| **E** a página de confirmação deve exibir o número do pedido e um resumo        |
| (Opcional) Um e-mail de confirmação de pedido deve ser (simulado/verificado).   |

| **Critérios de aceitação**                                                       |
| :------------------------------------------------------------------------------- |
| O sistema deve processar o pedido e mostrar a confirmação com os dados corretos. |

---

### Caso de Teste 06: Checkout - Revisão do pedido antes da finalização

| ID                           | Descrição                                            |
| :--------------------------- | :--------------------------------------------------- |
| CHECKOUT\_ORDER\_REVIEW\_001 | Usuário revisa o pedido antes de finalizar a compra. |

| **Pré-condições**                                            |
| :----------------------------------------------------------- |
| Usuário está na última etapa do checkout antes de finalizar. |

| **Passos**                                                                                     |
| :--------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na última etapa do checkout, antes de clicar em "Finalizar Pedido" |
| **ENTÃO** um resumo completo do pedido deve ser visível, incluindo:                            |
| - Itens do pedido (nome, quantidade, preço)                                                    |
| - Endereço de entrega e cobrança                                                               |
| - Método de envio selecionado e custo                                                          |
| - Subtotal, impostos (se houver), frete e total geral                                          |

| **Critérios de aceitação**                                                           |
| :----------------------------------------------------------------------------------- |
| O sistema deve mostrar um resumo detalhado e correto do pedido antes da finalização. |
