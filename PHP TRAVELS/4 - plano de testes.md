## 🧪 Plano de Testes - PHPTRAVELS.NET

### 📌 1. Identificação

* **Nome do Projeto**: PHPTRAVELS.NET – Sistema de Demonstração de Reservas Online
* **Versão Avaliada**: Demo Pública
* **Ambiente de Testes**: [https://phptravels.net](https://phptravels.net)
* **Tipo de Teste**: Testes Manuais Funcionais e Exploratórios
* **Data do Documento**: 27/06/2025
* **Responsável**: Miguel Luis

---

### 🎯 2. Objetivo

Realizar testes manuais funcionais e exploratórios na plataforma de demonstração PHPTRAVELS.NET, com foco na validação dos requisitos funcionais e regras de negócio mais relevantes para o usuário final.

Além disso, serão utilizadas **heurísticas de software** para guiar o pensamento crítico e a investigação exploratória durante a execução dos testes.

---

### 🧩 3. Escopo

**Incluído:**

* Módulo de busca principal (hotéis, voos, passeios, carros, visto)
* Cadastro e login de usuários
* Acesso e edição do painel do cliente
* Processo de reserva (fluxo demonstrativo)
* Troca de idioma e moeda
* Validações de formulários
* Página de resultados e filtros
* Página de detalhes (hotel, voo, etc.)
* Funcionalidades do perfil: bookings, perfil, logout

**Excluído:**

* Integrações reais com sistemas de pagamento
* Painel administrativo (backoffice)
* Testes de desempenho (carga ou estresse)
* Testes de segurança avançados (ex: injeção, pen test)
* Funcionalidades relacionadas a e-mails reais

---

### ⚖️ 4. Ferramentas Utilizadas

* Navegador Microsoft Edge v.137.0
* DevTools (inspeção de elementos e logs)
* Google Sheets (gestão de testes e bugs)
* Notepad (registro de anotações livres)
* Gravador de tela e prints (Jam.dev)

---

### 🧪 5. Técnicas de Teste

* **Happy Path** (Caminho feliz)
* **Testes Negativos** (valores inválidos, inputs vazios)
* **Partição de Equivalência**
* **Análise de Valor Limite**
* **Caminhos Alternativos**
* **Testes Exploratórios com base em Heurísticas de Software**, como:
  * H-T-C (Heurística de Consistência com o Histórico, Tendência e Cliente)
  * CRUD (Create, Read, Update, Delete)
  * SFDPOT (Estrutura, Função, Dados, Plataforma, Operações, Tempo)
  * Oracles de Erro (consistência, ausência, reversibilidade, etc.)

---

### 📄 6. Critérios de Aceitação

* Cada funcionalidade testada deve funcionar conforme descrito nos requisitos.
* As mensagens de erro devem ser claras e informativas.
* Os campos obrigatórios devem ser validados corretamente.
* A reserva demonstrativa deve concluir sem bloqueios.
* Feedbacks visuais devem ocorrer em interações com botões, campos, etc.
* As seleções de idioma e moeda devem refletir em toda a interface.
* O sistema deve se comportar adequadamente em diferentes navegadores.

---

### 🚦 7. Critérios de Saída (Exit Criteria)

* 100% dos testes planejados executados.
* Casos de testes com status documentado (Passou/Falhou).
* Todos os bugs encontrados devidamente registrados com evidência.
* Relatório de exploração executado e documentado.
* Print screens e vídeos organizados e catalogados por funcionalidade.

---

### ⏱️ 8. Cronograma Estimado

| Atividade                   | Data Início | Data Fim   |
| --------------------------- | ----------- | ---------- |
| Execução de Testes Exploratórios | 26/06/2025 | 27/06/2025 |
| Planejamento e Casos de Teste    | 27/06/2025 | 28/06/2025 |
| Execução de Testes Funcionais   | 28/06/2025 | 01/07/2025 |
| Registro de Bugs e Evidências   | 01/07/2025 | 02/07/2025 |
| Relatório Final e Organização   | 02/07/2025 | 03/07/2025 |

---

### 📋 9. Módulos a Serem Testados

| Código RF | Módulo                                  | Prioridade |
|-----------|------------------------------------------|------------|
| RF01      | Módulo de Busca (hotéis, voos, etc.)     | Alta       |
| RF02      | Login e Cadastro                         | Alta       |
| RF03      | Página de Resultados e Filtros           | Alta       |
| RF04      | Página de Detalhes do Item               | Média      |
| RF05      | Processo de Reserva e Pagamento Simulado | Alta       |
| RF06      | Troca de Idioma e Moeda                  | Média      |
| RF07      | Acesso ao Painel do Cliente              | Alta       |
| RF08      | Logout e Persistência de Sessão          | Média      |
| RNF01     | Usabilidade e mensagens                  | Média      |
| RNF02     | Compatibilidade e responsividade         | Média      |

---

### 🐞 10. Gestão de Defeitos

* Os defeitos serão registrados contendo:
  * ID único e título
  * Descrição detalhada do problema
  * Passos para reprodução
  * Resultado esperado vs obtido
  * Severidade (Crítico, Alto, Médio, Baixo)
  * Evidência (print ou vídeo)
* Ferramenta utilizada: **Google Sheets + Jam.dev para evidências**

---

### 📌 11. Riscos Identificados

| Risco                                           | Impacto | Mitigação                                 |
|------------------------------------------------|---------|--------------------------------------------|
| Funcionalidade de reserva não persistente      | Médio   | Validar em várias sessões e usuários       |
| Bugs intermitentes em filtros de busca         | Alto    | Repetir testes e usar gravação de tela     |
| Tradução parcial em idiomas diferentes do inglês| Médio   | Registrar como limitação do sistema demo   |
| Variações frequentes no conteúdo do site       | Médio   | Revalidar elementos antes de cada execução |
| Sem acesso ao backend                          | Baixo   | Foco exclusivo no fluxo do usuário final   |

---

### 📁 12. Entregáveis

* Plano de Testes (.md)
* Casos de Teste Manuais (.md)
* Relatório de Bugs com Evidências (.md/.xlsx)
* Relatório de Testes Exploratórios (.md)
* Prints e vídeos organizados por cenário/teste

---

🎯 **Nota Final**: Este plano visa garantir a cobertura de testes nos fluxos mais relevantes da plataforma, com foco em simular o comportamento do usuário real e identificar falhas ou inconsistências que possam comprometer a experiência de uso. As heurísticas de teste guiarão as sessões exploratórias para gerar descobertas além dos requisitos documentados.

