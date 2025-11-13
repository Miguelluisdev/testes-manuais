## 🧩 O que é a ISO/IEC 25010

A **ISO/IEC 25010:2011** (parte da série **SQuaRE — *System and Software Quality Requirements and Evaluation***), substituiu a antiga **ISO/IEC 9126** e define dois modelos principais:

1. **Modelo de Qualidade de Produto de Software**
2. **Modelo de Qualidade em Uso**

Esses modelos servem como **base para definir, avaliar e validar** a qualidade de um produto de software em diferentes níveis — desde a perspectiva técnica até a experiência do usuário.

---

## 🧠 1. Modelo de Qualidade do Produto (8 características)

Esse modelo analisa o software em si — seu código, arquitetura, funcionamento e comportamento.

### 🔹 1. Funcionalidade (*Functional Suitability*)

Avalia se o sistema **atende às funções esperadas** e cumpre os requisitos.

* **Completude funcional:** o software faz tudo o que precisa?
* **Correção funcional:** faz da forma correta?
* **Apropriabilidade funcional:** faz sentido para o usuário?

🧪 *Exemplo:* Verificar se o módulo de login realmente autentica usuários válidos e bloqueia acessos indevidos.

---

### 🔹 2. Eficiência de Desempenho (*Performance Efficiency*)

Avalia **tempo de resposta, consumo de recursos e capacidade**.

* **Tempo de resposta**
* **Utilização de recursos (CPU, memória, rede)**
* **Capacidade sob carga**

🧪 *Exemplo:* O sistema suporta 500 usuários simultâneos sem travar?

---

### 🔹 3. Compatibilidade (*Compatibility*)

Mede se o software **funciona bem em diferentes ambientes** e **coexiste com outros sistemas**.

* **Coexistência:** não interfere em outros sistemas.
* **Interoperabilidade:** troca dados corretamente com outros sistemas.

🧪 *Exemplo:* O sistema exporta dados corretamente para o ERP da empresa?

---

### 🔹 4. Usabilidade (*Usability*)

Analisa se o sistema é **fácil de aprender, entender e usar**.

* **Reconhecibilidade da adequação**
* **Aprendibilidade**
* **Operabilidade**
* **Proteção contra erros**
* **Acessibilidade**

🧪 *Exemplo:* Um novo usuário consegue entender facilmente como cadastrar um produto?

---

### 🔹 5. Confiabilidade (*Reliability*)

Avalia se o sistema **mantém seu desempenho sob condições específicas**.

* **Maturidade:** frequência de falhas
* **Disponibilidade**
* **Tolerância a falhas**
* **Recuperabilidade**

🧪 *Exemplo:* O sistema continua funcional após uma queda momentânea de rede?

---

### 🔹 6. Segurança (*Security*)

Verifica se o sistema **protege informações e dados** contra acesso não autorizado.

* **Confidencialidade**
* **Integridade**
* **Não-repúdio**
* **Autenticidade**
* **Responsabilização**

🧪 *Exemplo:* Dados pessoais estão criptografados? Há controle de permissões?

---

### 🔹 7. Manutenibilidade (*Maintainability*)

Avalia o **quanto é fácil modificar, corrigir e evoluir o sistema**.

* **Modularidade**
* **Reusabilidade**
* **Analisabilidade**
* **Modificabilidade**
* **Testabilidade**

🧪 *Exemplo:* Um QA consegue testar alterações sem precisar reexecutar todo o sistema?

---

### 🔹 8. Portabilidade (*Portability*)

Mede a **facilidade de o software ser transferido entre ambientes**.

* **Adaptabilidade**
* **Instalabilidade**
* **Substituibilidade**

🧪 *Exemplo:* O sistema funciona tanto no Windows quanto no Linux?

---

## 🌍 2. Modelo de Qualidade em Uso (5 características)

Esse modelo analisa **a experiência do usuário final** e o impacto do software em seu trabalho.

### 🔹 1. Eficácia

O usuário **consegue atingir seus objetivos** corretamente?

### 🔹 2. Eficiência

O usuário **atinge os objetivos com esforço mínimo** (tempo, cliques, navegação).

### 🔹 3. Satisfação

O usuário **fica satisfeito com o uso do sistema**? É agradável e confiável?

### 🔹 4. Liberdade de Riscos

O software **reduz riscos para o usuário e seus dados** (falhas, segurança, saúde etc).

### 🔹 5. Cobertura do Contexto

O sistema **funciona bem em diferentes contextos de uso**, dispositivos e situações.

---

## 🧩 Relação com QA e Testes

A **ISO 25010 serve como base para o QA planejar testes e critérios de aceitação.**
Ela ajuda o time de QA a **ir além do “funciona ou não funciona”**, avaliando a **qualidade completa** do produto.

📋 **Como o QA aplica na prática:**

* Ao criar **casos de teste de performance, segurança e usabilidade**
* Ao fazer **testes de regressão e manutenção**
* Ao validar **interoperabilidade e compatibilidade de versões**
* Ao **definir métricas de qualidade** (ex: tempo de resposta, taxa de erro, cobertura de código)
* Ao **relatar bugs classificados por impacto em uma característica da norma**

---

## 💡 Exemplo prático

> **Requisito:** “O sistema deve permitir o cadastro de novos clientes.”
>
> QA aplica a ISO 25010 para validar:
>
> * Funcionalidade: o cadastro realmente salva dados válidos?
> * Usabilidade: o formulário é claro e fácil de preencher?
> * Segurança: há proteção contra SQL Injection?
> * Manutenibilidade: é fácil testar e atualizar o módulo?
> * Eficiência: o cadastro responde rapidamente?

---

## 📘 Conclusão

A **ISO/IEC 25010** é uma **base conceitual para toda a garantia da qualidade**.
Ela **não diz “como testar”**, mas define **o que significa qualidade de software**, permitindo que QA, desenvolvedores e gestores falem a mesma língua.
