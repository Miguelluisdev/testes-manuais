# 🐞 Relatório de Bugs Encontrados

📅 **Data dos Testes:** Junho de 2025  
🧪 **Tipo de Teste:** Manual  
🎯 **Ambiente:** BPrestaShop) 
📂 **Base:** Casos de teste dos RFs executados (RF01–RF06)  

---

## 🧩 Bugs por Requisito Funcional

---

### 🔐 RF01 - Login e Cadastro

#### 🐞 Bug 01: Erro ao tentar recuperar senha com e-mail válido
- **Severidade:** Alta
- **Comportamento Esperado:** Mensagem de sucesso ao enviar link de recuperação.
- **Comportamento Obtido:** Mensagem de erro:  
  > *"An error occurred while sending the email."*
- **Passos:**
  1. Acessar tela de login.
  2. Clicar em "Esqueci minha senha".
  3. Inserir e-mail válido e enviar.
- **Status:** Reproduzível

---

### 🔍 RF02 - Busca de Produto

#### 🐞 Bug 02: Termos curtos como "mu" não retornam resultados
- **Severidade:** Média
- **Comportamento Esperado:** Produtos relevantes relacionados ao termo parcial.
- **Comportamento Obtido:** "Nenhum resultado encontrado".

#### 🐞 Bug 03: Termos numéricos exibem resultados incoerentes
- **Severidade:** Média
- **Comportamento Esperado:** Filtragem coerente com nomes ou códigos de produtos.
- **Comportamento Obtido:** Resultados desconexos.

---

### 🛒 RF03 - Listagem de Produtos (PLP)

#### 🐞 Bug 04: Filtro por cor aplica cor errada
- **Severidade:** Alta
- **Comportamento Esperado:** Clicar em "White" exibe produtos brancos.
- **Comportamento Obtido:** Exibe produtos com cores diferentes (ex: preto).
- **Evidência:** [Vídeo](https://jam.dev/c/1ea3016f-b83c-4fe1-bd77-ed027868e010)

#### 🆕 Melhoria: Página recarrega a cada novo filtro aplicado
- **Severidade:** Baixa (UX)
- **Comportamento Esperado:** Atualização dinâmica sem reload total da página.
- **Comportamento Obtido:** Recarrega após cada clique.
- **Evidência:** [Vídeo](https://jam.dev/c/7a5e6621-28cf-4117-b79e-0e24f6079502)

---

### 🧺 RF05 - Carrinho de Compras

#### 🐞 Bug 05: Quantidade pode ultrapassar estoque
- **Severidade:** Alta
- **Comportamento Esperado:** Limite baseado em estoque do produto.
- **Comportamento Obtido:** Sem limite — possível adicionar quantidades excessivas.

#### 🐞 Bug 06: Delay ao alterar/remover produtos
- **Severidade:** Média
- **Comportamento Esperado:** Atualização imediata de valores no carrinho.
- **Comportamento Obtido:** Atraso perceptível de 1–2 segundos.

#### 🐞 Bug 07: Alterações rápidas de quantidade causam inconsistência
- **Severidade:** Alta
- **Comportamento Obtido:** Valor muda, mas volta para outro número aleatório.
- **Exemplo:** De 2 para 10 → volta para 8 ou 5.
- **Evidência:** [Vídeo](https://jam.dev/c/7237e2ee-975b-44b9-9bd7-120ed07dac2f)

#### 🐞 Bug 08: Quantidade pode ser negativa
- **Severidade:** Alta
- **Mensagem:**  
  > *"The minimum purchase order quantity for the product [...] is 1."*

---

### 💳 RF06 - Processo de Checkout

#### 🐞 Bug 09: Erro 500 ao excluir endereço no checkout
- **Severidade:** Crítica
- **Mensagem:**  
  > *"500 Server Error — Try to refresh this page or contact support."*
- **Causa:** Tentativa de excluir endereço em uso.
- **Evidência:** [Vídeo](https://jam.dev/c/345c8764-70d5-4266-b701-8e3083be8f83)

#### 🐞 Bug 10: Checkout falha na etapa de pagamento
- **Severidade:** Crítica
- **Comportamento Esperado:** Concluir simulação de pagamento (modo demo).
- **Comportamento Obtido:** Processo falha e não avança.
- **Evidência:** [Vídeo](https://jam.dev/c/d58163e8-62db-4999-9b00-293930fe2af1)

---

## ✅ Conclusão

- Foram encontrados **10 bugs** com diferentes níveis de severidade, sendo **3 críticos**, relacionados ao **checkout** e à **quantidade de produtos no carrinho**.
- Todos os bugs possuem documentação clara, muitos com **evidência em vídeo (Jam.dev)**.
- Melhorias adicionais de usabilidade também foram identificadas.

---

✍️ **Autor:** Miguel  
📂 **Associado ao Plano de Testes:** RF01–RF06  
🧪 **Metodologia:** Manual + Exploratório
