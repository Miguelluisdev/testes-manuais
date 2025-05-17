## 🧪 **Plano de Testes - Demo SaaS**

### 📌 1. **Identificação**

* **Nome do Projeto**: Demo SaaS - Sistema de Gerenciamento de Tickets
* **Versão Avaliada**: Demo pública
* **Ambiente de Testes**: [https://demo-saas.bugbug.io/](https://demo-saas.bugbug.io/)
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 17/05/2025
* **Responsável**: Miguel Luis

---

### 🎯 2. **Objetivo**

Validar manualmente os principais requisitos funcionais do sistema Demo SaaS, assegurando a conformidade com os comportamentos esperados, mensagens de erro claras, usabilidade e estabilidade da aplicação web.

---

### 🧩 3. **Escopo**

**Incluído:**

* Autenticação de usuário (login e recuperação de senha)
* Cadastro de novo usuário
* Criação de organizações
* Gestão de conta (perfil e segurança)
* Dashboard com tickets
* Gerenciamento e visualização de tickets
* Convidar membro no Settings

**Excluído:**

* Integração com email real para reset de senha (testes simulados)
* Testes responsivos e mobile
* Testes de performance ou segurança profunda

---

### ⚖️ 4. **Ferramentas Utilizadas**

* Navegador Microsoft Edge v.136.0 
* Ferramentas de inspeção (DevTools) e Selion
* Google Sheets (registro de execução e bugs)
* Captura de tela (JAM)

---

### 🧪 5. **Técnicas de Teste**

* Caminho feliz (Happy Path)
* Testes negativos
* Análise de valor limite
* Testes exploratórios
* Caminho Alternativo

---

### 📄 6. **Critérios de Aceitação**

* Todos os casos de teste devem ter resultado "Aprovado".
* As mensagens de erro devem ser claras e coerentes.
* Fluxos principais devem ser executados sem falhas.

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* 100% dos testes executados.
* Evidências anexadas e bugs documentados.
* Testes reexecutados após correções (quando aplicável).

---

### ⏱️ 8. **Cronograma Estimado**

| Atividade                   | Data Início | Data Fim   |
| --------------------------- | ----------- | ---------- |
| Planejamento de Testes      | 17/05/2025  | 17/05/2025 |
| Criação de Casos de Teste   | 17/05/2025  | 18/05/2025 |
| Execução dos Testes Manuais | 18/05/2025  | 20/05/2025 |
| Registro e Report de Bugs   | 18/05/2025  | 20/05/2025 |
| Encerramento e Evidências   | 20/05/2025  | 20/05/2025 |

---

### 📋 9. **Módulos a Serem Testados**

| Código RF | Módulo                     | Prioridade |
| --------- | -------------------------- | ---------- |
| RF01      | Login                      | Alta       |
| RF02      | Cadastro                   | Alta       |
| RF03      | Criação de Organização     | Média      |
| RF04      | Gestão de Conta            | Média      |
| RF05      | Dashboard de Tickets       | Alta       |
| RF06      | Tabela e Busca de Tickets  | Alta       |
| RF07      | Navegação e Usabilidade    | Alta       |
| RF08      | Convidar Membro (Settings) | Média      |
| RF09      | Recuperação de Senha       | Alta       |

---

### 🐞 10. **Gestão de Defeitos**

* Bugs serão registrados com:

  * Título
  * Descrição
  * Passos para reproduzir
  * Evidência (print ou vídeo)
  * Gravidade (Crítica, Alta, Média, Baixa)

* Ferramenta usada: Google Sheets

---

Aqui estão mais riscos possíveis para o projeto de testes manuais do **Demo SaaS**, mantendo o padrão do seu plano:

---

### 📌 11. **Riscos Identificados**

| Risco                                           | Impacto | Mitigação                                     |
| ----------------------------------------------- | ------- | --------------------------------------------- |
| Sistema temporariamente indisponível            | Alto    | Retestar após intervalo de tempo              |
| Dados da demo podem ser apagados                | Médio   | Refazer cenários se necessário                |
| Login social pode não funcionar sempre          | Médio   | Testar com email clássico também              |
| Funcionalidades novas não documentadas          | Médio   | Realizar testes exploratórios e documentar    |
| Layout pode mudar sem aviso                     | Baixo   | Validar fluxo mesmo com mudanças visuais      |
| Falta de mensagens de erro padronizadas         | Médio   | Validar consistência e reportar variações     |
| Bugs intermitentes (difíceis de reproduzir)     | Médio   | Gravar a execução e documentar padrões        |
| Incompatibilidade com navegadores específicos   | Médio   | Testar em navegadores diferentes              |
| Restrições de idioma/localização                | Baixo   | Testar interface e mensagens em inglês padrão |
| Limitação de acesso a funcionalidades por conta | Médio   | Explorar todas as possibilidades permitidas   |
| Campos sem validação adequada                   | Alto    | Testar com dados inválidos                    |

---

### 📁 12. **Entregáveis**

* Plano de Testes (.md)
* Casos de Teste por RF (.md)
* Evidências de Execução (prints organizados)
* Registro de Bugs (planilha ou .md)
* Relatório Final de Execução

