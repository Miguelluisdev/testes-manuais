### 🧭 Plano de Testes Exploratórios — Swag Labs

#### 🎯 Objetivo

Explorar a aplicação com foco em **autenticação**, **navegação**, **adicionar/remover produtos**, **carrinho**, e **checkout**, buscando identificar comportamentos inesperados, problemas de fluxo, usabilidade ou inconsistências.

---

### 📌 Informações Gerais

| Item             | Detalhe                                                                            |
| ---------------- | ---------------------------------------------------------------------------------- |
| Sistema Testado  | Swag Labs                                                                          |
| URL              | [https://www.saucedemo.com/v1/index.html](https://www.saucedemo.com/v1/index.html) |
| Tipo de Teste    | Exploratórios (Manuais)                                                            |
| Navegadores Alvo | Microsoft Edge v138                                                              |
| Ambiente         | Produção pública                                                                   |
| Data do Teste    | 28/07/2025                                                           |
| Responsável      | Miguel Luis                                                                        |

---

### 🧪 Credenciais de Teste (públicas)

| Tipo de Usuário    | Username                  | Senha         |
| ------------------ | ------------------------- | ------------- |
| Padrão             | standard\_user            | secret\_sauce |
| Travado            | locked\_out\_user         | secret\_sauce |
| Problema de imagem | problem\_user             | secret\_sauce |
| Demorado           | performance\_glitch\_user | secret\_sauce |

---

### 🔍 Charter 1: Autenticação

| Charter          | Validar o comportamento do login                           |
| ---------------- | ---------------------------------------------------------- |
| Meta             | Investigar diferentes tipos de login e resposta do sistema |
|conclusão |                                         (pequeno resumo se foi envontrado bugs ou passou sem bugs)                   |

* O que acontece ao usar logins inválidos?
* O sistema informa claramente o erro?
* Usuário travado (locked\_out\_user) exibe erro claro?
* Há feedback visual (ex: loading)?
* O campo de senha permite visualização?

---

### 🔍 Charter 2: Navegação e Itens na Loja

| Charter          | Avaliar experiência na loja e navegação entre páginas   |
| ---------------- | ------------------------------------------------------- |
| Meta             | Verificar como o usuário interage com produtos e navega |
|conclusão |                                         (pequeno resumo se foi envontrado bugs ou passou sem bugs)                   |

* Produtos aparecem corretamente?
* Itens quebrados (ex: imagens do problem\_user)?
* Clicar em um item leva à página de detalhes?
* O botão “Back to Products” funciona?
* O botão de filtro (Sort A-Z, Price, etc.) altera a ordem?

---

### 🔍 Charter 3: Carrinho de Compras

| Charter          | Explorar o comportamento do carrinho              |
| ---------------- | ------------------------------------------------- |
| Meta             | Avaliar como produtos são adicionados e removidos |
|conclusão |                                         (pequeno resumo se foi envontrado bugs ou passou sem bugs)                   |

* É possível adicionar múltiplos itens?
* Remover um item funciona corretamente?
* Badge com número de itens no ícone é atualizado corretamente?
* O carrinho mantém o estado ao navegar entre páginas?

---

### 🔍 Charter 4: Checkout

| Charter          | Testar todo o fluxo de finalização de compra           |
| ---------------- | ------------------------------------------------------ |
| Meta             | Verificar consistência, validações e término do pedido |
|conclusão |                                         (pequeno resumo se foi envontrado bugs ou passou sem bugs)                   |

* O botão de checkout está visível e funcional?
* Há validação para campos obrigatórios?
* O fluxo avança corretamente entre as etapas?
* O botão “Finish” leva à página de confirmação?
* Após o pedido, o carrinho é limpo?

---

### 🔍 Charter 5: Usabilidade e Experiência Geral

| Charter          | Avaliar UX e comportamento responsivo    |
| ---------------- | ---------------------------------------- |
| Meta             | Testar comportamento visual e responsivo |
|conclusão |                                         (pequeno resumo se foi envontrado bugs ou passou sem bugs)                   |

* Layouts quebram em tamanhos menores?
* Texto é legível e botões têm tamanho adequado?
* Existem falhas de contraste ou acessibilidade?
* Há mensagens de erro claras e amigáveis?

---

### 📋 Registro de Descobertas

Durante a execução, registre os seguintes pontos:

| Tipo              | Descrição                                                        |
| ----------------- | ---------------------------------------------------------------- |
| 💥 Bug            | Erros ou comportamentos inesperados (ex: botão que não responde) |
| ⚠️ Inconsistência | Diferença entre comportamento esperado e obtido                  |
| 💡 Ideia          | Sugestões de melhoria para o sistema                             |
| 🤔 Observação     | Detalhes interessantes ou pontos ambíguos                        |

---

### ✅ Dicas para Execução

* Use diferentes perfis de usuário.
* Troque entre navegadores.
* Varie a ordem dos cliques e interações.
* Teste com inputs inesperados (ex: strings longas).
* Faça refresh e volte nas páginas.

