## 🧪 **Plano de Testes - PrestaShop Demo**

### 📌 1. **Identificação**

* **Nome do Projeto**: PrestaShop Demo - Loja Internacional de Roupas e Utensílios
* **Versão Avaliada**: Demo pública
* **Ambiente de Testes**: [https://demo.prestashop.com/#/en/front](https://demo.prestashop.com/#/en/front)
* **Tipo de Teste**: Teste Funcional Manual e Exploratórios
* **Data do Documento**: 06/06/2025
* **Responsável**: Miguel Luis

---

### 🎯 2. **Objetivo**

Realizar testes manuais funcionais e exploratórios na loja virtual PrestaShop Demo com o objetivo de validar os principais requisitos funcionais, usabilidade, comportamento esperado e levantar falhas, inconsistências ou limitações técnicas para posterior documentação e planejamento de testes mais estruturados.

---

### 🧩 3. **Escopo**

**Incluído:**

* Navegação pelas páginas principais (home, PLP, PDP)
* Login e gerenciamento de perfil do usuário
* Carrinho de compras e wishlist
* Funcionalidade de tradução de idioma
* Processo de checkout (pagamento multistep)
* Avaliações e compartilhamento de produtos
* Teste de responsividade e layout
* Validações de formulário

**Excluído:**

* Integração com pagamento real
* Fluxo de administração (Back Office)
* Integrações com transportadoras e impostos
* Testes mobile nativos ou app

---

### ⚖️ 4. **Ferramentas Utilizadas**

* Navegador Microsoft Edge v.137.0
* Ferramentas de inspeção (DevTools)
* Google Sheets (registro de bugs e execução)
* Gravador de tela e capturas para evidência (Jam.dev)
* Notepad (anotações importantes)

---

### 🧪 5. **Técnicas de Teste**

* Caminho feliz (Happy Path)
* Testes negativos (valores inválidos)
* Partição de equivalência
* Teste exploratório livre
* Caminhos alternativos (como idioma, sem login, etc.)

---

### 📄 6. **Critérios de Aceitação**

* Todas as funcionalidades principais devem funcionar conforme o esperado.
* Campos obrigatórios devem exibir mensagens de erro adequadas.
* O fluxo de compra deve ser possível sem bloqueios indevidos.
* Links e botões devem ser responsivos e funcionais.
* A aplicação deve responder bem às ações do usuário.

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* 100% dos módulos testados.
* Registro completo de bugs encontrados.
* Evidências capturadas (prints ou vídeos).
* Documentação do teste exploratório finalizada.

---

### ⏱️ 8. **Cronograma Estimado**

| Atividade                   | Data Início | Data Fim   |
| --------------------------- | ----------- | ---------- |
| Execução do Teste Explorat. | 04/06/2025  | 04/06/2025 |
| Planejamento de Testes      | 06/06/2025  | 06/06/2025 |
| Documentação e Evidências   | 07/06/2025  | 07/06/2025 |
| Registro de Bugs            | 08/06/2025  | 08/06/2025 |

---

### 📋 9. **Módulos a Serem Testados**

| Código RF | Módulo                       | Prioridade |
| --------- | ---------------------------- | ---------- |
| RF01      | Login e Autenticação         | Alta       |
| RF02      | Tradução e Idioma            | Média      |
| RF03      | Navegação e Responsividade   | Alta       |
| RF04      | Carrinho e Wishlist          | Alta       |
| RF05      | Página do Produto (PDP)      | Alta       |
| RF06      | Processo de Checkout         | Alta       |
| RF07      | Avaliação e Compartilhamento | Média      |
| RF08      | Contato e Suporte            | Média      |
| RF09      | Gerenciamento do Perfil      | Alta       |
| RF10      | Validação de Formulários     | Alta       |
| RF11      | Breadcrumbs e Pesquisa       | Média      |

---

### 🐞 10. **Gestão de Defeitos**

* Bugs serão registrados com:

  * ID e título do bug
  * Descrição detalhada
  * Passos para reproduzir
  * Resultado esperado x obtido
  * Severidade (Crítico, Alto, Médio, Baixo)
  * Evidência (screenshot ou vídeo)

* Ferramenta usada: Google Sheets

---

### 📌 11. **Riscos Identificados**

| Risco                                    | Impacto | Mitigação                                |
| ---------------------------------------- | ------- | ---------------------------------------- |
| Funções restritas sem login              | Médio   | Testar fluxos logado e não logado        |
| Bugs intermitentes no botão de checkout  | Alto    | Repetir testes e gravar tentativa        |
| Carregamento lento em alguns momentos    | Médio   | Validar em horários diferentes           |
| Tradução não funcional sem login         | Médio   | Registrar como limitação                 |
| Restrições geográficas no checkout       | Médio   | Verificar impacto no fluxo de teste      |
| Layout pode ser alterado pela plataforma | Baixo   | Registrar nova versão no início do teste |

---

### 📁 12. **Entregáveis**

* Plano de Testes (.md)
* Casos de Teste por RF (.md)
* Registro de bugs com evidência (.md ou planilha)
* Relatório de Teste Exploratório (.md)
* Prints e vídeos organizados como evidência
