# ✅ Relatório Geral dos Testes Funcionais

📅 **Data de Execução:** Junho de 2025  
🧪 **Tipo de Teste:** Manual  
🧠 **Base:** Casos de teste previamente documentados por requisito funcional  
🌐 **Sistema Testado:** PrestaShop

---

## 📊 Visão Geral

| Código RF  | Nome do Requisito                              | Total CTs | Passaram | Não Testado | Erros/Bugs Encontrados | Prioridade   |
|------------|------------------------------------------------|-----------|----------|-------------|------------------------|--------------|
| RF01       | Login e Cadastro                               | 9         | 8        | 0           | 2                      | ALTA         |
| RF02       | Busca de Produto                               | 6         | 5        | 1           | 2                      | ALTA         |
| RF03       | Listagem de Produtos (PLP)                     | 7         | 5        | 1           | 2                      | ALTA         |
| RF04       | Página de Detalhes do Produto (PDP)            | 8         | 7        | 0           | 1                      | ALTA         |
| RF05       | Carrinho de Compras                            | 8         | 6        | 2           | 3                      | ALTÍSSIMA    |
| RF06       | Processo de Checkout                           | 6         | 2        | 2           | 2                      | ALTÍSSIMA    |
| RF07       | Gerenciamento de Conta de Usuário              | 6         | 4        | 2           | 1 (restrição esperada) | MÉDIA        |

---

## 🧩 Resumo por Requisito

### 🔐 **RF01 - Login e Cadastro**
- ✅ 8 casos passaram
- ⚠️ Bug 1: Após logout, usuário é redirecionado para a última página acessada (ex: página de recuperação).
- ⚠️ Bug 2: Erro ao tentar recuperar senha com e-mail válido: *"An error occurred while sending the email."*

### 🔍 **RF02 - Busca de Produto**
- ✅ 5 casos passaram
- ⚠️ Bug 1: Busca com números retorna resultados inesperados.
- ⚠️ Bug 2: Termos parciais curtos como "mu" não funcionam.

### 🛒 **RF03 - Listagem de Produtos (PLP)**
- ✅ 5 casos passaram
- ⚠️ Bug 1: Seleção de filtro de cor exibe produto com cor incorreta.
- ⚠️ Melhoria: Filtros atualizam a página a cada clique (UX prejudicada).

### 📦 **RF04 - Página de Detalhes do Produto (PDP)**
- ✅ 7 casos passaram
- ⚠️ Observação: Produtos precisam ter variações obrigatórias para cobrir mais testes.

### 🧺 **RF05 - Carrinho de Compras**
- ✅ 6 casos passaram
- ⚠️ Bug 1: Demora na atualização de valores ao alterar/remover produtos.
- ⚠️ Bug 2: Sem controle de limite por estoque.
- ⚠️ Bug 3: Quantidade pode ficar negativa.

### 💳 **RF06 - Processo de Checkout**
- ✅ 2 casos passaram
- ❌ Checkout falhou na etapa de pagamento.
- ⚠️ Bug: Erro 500 ao deletar endereço durante checkout.
- ⚠️ Não há opção de checkout como convidado.

### 👤 **RF07 - Gerenciamento de Conta do Usuário**
- ✅ 4 casos passaram
- ⚠️ Não foi possível testar histórico e detalhes de pedido (sem pedido concluído).
- ⚠️ Restrição correta: endereço em uso não pode ser deletado.

---

## 🧾 Conclusão Geral

🔎 Foram executados testes manuais com foco em **funcionalidades críticas do e-commerce**, cobrindo:
- Autenticação e Cadastro
- Busca e navegação de produtos
- Adição ao carrinho e processo de checkout
- Gerenciamento de conta

⚠️ **Principais falhas encontradas:**
- Bugs na recuperação de senha e sessão expirada
- Problemas de UX em filtros e delays no carrinho
- Falha crítica no **pagamento do checkout** (impede o fluxo completo de compra)
- Validação de quantidade e estoque inconsistente

---

📁 **Documentos Individuais por RF:**
- [CT_RF01: Login e Cadastro](./CT_RF01:%20Login%20e%20Cadastro%20(Prioridade:%20ALTA).md)
- [CT_RF02: Busca de Produto](./CT_RF02:%20Busca%20de%20Produto%20(Prioridade:%20ALTA).md)
- [CT_RF03: Listagem de Produtos (PLP)](./CT_RF03:%20Listagem%20de%20Produtos%20(PLP)%20(Prioridade:%20ALTA).md)
- [CT_RF04: Página de Detalhes do Produto (PDP)](./CT_RF04:%20Página%20de%20Detalhes%20do%20Produto%20(PDP)%20(Prioridade:%20ALTA).md)
- [CT_RF05: Carrinho de Compras](./CT_RF05:%20Carrinho%20de%20Compras%20(Prioridade:%20ALTÍSSIMA).md)
- [CT_RF06: Processo de Checkout](./CT_RF06:%20Processo%20de%20Checkout%20(Prioridade:%20ALTÍSSIMA).md)
- [CT_RF07: Gerenciamento de Conta de Usuário](./CT_RF07:%20Gerenciamento%20de%20Conta%20de%20Usuário%20(Prioridade:%20MÉDIA).md)

---

✍️ **Autor:** Miguel Luis
🔍 **Método de Teste:** Manual com foco em QA funcional e experiência do usuário  
📌 **Observação Final:** Documentação de bugs foi feita com vídeos (Jam.dev) e pode ser incluída na seção de evidências do repositório.

