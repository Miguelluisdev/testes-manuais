## 🧩 TESTES BASEADOS NA ISO/IEC 25010

### 1️⃣ Funcionalidade (*Functional Suitability*)

Avalia se o software **realiza corretamente o que foi especificado**.

**Objetivo:** garantir que as funções atendem aos requisitos.
**Testes típicos:**

* Testes funcionais (Happy Path, Negativo, Valor Limite)
* Testes de integração
* Testes ponta a ponta (E2E)

**Exemplo:**

> Validar que o sistema permite login apenas com credenciais válidas e bloqueia após 3 tentativas inválidas.

**Evidência esperada:**
✅ Todos os fluxos funcionais implementados e operando conforme os requisitos.

---

### 2️⃣ Eficiência de Desempenho (*Performance Efficiency*)

Avalia **tempo de resposta, consumo de recursos e capacidade sob carga.**

**Objetivo:** garantir que o sistema é rápido e escalável.
**Testes típicos:**

* Teste de desempenho (response time)
* Teste de carga (load test)
* Teste de stress
* Teste de volume

**Ferramentas:** JMeter, Gatling, k6

**Exemplo:**

> Verificar se o sistema responde em até 2s com 100 usuários simultâneos.

**Evidência esperada:**
✅ Tempo de resposta dentro dos limites estabelecidos.

---

### 3️⃣ Compatibilidade (*Compatibility*)

Verifica se o software **funciona em diferentes ambientes, sistemas e navegadores.**

**Objetivo:** garantir interoperabilidade e coexistência.
**Testes típicos:**

* Testes cross-browser (Chrome, Firefox, Edge, Safari)
* Testes cross-device (desktop, tablet, mobile)
* Testes de integração com sistemas externos (APIs, ERPs, etc.)

**Ferramentas:** BrowserStack, LambdaTest, Postman, Newman

**Exemplo:**

> Validar se o e-commerce funciona corretamente em Windows, Android e iOS.

**Evidência esperada:**
✅ Layouts e funcionalidades consistentes em todos os ambientes.

---

### 4️⃣ Usabilidade (*Usability*)

Avalia se o sistema é **fácil de usar, entender e aprender.**

**Objetivo:** garantir uma boa experiência de uso.
**Testes típicos:**

* Teste de UX (fluxos e usabilidade geral)
* Teste de acessibilidade (WCAG)
* Teste de aprendizado (novos usuários)
* Heuristic evaluation (avaliação por especialistas)

**Ferramentas:** Axe, Lighthouse, NVDA, WAVE

**Exemplo:**

> Avaliar se o processo de cadastro é intuitivo e sem erros de preenchimento.

**Evidência esperada:**
✅ Usuário executa tarefas com facilidade, sem confusão ou erros desnecessários.

---

### 5️⃣ Confiabilidade (*Reliability*)

Mede se o software **mantém funcionamento estável em diferentes condições.**

**Objetivo:** garantir estabilidade, tolerância a falhas e recuperação.
**Testes típicos:**

* Teste de estabilidade (long-run test)
* Teste de recuperação (reconexão após falha)
* Teste de falhas controladas (failover test)

**Exemplo:**

> Desconectar a rede durante o uso e verificar se o sistema se recupera sem perda de dados.

**Evidência esperada:**
✅ O sistema continua funcional ou se recupera de forma segura.

---

### 6️⃣ Segurança (*Security*)

Avalia se o software **protege dados e impede acessos indevidos.**

**Objetivo:** garantir integridade, confidencialidade e autenticidade.
**Testes típicos:**

* Teste de autenticação e autorização
* Teste de vulnerabilidades (SQL Injection, XSS, CSRF)
* Teste de senhas e tokens
* Teste de logs e auditoria

**Ferramentas:** OWASP ZAP, Burp Suite, Postman

**Exemplo:**

> Verificar se campos de login não aceitam scripts e se os dados trafegam criptografados (HTTPS).

**Evidência esperada:**
✅ Dados protegidos, acessos controlados e sem vulnerabilidades conhecidas.

---

### 7️⃣ Manutenibilidade (*Maintainability*)

Analisa se o sistema é **fácil de corrigir, atualizar e testar.**

**Objetivo:** reduzir esforço de manutenção e risco de regressões.
**Testes típicos:**

* Testes de regressão automatizados
* Análise de cobertura de testes
* Revisão de código e análise estática
* Teste de impacto (mudança de versão)

**Ferramentas:** SonarQube, Cypress, Jest, Playwright

**Exemplo:**

> Rodar testes automatizados após alteração de código e validar se não houve regressões.

**Evidência esperada:**
✅ O sistema continua funcional após mudanças.

---

### 8️⃣ Portabilidade (*Portability*)

Verifica se o software **pode ser instalado, adaptado e utilizado em outros ambientes.**

**Objetivo:** facilitar migração e reutilização.
**Testes típicos:**

* Teste de instalação/desinstalação
* Teste de compatibilidade de versão
* Teste de execução em diferentes sistemas operacionais

**Exemplo:**

> Validar se o aplicativo mobile instala corretamente em Android e iOS.

**Evidência esperada:**
✅ Sistema roda e mantém consistência em múltiplas plataformas.

---

## 🌍 QUALIDADE EM USO — testando a experiência real

| Atributo                  | O que medir                                | Como testar                                        |
| ------------------------- | ------------------------------------------ | -------------------------------------------------- |
| **Eficácia**              | O usuário consegue atingir seus objetivos? | Testes de tarefas reais (ex: completar uma compra) |
| **Eficiência**            | O usuário gasta pouco tempo/esforço?       | Medir tempo médio de execução de tarefas           |
| **Satisfação**            | O usuário gosta da experiência?            | Pesquisa de feedback e testes A/B                  |
| **Liberdade de riscos**   | Há falhas ou danos?                        | Testes de segurança, perda de dados                |
| **Cobertura do contexto** | Funciona em todos os contextos reais?      | Testes em diferentes cenários de uso               |

---

## 💡 COMO IMPLEMENTAR NO PROCESSO DE QA

1. **Planejamento:** mapear quais características ISO 25010 são mais críticas para o projeto.
2. **Casos de teste:** incluir colunas no plano de testes indicando a característica ISO associada.
3. **Execução:** executar testes cobrindo as dimensões de qualidade.
4. **Relatórios:** classificar os bugs segundo as características (ex: “Falha de usabilidade” ou “Falha de segurança”).
5. **Métricas:** medir desempenho, taxa de falhas, cobertura e satisfação.

---

## 🎯 Em resumo

> **Testar com base na ISO/IEC 25010 é testar com propósito.**

Ela transforma o QA de um simples executor de testes em um **avaliador completo da qualidade do produto** — técnico, funcional e humano.
