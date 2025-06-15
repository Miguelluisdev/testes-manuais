# 🔎 Análise de Causa Raiz dos Bugs Encontrados

📅 **Data da Análise:** Junho de 2025  
🔧 **Base:** Testes manuais realizados nos RF01–RF06  
📁 **Tipo:** Root Cause Analysis (RCA)  
🧪 **Contexto:** Plataforma e-commerce (PrestaShop)

---

## RF01 - Login e Cadastro

### 🐞 Bug 01: Erro ao tentar recuperar senha com e-mail válido

- **Causa Raiz:** Endpoint de recuperação de senha pode estar desabilitado, mal configurado ou sem integração com serviço de e-mail SMTP.
- **Impacto:** Usuários não conseguem redefinir a senha.
- **Sugestão Técnica:** Verificar logs do servidor e configuração de envio de e-mail (ex: SMTP/Sendmail). Testar endpoint isoladamente com ferramentas como Postman.
---

## RF02 - Busca de Produto

### 🐞 Bug 02: Termos curtos como "mu" não retornam resultados

- **Causa Raiz:** Limitação na implementação do mecanismo de busca (ex: busca exige no mínimo 3 caracteres).
- **Impacto:** Experiência de usuário prejudicada, especialmente em produtos com nomes curtos.
- **Sugestão Técnica:** Revisar configuração do índice de busca e lógica de correspondência parcial.

### 🐞 Bug 03: Termos numéricos exibem resultados incoerentes

- **Causa Raiz:** Falta de tratamento adequado de inputs numéricos (ex: busca genérica por números retorna qualquer valor de SKU, preço ou atributos).
- **Impacto:** Gera confusão ao usuário e resultados irrelevantes.
- **Sugestão Técnica:** Implementar filtros para tipos de busca e regras específicas para números.

---

## RF03 - Listagem de Produtos (PLP)

### 🐞 Bug 04: Filtro por cor aplica cor errada

- **Causa Raiz:** Atributo de cor pode estar mal associado ao produto no banco de dados ou a lógica de exibição não reflete a seleção.
- **Impacto:** Exibe produtos com cores diferentes da filtrada.
- **Sugestão Técnica:** Validar mapeamento entre atributos e produtos. Conferir estrutura do banco e consulta SQL/GraphQL.

### 🐞 Bug 05 (UX): Reload da página a cada filtro aplicado

- **Causa Raiz:** Ausência de renderização assíncrona (AJAX). Cada filtro dispara um reload completo.
- **Impacto:** Experiência lenta e pouco fluida.
- **Sugestão Técnica:** Implementar filtros com AJAX e reatividade frontend (ex: Vue/React).

---

## RF05 - Carrinho de Compras

### 🐞 Bug 06: Sem limite de estoque na quantidade adicionada

- **Causa Raiz:** Falta de validação no frontend e backend para validar estoque disponível.
- **Impacto:** Inconsistência entre produto disponível e o que é exibido no carrinho.
- **Sugestão Técnica:** Implementar lógica de verificação do estoque atual ao clicar no botão de adicionar.

### 🐞 Bug 07: Delay ao alterar/remover itens

- **Causa Raiz:** Execução de operações síncronas com delays de renderização ou espera de resposta do servidor.
- **Impacto:** Feedback lento ao usuário.
- **Sugestão Técnica:** Adicionar indicadores de carregamento e otimizar requisições assíncronas.

### 🐞 Bug 08: Alterações rápidas causam inconsistência

- **Causa Raiz:** Condição de corrida (race condition) entre o clique do usuário e a resposta do servidor.
- **Impacto:** Quantidade no carrinho muda inesperadamente.
- **Sugestão Técnica:** Implementar debounce/throttle nas interações e garantir estado sincronizado no frontend.

### 🐞 Bug 09: Quantidade negativa no carrinho

- **Causa Raiz:** Falta de validação ao tentar diminuir abaixo do mínimo permitido.
- **Impacto:** Mensagens de erro inesperadas e lógica quebrada.
- **Sugestão Técnica:** Implementar validação no frontend para impedir valores < 1 e desabilitar botão de decremento quando necessário.

---

## RF06 - Checkout

### 🐞 Bug 10: Erro 500 ao excluir endereço

- **Causa Raiz:** O sistema tenta excluir um endereço em uso no carrinho ou na sessão do checkout, causando conflito.
- **Impacto:** Interrupção no processo de finalização.
- **Sugestão Técnica:** Impedir exclusão de endereços ativos ou reapontar o endereço selecionado antes da exclusão.

### 🐞 Bug 11: Checkout falha na etapa de pagamento (modo demo)

- **Causa Raiz:** Endpoint de pagamento desativado, configuração incorreta ou conflito com método de pagamento selecionado.
- **Impacto:** Processo de compra é bloqueado.
- **Sugestão Técnica:** Validar se o modo demo está corretamente ativado. Revisar logs de erros no back-end.

---

## Conclusão Geral

| Bug ID | Severidade | Área Impactada | Causa Provável | Ação Recomendada |
|--------|------------|----------------|----------------|------------------|
| Bug 01 | Alta       | RF01           | Config SMTP/API | Revisar envio de e-mail |
| Bug 02 | Média      | RF02           | Filtro por tamanho de string | Melhorar indexador |
| Bug 04 | Alta       | RF03           | Associações incorretas | Revisar atributos |
| Bug 06 | Alta       | RF05           | Validação ausente | Validar estoque no back e front |
| Bug 10 | Crítica    | RF06           | Conflito de uso | Impedir exclusão de item ativo |
| Bug 11 | Crítica    | RF06           | Endpoint quebrado | Revisar config. de pagamento |

---

✍️ **Autor da Análise:** Miguel Luis
📅 **Data:** 15/06/2025  
🧪 **Metodologia:** RCA via observação + inferência técnica

