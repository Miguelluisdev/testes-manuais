## 📦 **Requisitos Funcionais Detalhados para Testes Manuais**



### 🔐 **RF01 - Autenticação de Usuário**

  * O sistema deve permitir que o usuário realize login com nome de usuário e senha válidos.

  * O sistema deve exibir mensagens de erro em caso de login inválido.

---

### 🏠 **RF02 - Dashboard Inicial**

**Descrição**: Após o login, o sistema deve exibir o painel com atalhos rápidos e widgets.

* **Funcionalidades esperadas**:

  * Exibição de widgets de: Empregados Ausentes, Avisos, Fluxo de Trabalho.
  * Navegação funcional pelos menus laterais.
  * Acesso rápido às áreas Admin, PIM, Leave, Time, Recruitment etc.

---

### 👤 **RF03 - Gestão de Funcionários (Módulo PIM)**

**Descrição**: O sistema deve permitir o gerenciamento completo de colaboradores.

* **Funcionalidades esperadas**:

  * Listagem de todos os funcionários cadastrados.
  * Filtros de busca por nome, ID, cargo, status.
  * Botão "Add" para adicionar um novo funcionário.
  * Opção de editar ou excluir um funcionário existente.

---

### 📅 **RF04 - Gerenciamento de Férias (Leave)**

**Descrição**: Permitir ao administrador visualizar e gerenciar requisições de licença.

* **Funcionalidades esperadas**:

  * Filtro de solicitações por data, status, nome do colaborador.
  * Aprovação ou rejeição de solicitações.
  * Visualização do saldo de férias do funcionário.

---

### 🧾 **RF05 - Recrutamento (Recruitment)**

**Descrição**: O sistema deve permitir a gestão de candidatos e vagas abertas.

* **Funcionalidades esperadas**:

  * Visualização da lista de vagas e candidatos.
  * Adição de novos candidatos.
  * Filtro por nome do candidato, cargo e status.

---

### 🛠️ **RF06 - Administração (Admin)**

**Descrição**: Gerenciar usuários, papéis e permissões.

* **Funcionalidades esperadas**:

  * Adicionar usuários ao sistema com diferentes níveis de acesso.
  * Editar e deletar usuários.
  * Aplicar filtros por tipo de usuário, status e nome.

---

### ⏱ **RF07 - Controle de Ponto (Time)**

**Descrição**: Gerenciar registros de entrada/saída dos funcionários.

* **Funcionalidades esperadas**:

  * Visualização dos horários registrados por funcionário.
  * Filtros por nome, data, status.
  * Geração de relatórios de tempo.

---

### 📈 **RF08 - Relatórios**

**Descrição**: O sistema deve permitir a geração de relatórios diversos (PIM, Férias, etc.).

* **Funcionalidades esperadas**:

  * Selecionar tipo de relatório (Ex: Employee Details Report)
  * Definir filtros personalizados.
  * Gerar e visualizar relatório.

---

### 📂 **RF09 - Diretório**

**Descrição**: Lista pública dos colaboradores da empresa.

* **Funcionalidades esperadas**:

  * Filtro por nome, cargo, localização.
  * Exibição das informações básicas de cada funcionário.

---

### ⚙️ **RF10 - Manutenção**

**Descrição**: Módulo com controle de senhas e logs.

* **Funcionalidades esperadas**:

  * Acesso mediante reautenticação (Admin).
  * Lista de logs de auditoria do sistema.
  * Possibilidade de buscar eventos por data, usuário ou ação.

---

### 🎓 **RF11 - Qualificações (My Info > Qualifications)**

**Descrição**: Visualizar e editar qualificações dos funcionários.

* **Funcionalidades esperadas**:

  * Adição de cursos, línguas e certificações.
  * Edição e remoção de qualificações.
  * Upload de documentos relacionados.
