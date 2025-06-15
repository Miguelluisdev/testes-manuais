# 👤 Relatório de Testes - Requisito Funcional RF07: Gerenciamento de Conta de Usuário

📌 **Prioridade:** MÉDIA  
📅 **Data de Execução:** 11 de Junho de 2025  
🔍 **Funcionalidade Testada:** Gestão da Conta do Usuário  
🌐 **Sistema:** PrestaShop Demo  
🔧 **Método de Teste:** Manual  

---

## 📚 Cenários e Resultados

### 🧾 Cenário 7.1: Visualização de Histórico de Pedidos
- **CT01 - Visualizar histórico de pedidos**  
  🚫 Resultado: **Não testado**  
  ❌ Impossível validar funcionalidade, pois **não foi possível concluir uma compra** no sistema.

- **CT02 - Visualizar detalhes de um pedido específico**  
  🚫 Resultado: **Não testado**  
  ⚠️ **Bloqueado** por dependência do caso de teste anterior.

---

### 📦 Cenário 7.2: Gerenciamento de Endereços
- **CT03 - Adicionar um novo endereço**  
  ✅ Resultado: **Passou**

- **CT04 - Editar um endereço existente**  
  ✅ Resultado: **Passou**

- **CT05 - Excluir um endereço existente**  
  ⚠️ Resultado: **Passou com comportamento esperado (restrição)**  
  🔒 Não é possível deletar o endereço se ele estiver **vinculado ao carrinho de compras**.  
  Mensagem exibida corretamente:
  > *"Could not delete the address since it is used in the shopping cart."*

---

### ✏️ Cenário 7.3: Atualização de Informações Pessoais
- **CT06 - Editar informações pessoais**  
  ✅ Resultado: **Passou**

---

## 📌 Conclusão

O gerenciamento de conta funciona **parcialmente**, com funcionalidades de endereço e edição pessoal operando corretamente. Contudo:

- 🚫 **Histórico de pedidos e detalhes** não puderam ser testados devido à falha no processo de compra (RF06).
- ✅ Restrição de exclusão de endereço em uso foi corretamente aplicada.

---

## 🧾 Sumário de Testes

| Caso de Teste | Descrição                                             | Resultado                   |
|---------------|---------------------------------------------------------|-----------------------------|
| CT01          | Visualizar histórico de pedidos                         | 🚫 Não testado              |
| CT02          | Visualizar detalhes de um pedido específico             | 🚫 Não testado              |
| CT03          | Adicionar um novo endereço                              | ✅ Passou                   |
| CT04          | Editar um endereço existente                            | ✅ Passou                   |
| CT05          | Excluir um endereço existente                           | ⚠️ Passou com restrição     |
| CT06          | Editar informações pessoais                             | ✅ Passou                   |

---

👤 **Autor dos Testes:** Miguel Luis
🧪 **Tipo de Teste:** Manual  
📂 **Arquivo Original dos Testes:** `CT_RF07: Gerenciamento de Conta de Usuário (Prioridade: MÉDIA).md`
