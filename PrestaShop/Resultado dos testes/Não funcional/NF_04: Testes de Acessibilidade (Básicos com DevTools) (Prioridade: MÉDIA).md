# 📋 Relatório de Testes - PrestaShop Demo

## 🛠️ Ferramenta Utilizada
- **Google Lighthouse** (via DevTools - Google Chrome)
- **DevTools - Acessibilidade**
- **Jam.dev** para gravação da análise de performance

---

## 📊 Resultados da Auditoria Lighthouse

| Categoria              | Nota | Status         |
|------------------------|------|----------------|
| 💨 Desempenho          | 86   | Boa            |
| ♿ Acessibilidade       | 93   | Excelente      |
| ✅ Boas Práticas       | 59   | Ruim           |
| 🔍 SEO                 | 91   | Excelente      |

> ⚠️ Observação: A análise de performance pode estar comprometida devido a extensões do Chrome ativas no momento da auditoria. Idealmente, o teste deve ser feito no **modo anônimo** ou com as extensões desativadas.

---

## ♿ Análise de Acessibilidade com DevTools

### ✅ Tags Semânticas
- A página utiliza tags semânticas como `<header>`, `<main>`, `<footer>` e `<nav>`.
- A hierarquia de títulos está estruturada corretamente, respeitando a sequência lógica dos heading tags.

### 🖼️ Atributo `alt` nas Imagens
- Imagens relevantes possuem o atributo `alt` descritivo.
- Imagens decorativas foram corretamente configuradas com `alt=""`.

### 🏷️ Formulários com `label`
- Todos os campos de formulário possuem `<label>` associado via `for="id"`.
- A navegação entre campos por `Tab` está fluida.

### 🎨 Contraste de Cores
- O contraste de cores entre texto e plano de fundo foi avaliado e está dentro dos padrões mínimos exigidos pelo WCAG (nível AA).
- Botões e links estão legíveis.

### ⌨️ Navegação por Teclado
- A navegação por teclado está funcionando conforme o esperado:
  - `Tab` e `Shift+Tab` respeitam a ordem lógica.
  - Foco visível ao navegar entre elementos interativos.
  - `Enter` e `Espaço` ativam os elementos apropriados.
  
### 👁️ Painel de Acessibilidade (DevTools)
- Elementos interativos possuem nome, função e estado identificáveis.
- ARIA roles estão corretamente aplicados onde necessário.

---

## 🧪 Pontos de Melhoria

### ⚠️ Boas Práticas (Score: 59)
- Verificar se há bibliotecas desatualizadas ou inseguras.
- Assegurar que todas as requisições utilizam HTTPS.
- Implementar segurança adicional para evitar práticas desatualizadas.

---

## 🎥 Evidência em Vídeo

- Link: [Jam.dev - Auditoria de Performance](https://jam.dev/c/75d5be7f-6988-4d55-892a-f6b2129a0027)

---

## ✅ Conclusão

A auditoria do site de demonstração do **PrestaShop** revela um bom nível de **acessibilidade**, com estrutura semântica adequada, contraste legível, navegação por teclado e boas práticas de HTML. Porém, recomenda-se investigar as **boas práticas técnicas** para atingir um padrão mais alto de segurança e confiabilidade.

---

📅 **Data da Auditoria:** 11 de Junho de 2025  
🔍 **QA:** Miguel Luis  
🧪 **Ambiente:** Google Chrome com extensões ativas  
🌐 **URL Avaliada:** [https://demo.prestashop.com](https://demo.prestashop.com)
