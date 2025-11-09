# 🧩 Testes de Privacidade e Conformidade com a LGPD

## 🧾 Objetivo

Garantir que o sistema **PHPTravels** ([https://phptravels.net/](https://phptravels.net/)) esteja em conformidade com os princípios e exigências da **LGPD (Lei Geral de Proteção de Dados – Lei nº 13.709/2018)**, assegurando que os **dados pessoais** dos usuários sejam coletados, tratados e armazenados de forma **segura, legítima e transparente**.

---

## ⚙️ Escopo

Estes testes cobrem:

* Coleta, consentimento e finalidade de uso de dados pessoais
* Direito à informação, portabilidade e exclusão
* Segurança, armazenamento e tratamento de dados sensíveis
* Gerenciamento de cookies e sessões
* Transparência na política de privacidade

---

## 🧪 Casos de Teste Detalhados

### **CT-LGPD-01 – Exibição da Política de Privacidade**

**Descrição:** Verificar se o site possui política de privacidade acessível, clara e atualizada.
**Pré-condição:** Usuário acessa o site principal.
**Passos:**

1. Acessar a página inicial.
2. Rolar até o rodapé.
3. Localizar o link “Privacy Policy” ou equivalente.
4. Clicar e verificar o conteúdo exibido.
   **Critério de Aceitação:**

* A política deve estar visível e facilmente acessível.
* Deve explicar como os dados são coletados e utilizados.
* Deve citar conformidade com a LGPD.
  **Risco e Impacto:**
  🔴 *Alta gravidade*: ausência de política clara pode gerar **multas da ANPD**, **perda de credibilidade** e **não conformidade legal**.

---

### **CT-LGPD-02 – Consentimento de Coleta de Dados**

**Descrição:** Verificar se o site solicita consentimento antes de coletar dados (cookies, formulários, rastreamento).
**Pré-condição:** Primeira visita ao site (sem cookies salvos).
**Passos:**

1. Limpar cookies do navegador.
2. Acessar o site.
3. Verificar se aparece banner ou modal de consentimento.
4. Testar opções “Aceitar” e “Recusar”.
   **Critério de Aceitação:**

* O sistema deve pedir consentimento explícito antes da coleta.
* Deve permitir recusa sem bloquear o uso básico do site.
  **Risco e Impacto:**
  🔴 *Alta gravidade*: coleta de dados sem consentimento pode causar **multas de até 2% do faturamento** e **violação direta da LGPD**.

---

### **CT-LGPD-03 – Transparência na Coleta de Dados**

**Descrição:** Verificar se os formulários informam claramente a finalidade do uso dos dados.
**Pré-condição:** Página de cadastro ou contato disponível.
**Passos:**

1. Acessar o formulário de cadastro.
2. Verificar textos explicativos sobre uso dos dados.
   **Critério de Aceitação:**

* O formulário deve informar a finalidade (ex: “Seu e-mail será usado para envio de confirmação”).
  **Risco e Impacto:**
  🟠 *Média*: ausência de transparência compromete a **confiança do usuário** e caracteriza **tratamento indevido de dados**.

---

### **CT-LGPD-04 – Direito de Acesso e Portabilidade**

**Descrição:** Verificar se o usuário pode visualizar ou exportar seus dados pessoais.
**Pré-condição:** Usuário logado e com dados cadastrados.
**Passos:**

1. Acessar configurações da conta.
2. Procurar opção “Meus dados” ou “Exportar informações”.
   **Critério de Aceitação:**

* O sistema deve permitir visualizar ou exportar dados pessoais.
  **Risco e Impacto:**
  🟠 *Média*: impossibilidade de acesso viola o **art. 18 da LGPD** e prejudica o **direito do titular**.

---

### **CT-LGPD-05 – Direito à Exclusão (Opt-out)**

**Descrição:** Verificar se o usuário pode excluir sua conta e apagar dados pessoais.
**Pré-condição:** Conta ativa e logada.
**Passos:**

1. Acessar o perfil.
2. Buscar opção “Excluir conta”.
3. Confirmar exclusão e verificar resultado.
   **Critério de Aceitação:**

* Sistema deve excluir permanentemente os dados pessoais.
* Mensagem de confirmação deve ser exibida.
  **Risco e Impacto:**
  🔴 *Alta gravidade*: retenção indevida após solicitação de exclusão é **infração grave** sujeita a **sanções legais**.

---

### **CT-LGPD-06 – Proteção de Dados Sensíveis**

**Descrição:** Verificar se dados sensíveis (senha, CPF, cartão) são protegidos e não expostos.
**Pré-condição:** Usuário envia dados pessoais em formulário.
**Passos:**

1. Analisar requisições de rede no navegador.
2. Verificar se tráfego é HTTPS.
3. Confirmar se senhas são mascaradas e não aparecem em logs/URLs.
   **Critério de Aceitação:**

* Dados sensíveis devem trafegar criptografados.
* Senhas nunca devem aparecer em texto simples.
  **Risco e Impacto:**
  🔴 *Alta gravidade*: exposição de dados pode gerar **vazamento**, **danos à imagem** e **responsabilidade civil**.

---

### **CT-LGPD-07 – Revogação de Consentimento**

**Descrição:** Verificar se o usuário pode revogar consentimento já concedido.
**Pré-condição:** Consentimento ativo.
**Passos:**

1. Acessar painel de privacidade.
2. Selecionar opção “Revogar consentimento”.
3. Confirmar revogação.
   **Critério de Aceitação:**

* Sistema deve permitir revogação simples e eficaz.
  **Risco e Impacto:**
  🟠 *Média*: ausência de revogação pode resultar em **tratamento indevido** e **reclamações formais** à ANPD.

---

### **CT-LGPD-08 – Retenção e Exclusão de Logs**

**Descrição:** Verificar se há política de retenção e exclusão de logs de usuários.
**Pré-condição:** Política de privacidade publicada.
**Passos:**

1. Consultar política de privacidade.
2. Identificar período de retenção e procedimento de exclusão.
   **Critério de Aceitação:**

* Logs devem ter prazo máximo de retenção informado.
  **Risco e Impacto:**
  🟡 *Baixa*: ausência de informação reduz **transparência**, mas não afeta diretamente a segurança.

---

### **CT-LGPD-09 – Consentimento para Cookies de Terceiros**

**Descrição:** Verificar se o site informa e solicita consentimento antes de usar cookies de terceiros (Google, Meta, etc.).
**Pré-condição:** Primeira visita ao site.
**Passos:**

1. Limpar cookies.
2. Acessar o site e inspecionar cookies criados.
3. Verificar se cookies de terceiros são ativados sem consentimento.
   **Critério de Aceitação:**

* Cookies externos só devem ser ativados após consentimento.
  **Risco e Impacto:**
  🔴 *Alta gravidade*: ativação automática sem aviso viola **LGPD e GDPR**, podendo gerar **multa imediata**.

---

### **CT-LGPD-10 – Segurança de Sessão**

**Descrição:** Garantir que sessões de usuários expirem após período de inatividade.
**Pré-condição:** Usuário logado.
**Passos:**

1. Fazer login.
2. Permanecer inativo por 15–30 minutos.
3. Verificar se a sessão expira automaticamente.
   **Critério de Aceitação:**

* Sessão deve encerrar e exigir novo login.
  **Risco e Impacto:**
  🟠 *Média*: sessão ilimitada expõe risco de **uso indevido de conta** ou **sequestro de sessão**.

---

## 🧭 Priorização dos Testes

| ID         | Prioridade | Gravidade | Risco/Impacto                                |
| ---------- | ---------- | --------- | -------------------------------------------- |
| CT-LGPD-01 | Alta       | Alta      | Falta de política → não conformidade legal   |
| CT-LGPD-02 | Alta       | Alta      | Coleta sem consentimento → multa e bloqueio  |
| CT-LGPD-03 | Alta       | Média     | Falta de transparência → tratamento indevido |
| CT-LGPD-04 | Média      | Média     | Impede direito do titular                    |
| CT-LGPD-05 | Alta       | Alta      | Retenção indevida → infração grave           |
| CT-LGPD-06 | Alta       | Alta      | Vazamento → dano à imagem e sanções          |
| CT-LGPD-07 | Média      | Média     | Revogação ausente → uso indevido             |
| CT-LGPD-08 | Baixa      | Baixa     | Falta de retenção → perda de transparência   |
| CT-LGPD-09 | Alta       | Alta      | Cookies sem consentimento → infração direta  |
| CT-LGPD-10 | Média      | Média     | Sessão aberta → risco de sequestro           |
