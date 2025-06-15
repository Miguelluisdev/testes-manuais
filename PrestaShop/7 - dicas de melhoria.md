# ✅ Sugestões e Dicas de Melhoria dos Bugs Encontrados

📁 Este documento apresenta recomendações para correção, prevenção e aprimoramento de funcionalidades com base nos bugs detectados durante os testes manuais.

---

## 🔍 RF02 - Busca de Produto

### 🐞 Bug: Termos numéricos retornam coleções irrelevantes
- **Melhoria Sugerida:** Implementar uma distinção entre busca por número de SKU e texto. Usar filtros no back-end para não retornar categorias aleatórias quando o termo for apenas numérico.
- **Dica:** Adicione validação no input para diferenciar tipos de busca com base em regex ou tipo de dado.

### 🐞 Bug: Termos curtos como "mu" não retornam resultados
- **Melhoria Sugerida:** Reduzir o limite mínimo de caracteres no mecanismo de busca para 2 letras ou implementar uma busca mais tolerante com fuzzy match.
- **Dica:** Use algoritmos como Levenshtein Distance ou implementações de auto complete com sugestões parciais.

---

## 🎨 RF03 - Listagem de Produtos (PLP)

### 🐞 Bug: Filtro por cor exibe cores erradas
- **Melhoria Sugerida:** Corrigir a associação de atributos no banco de dados. Verificar se os produtos estão corretamente vinculados à cor selecionada.
- **Dica:** Criar testes automatizados para validar a consistência entre atributo → produto exibido.

### 🐞 Melhoria: Reload da página a cada filtro aplicado
- **Melhoria Sugerida:** Aplicar filtros via AJAX para evitar recarregamento da página e melhorar a fluidez da navegação.
- **Dica:** Utilizar frameworks como Vue.js, React ou jQuery para renderizar filtros dinamicamente.

---

## 🛒 RF05 - Carrinho de Compras

### 🐞 Bug: Quantidade no carrinho pode ultrapassar o estoque
- **Melhoria Sugerida:** Validar o estoque no frontend (JavaScript) e backend antes de permitir a adição de itens.
- **Dica:** Desabilitar ou limitar o campo de quantidade com base no inventário real.

### 🐞 Bug: Delay na atualização de preço/quantidade
- **Melhoria Sugerida:** Otimizar a comunicação assíncrona com o backend e adicionar indicadores visuais de carregamento.
- **Dica:** Usar `loading states` e `skeleton loaders` para indicar atualização em tempo real.

### 🐞 Bug: Alterações rápidas na quantidade causam valores incorretos
- **Melhoria Sugerida:** Implementar `debounce` ou `throttle` para evitar chamadas múltiplas ao backend.
- **Dica:** Bloquear o botão enquanto a requisição de quantidade ainda estiver em andamento.

### 🐞 Bug: Quantidade negativa pode ser exibida
- **Melhoria Sugerida:** Adicionar validação no campo de input para impedir valores menores que 1.
- **Dica:** Desabilitar botão de subtração quando a quantidade for 1.

---

## 🧾 RF06 - Checkout

### 🐞 Bug: Erro 500 ao excluir endereço usado no carrinho
- **Melhoria Sugerida:** Impedir a exclusão de endereços vinculados ao pedido atual. Exibir alerta informativo ao usuário.
- **Dica:** Permitir exclusão somente se o endereço não estiver em uso ativo (checkout, carrinho, etc.).

### 🐞 Bug: Falha ao finalizar pagamento
- **Melhoria Sugerida:** Verificar se o modo demo está corretamente configurado e se os métodos de pagamento estão funcionando no ambiente de testes.
- **Dica:** Simular pagamentos com um gateway de sandbox (ex: Stripe, PayPal, MercadoPago) e revisar logs.

---

## 👤 RF07 - Conta do Usuário

### ⚠️ Restrição: Não é possível deletar um endereço se estiver em uso
- **Melhoria Sugerida:** Exibir mensagem clara e impedir a exclusão de endereços vinculados a pedidos ou carrinhos ativos.
- **Dica:** Permitir substituição do endereço antes de solicitar exclusão.

---

## 💡 Sugestões Gerais

- ✔️ **Implementar validações em camadas**: frontend e backend devem validar os dados independentemente.
- 🔄 **Feedback visual em todas as ações**: usar loaders, alertas e mensagens claras.
- 📉 **Monitoramento de erros**: integrar ferramentas como Sentry, LogRocket ou console/logs server-side.
- 🧪 **Testes automatizados**: aplicar testes de regressão para comportamentos esperados, especialmente nos fluxos de carrinho, busca e checkout.

---

📅 Documento criado em: **15/06/2025**  
🧪 Ambiente testado: **Presta Shop**  
✍️ Elaborado por: **Miguel Luis**

