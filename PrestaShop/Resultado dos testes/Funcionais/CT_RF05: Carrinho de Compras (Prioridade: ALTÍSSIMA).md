# 🛒 Relatório de Testes - Requisito Funcional RF05: Carrinho de Compras

📌 **Prioridade:** ALTÍSSIMA  
📅 **Data de Execução:** 11 de Junho de 2025  
🔍 **Funcionalidade Testada:** Carrinho de Compras  
🌐 **Sistema:** PrestaShop Demo  
🔧 **Método de Teste:** Manual  

---

## 📚 Cenários e Resultados

### 🛍️ Cenário 5.1: Visualizar carrinho com itens adicionados
- **CT01 - Listagem correta dos produtos no carrinho**  
  ✅ Resultado: **Passou**

---

### 🔄 Cenário 5.2: Atualizar quantidade de um item no carrinho
- **CT02 - Alterar quantidade e recalcular valores corretamente**  
  ✅ Resultado: **Passou (com ressalvas)**  
  ⚠️ *Observações:*  
  - Atualização de preços possui **atraso considerável**.  
  - **Não há limite** de quantidade com base no estoque.  
  - **Bug:** Alterar rapidamente a quantidade pode fazer com que ela volte a um valor anterior.  
  🎥 Vídeo de evidência: [Jam Link](https://jam.dev/c/7237e2ee-975b-44b9-9bd7-120ed07dac2f)

---

### 🗑️ Cenário 5.3: Remover item do carrinho
- **CT03 - Remover produto e atualizar valores do carrinho**  
  ⚠️ Resultado: **Passou com falhas**  
  ⚠️ *Problemas encontrados:*  
  - Delay na remoção e atualização de valores.  
  - Ao tentar reduzir quantidade para menos de 1, aparece o erro:  
    > *"The minimum purchase order quantity for the product The best is yet to come' Framed poster is 1."*  
  - Quantidade **chega a ficar negativa brevemente** antes da correção automática.

---

### 💸 Cenário 5.4: Aplicar cupom de desconto válido
- **CT04 - Aplicar cupom e calcular desconto corretamente**  
  🚫 Resultado: **Não testado** – Funcionalidade **não implementada** no sistema atual.

---

### ❌ Cenário 5.5: Tentativa de aplicar cupom inválido ou expirado
- **CT05 - Exibir erro para cupom inválido e não aplicar desconto**  
  🚫 Resultado: **Não testado** – Funcionalidade **não implementada**.

---

### 🧺 Cenário 5.6: Visualizar carrinho vazio
- **CT06 - Exibir mensagem de carrinho vazio e opção de continuar comprando**  
  ✅ Resultado: **Passou**

---

### 🔙 Cenário 5.7: Clicar em "Continuar Comprando"
- **CT07 - Redirecionar para homepage ou categoria após clicar em continuar comprando**  
  ✅ Resultado: **Passou**

---

### 🧾 Cenário 5.8: Clicar em "Proceder para o Checkout"
- **CT08 - Redirecionar para a primeira etapa do checkout**  
  ✅ Resultado: **Passou**

---

## 📌 Conclusão

O carrinho de compras atende à maioria dos requisitos básicos, porém há **problemas importantes de UX e bugs técnicos**:

- **Atualização lenta** de valores ao alterar ou remover itens.
- **Falta de validação de estoque** na quantidade máxima de produtos.
- **Falhas de sincronização** ao modificar rapidamente a quantidade de itens.
- **Cupom de desconto não implementado**, limitando a cobertura de testes.

🔧 É altamente recomendado priorizar a correção dos bugs citados e a implementação do sistema de cupons para uma experiência de compra completa.

---

## 🧾 Sumário de Testes

| Caso de Teste | Descrição                                                             | Resultado         |
|---------------|-----------------------------------------------------------------------|-------------------|
| CT01          | Listagem correta dos produtos no carrinho                             | ✅ Passou          |
| CT02          | Alterar quantidade e recalcular valores corretamente                  | ⚠️ Passou com falhas |
| CT03          | Remover produto e atualizar valores do carrinho                       | ⚠️ Passou com falhas |
| CT04          | Aplicar cupom de desconto válido                                      | 🚫 Não testado     |
| CT05          | Exibir erro para cupom inválido ou expirado                           | 🚫 Não testado     |
| CT06          | Exibir mensagem de carrinho vazio                                     | ✅ Passou          |
| CT07          | Redirecionar ao clicar em "Continuar Comprando"                      | ✅ Passou          |
| CT08          | Redirecionar ao clicar em "Proceder para o Checkout"                 | ✅ Passou          |

---

👤 **Autor dos Testes:** Miguel Luis
🧪 **Tipo de Teste:** Manual  
📂 **Arquivo Original dos Testes:** `CT_RF05: Carrinho de Compras (Prioridade: ALTÍSSIMA).md`
