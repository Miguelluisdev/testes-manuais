# 💳 Relatório de Testes - Requisito Funcional RF06: Processo de Checkout

📌 **Prioridade:** ALTÍSSIMA  
📅 **Data de Execução:** 11 de Junho de 2025  
🔍 **Funcionalidade Testada:** Processo de Checkout  
🌐 **Sistema:** PrestaShop Demo  
🔧 **Método de Teste:** Manual  

---

## 📚 Cenários e Resultados

### 🧾 Cenário 6.1: Checkout como convidado - Endereço
- **CT01 - Checkout como convidado - Preenchimento de endereço**  
  🚫 Resultado: **Não testado** – Funcionalidade **não disponível** no ambiente.

- **CT02 - Checkout como convidado - Validação de campos obrigatórios no endereço**  
  🚫 Resultado: **Não testado** – Funcionalidade **não disponível** no ambiente.

---

### 👤 Cenário 6.2: Checkout como usuário logado
- **CT03 - Selecionar endereço salvo**  
  ✅ Resultado: **Passou (com ressalvas)**  
  ✅ Endereço é carregado automaticamente se já estiver salvo.  
  ✅ Também é possível adicionar novo endereço diretamente no checkout.  
  ⚠️ *Erro encontrado:*  
  - Ao tentar **adicionar um novo endereço com um já selecionado**, ocorre erro no sistema ao tentar deletar o endereço:
    > *500 Server Error: Oops, something went wrong*  
  🎥 Evidência: [Jam Link](https://jam.dev/c/345c8764-70d5-4266-b701-8e3083be8f83)

---

### 🚚 Cenário 6.3: Seleção de Método de Envio
- **CT04 - Selecionar método de envio**  
  ✅ Resultado: **Passou**

---

### 💳 Cenário 6.4: Seleção de Pagamento e Finalização
- **CT05 - Selecionar método de pagamento e finalizar pedido**  
  ❌ Resultado: **Falhou**  
  ⚠️ *Erro crítico no momento da finalização da compra*  
  🎥 Evidência: [Jam Link](https://jam.dev/c/d58163e8-62db-4999-9b00-293930fe2af1)

---

### 🔍 Cenário 6.5: Revisão Final do Pedido
- **CT06 - Revisão final antes da finalização do pedido**  
  🚫 Resultado: **Não testado**  
  ❌ *Impossibilitado de testar devido à falha no passo anterior de pagamento.*

---

## 📌 Conclusão

O processo de checkout **apresenta falhas importantes** e **impede a conclusão do fluxo de compra**. Os principais pontos de atenção:

- ✅ Endereço salvo funciona corretamente, mas novo endereço **quebra o fluxo ao tentar excluir**.
- ❌ Erro crítico ao tentar **finalizar o pedido com pagamento**, interrompendo o teste de revisão final.
- 🚫 Checkout como convidado **não disponível** no ambiente de testes atual.

---

## 🧾 Sumário de Testes

| Caso de Teste | Descrição                                                         | Resultado         |
|---------------|-------------------------------------------------------------------|-------------------|
| CT01          | Checkout como convidado - Preenchimento de endereço              | 🚫 Não testado     |
| CT02          | Checkout como convidado - Validação de campos obrigatórios       | 🚫 Não testado     |
| CT03          | Selecionar endereço salvo como usuário logado                    | ✅ Passou (com erro) |
| CT04          | Selecionar método de envio                                        | ✅ Passou          |
| CT05          | Selecionar método de pagamento e finalizar pedido                | ❌ Falhou          |
| CT06          | Revisão do pedido antes da finalização                           | 🚫 Não testado     |

---

👤 **Autor dos Testes:** Miguel Luis  
🧪 **Tipo de Teste:** Manual  
📂 **Arquivo Original dos Testes:** `CT_RF06: Processo de Checkout (Prioridade: ALTÍSSIMA).md`
