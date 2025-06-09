## 🚀 Teste de Performance Manual (Análise de Velocidade Percebida)

**Prioridade:** ALTA
**Objetivo:**
Avaliar a velocidade de carregamento percebida das páginas e a responsividade das principais ações no sistema.

---

### ⚙️ Abordagem

#### ⏱️ Carregamento de Páginas-Chave

Páginas analisadas:

* Homepage
* Páginas de Categoria (PLP)
* Páginas de Produto (PDP)
* Carrinho
* Checkout

**Critério subjetivo:**

* As páginas **carregam rapidamente** ou apresentam atrasos perceptíveis?

#### 📊 Análise com DevTools (Painel Network)

1. Limpe o cache do navegador:
   `Ctrl + Shift + Delete` → selecione "Imagens e arquivos armazenados em cache".

2. Ative o modo "Disable cache" no DevTools (F12) → aba **Network**.

3. Recarregue a página:
   `Ctrl + R` ou `Ctrl + F5`.

4. Observe os tempos de:

   * **DOMContentLoaded**
   * **Load**

5. Verifique:

   * Há arquivos muito grandes? (ex: imagens pesadas, JS/CSS mal otimizados)
   * Algum recurso está bloqueando o carregamento geral?

#### ⚡ Responsividade de Ações Interativas

Avaliar se as seguintes ações retornam resposta de forma **rápida e fluida**:

* ✅ **Adicionar produto ao carrinho**: confirmação é imediata?
* ✅ **Aplicar filtros na PLP**: produtos atualizam sem atraso?
* ✅ **Alterar quantidade no carrinho**: o recálculo ocorre instantaneamente?
* ✅ **Etapas do checkout**: as transições são ágeis e contínuas?

#### 🖼️ Impacto de Imagens

* As imagens estão otimizadas?
* Em conexões simuladas mais lentas (DevTools → Network → Throttling), as imagens **demoram a carregar**?
* Há **quebras de layout ou lentidão visual** associadas ao carregamento das imagens?
