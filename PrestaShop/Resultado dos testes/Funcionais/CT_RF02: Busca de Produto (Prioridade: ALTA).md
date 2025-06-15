# 🔍 Relatório de Testes - Requisito Funcional RF02: Busca de Produto

📌 **Prioridade:** ALTA  
📅 **Data de Execução:** 11 de Junho de 2025  
🔍 **Funcionalidade Testada:** Barra de Pesquisa de Produtos  
🌐 **Sistema:** PrestaShop Demo  
🔧 **Método de Teste:** Manual  

---

## 📚 Cenários e Resultados

### 🔠 Cenário 02.1: Busca por nome exato do produto
- **CT01 - Busca com nome exato do produto**  
  ✅ Resultado: **Passou**  
  ⚠️ *Observação:*  
  Ao digitar **números**, a barra de pesquisa retorna a **coleção de acessórios**, comportamento inesperado.  
  🎥 **Evidência:** [Vídeo Jam.dev](https://jam.dev/c/ea4ffcc2-a71f-40a6-b8a4-44d3c07604b9)

---

### 🔤 Cenário 02.2: Busca por termo parcial do produto
- **CT02 - Busca com termo parcial no nome do produto**  
  ✅ Resultado: **Passou (parcialmente)**  
  ⚠️ *Observação:*  
  Nem todos os termos parciais funcionam. Exemplo: ao digitar apenas **"mu"**, nenhum produto é retornado.

---

### 🔢 Cenário 02.3: Busca por SKU (se aplicável)
- **CT03 - Busca com SKU do produto**  
  ⚠️ Resultado: **Não Aplicável**  
  📌 A funcionalidade de busca por SKU não está presente ou não foi possível testar.

---

### 🚫 Cenário 02.4: Busca por termo inexistente
- **CT04 - Busca com termo sem correspondência**  
  ✅ Resultado: **Passou**  
  📌 O sistema retorna uma mensagem informando que nenhum produto foi encontrado, conforme esperado.

---

### 🧠 Cenário 02.5: Busca com sugestões (Autocomplete)
- **CT05 - Sugestões de busca enquanto digita**  
  ✅ Resultado: **Passou**  
  📌 As sugestões aparecem dinamicamente com base no texto digitado, confirmando que o recurso de autocomplete está funcional.

---

### ❓ Cenário 02.6: Busca vazia
- **CT06 - Busca sem digitar termo**  
  ❌ Resultado: **Falhou**  
  📌 Com o campo de busca vazio, o sistema exibe uma mensagem de erro indicando que não há nenhum produto — comportamento coerente, porém **não alinhado ao esperado**, que seria exibir **todos os produtos disponíveis** por padrão.

---

## 🐞 Bugs e Comportamentos Inesperados

| ID   | Descrição                                                                                          | Severidade | Prioridade | Evidência |
|------|----------------------------------------------------------------------------------------------------|------------|------------|-----------|
| B04  | Busca com apenas números retorna produtos de acessórios                                            | Média      | Média      | [Jam.dev](https://jam.dev/c/ea4ffcc2-a71f-40a6-b8a4-44d3c07604b9) |
| B05  | Termos parciais curtos (ex: "mu") não retornam nenhum resultado                                    | Baixa      | Média      | N/A       |
| B06  | Busca vazia retorna erro ao invés de exibir todos os produtos, prejudicando usabilidade            | Média      | Alta       | N/A       |

---

## 📌 Conclusão

A funcionalidade de busca atende parcialmente os critérios esperados. Os testes demonstraram que os **cenários principais funcionam**, mas há **comportamentos inconsistentes e não intuitivos**, especialmente com **buscas vazias**, **inputs numéricos** e **termos curtos**. A usabilidade pode ser melhorada com ajustes na lógica de retorno da pesquisa.

---

👤 **Autor dos Testes:** Miguel Luis  
🧪 **Tipo de Teste:** Manual  
📂 **Arquivo Original dos Testes:** `CT_RF02: Busca de Produto (Prioridade: ALTA).md`  
