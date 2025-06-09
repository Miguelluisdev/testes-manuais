## ♿ Testes de Acessibilidade (Básicos com DevTools)

**Prioridade:** MÉDIA
**Objetivo:**
Verificar se os elementos HTML estão otimizados para acessibilidade, utilizando ferramentas básicas do navegador.

---

### 🧪 Abordagem

#### 🧱 Tags Semânticas HTML5

* Utiliza `<header>`, `<footer>`, `<nav>`, `<main>`, `<article>`, `<aside>`, `<section>` de forma apropriada?
* Evita uso excessivo de `<div>` para estrutura?
* Os cabeçalhos (`<h1>` a `<h6>`) estão em ordem lógica e hierárquica?
  (Ex: não usar `<h3>` logo após `<h1>`)

#### 🖼️ Atributos `alt` em Imagens

* Imagens **relevantes** (logo, banners, produtos) possuem `alt` com descrição clara e útil?
* Imagens **decorativas** possuem `alt=""` (vazio) para serem ignoradas por leitores de tela?

#### 🏷️ Rótulos de Formulário (`<label>`)

* Cada `input`, `select`, `textarea` tem um `<label>` associado corretamente?
* O atributo `for` do `<label>` aponta para o `id` do campo correspondente?
* Clicar no texto do `label` foca o campo correto?

#### 🎨 Contraste de Cores (Verificação Básica)

* Use o **DevTools > Computed/Styles** para checar contraste entre texto e fundo.
* O navegador indica se o contraste atende aos padrões **WCAG** (AA ou AAA).
* Verificar especialmente em:

  * Textos de leitura
  * Botões
  * Links

#### ⌨️ Navegação por Teclado

* Use a tecla **Tab** para navegar:

  * A ordem de foco é lógica e segue a ordem visual?
  * O foco é visível (ex: outline, sombra, borda)?
* Testar interações:

  * `Enter` ativa botões e links
  * `Espaço` ativa checkboxes e radios
  * Menus dropdown são navegáveis por teclado?

#### 👁️ Painel "Accessibility" no DevTools

* Use a aba **"Accessibility"** no DevTools (Chrome/Edge):

  * Verifique **Nome**, **Função**, **Estado** dos elementos selecionados.
  * Ajuda a visualizar como os leitores de tela interpretam os componentes.

---

### 🛠️ Dica Extra

Use a ferramenta **Lighthouse** (no DevTools) → aba **"Accessibility"**
Ela fornece uma **pontuação automática** e **recomendações** de melhoria para acessibilidade.
