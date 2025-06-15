# 🛒 Relatório de Testes - Requisito Funcional RF03: Listagem de Produtos (PLP)

📌 **Prioridade:** ALTA  
📅 **Data de Execução:** 11 de Junho de 2025  
🔍 **Funcionalidade Testada:** Página de Listagem de Produtos (PLP)  
🌐 **Sistema:** PrestaShop Demo  
🔧 **Método de Teste:** Manual  

---

## 📚 Cenários e Resultados

### 📂 Cenário 03.1: Navegar para uma página de categoria
- **CT01 - Navegar para página de categoria via menu principal**  
  ✅ Resultado: **Passou**

---

### 🎨 Cenário 03.2: Aplicar filtro de atributo (ex: Cor)
- **CT02 - Aplicar filtro de atributo em PLP**  
  ⚠️ Resultado: **Passou com erro visual**  
  🐞 *Bug:* Ao aplicar o filtro de cor (ex: selecionar "White"), o produto exibido aparece com cor **preta**, causando confusão ao usuário.  
  🎥 **Evidência:** [Vídeo Jam.dev](https://jam.dev/c/1ea3016f-b83c-4fe1-bd77-ed027868e010)

---

### 🔗 Cenário 03.3: Aplicar múltiplos filtros combinados (ex: Cor e Tamanho)
- **CT03 - Aplicar filtros combinados em PLP**  
  ✅ Resultado: **Passou com sugestão de melhoria**  
  💡 *Melhoria Sugerida:*  
  A cada clique em um novo filtro, a página recarrega, o que impacta a **experiência do usuário**. Idealmente, a atualização dos resultados deveria ser dinâmica.  
  🎥 **Evidência:** [Vídeo Jam.dev](https://jam.dev/c/7a5e6621-28cf-4117-b79e-0e24f6079502)

---

### 🔄 Cenário 03.4: Limpar/Resetar filtros aplicados
- **CT04 - Limpar filtros na PLP**  
  ✅ Resultado: **Passou**

---

### 💰 Cenário 03.5: Ordenar produtos por Preço (Crescente/Decrescente)
- **CT05 - Ordenar produtos por preço na PLP**  
  ✅ Resultado: **Passou**

---

### 📄 Cenário 03.6: Paginação de produtos
- **CT06 - Navegação entre páginas da PLP**  
  ⚠️ Resultado: **Não Testado / Funcionalidade Inexistente**  
  📌 A PLP atual não apresenta suporte à paginação, exibindo todos os produtos em uma única página.

---

### 🛍️ Cenário 03.7: "Adicionar ao Carrinho" rápido da PLP
- **CT07 - Adicionar produto simples ao carrinho direto na PLP**  
  ✅ Resultado: **Passou**

---

## 🐞 Bugs e Melhorias Identificadas

| ID   | Descrição                                                                 | Tipo       | Severidade | Prioridade | Evidência |
|------|---------------------------------------------------------------------------|------------|------------|------------|-----------|
| B07  | Cor do produto exibida não corresponde à cor selecionada no filtro        | Bug        | Média      | Alta       | [Jam.dev](https://jam.dev/c/1ea3016f-b83c-4fe1-bd77-ed027868e010) |
| M01  | Página é recarregada a cada novo filtro selecionado                      | Melhoria   | Baixa      | Média      | [Jam.dev](https://jam.dev/c/7a5e6621-28cf-4117-b79e-0e24f6079502) |
| M02  | Falta de paginação na PLP pode comprometer usabilidade com muitos itens  | Melhoria   | Média      | Média      | N/A       |

---

## 📌 Conclusão

A listagem de produtos atende aos requisitos principais, mas apresenta **problemas de consistência visual** com os filtros e **pontos de melhoria na usabilidade** da página. Os testes confirmam que a funcionalidade está operante, mas recomenda-se correções para garantir uma melhor experiência ao usuário.

---

👤 **Autor dos Testes:** Miguel Luis  
🧪 **Tipo de Teste:** Manual  
📂 **Arquivo Original dos Testes:** `CT_RF03: Listagem de Produtos (PLP) (Prioridade: ALTA).md`  
