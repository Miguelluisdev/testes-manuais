### 🧩 **Contexto dentro da série ISO/IEC/IEEE 29119**

A **Parte 5 – Keyword-Driven Testing (KDT)** é uma extensão prática da família 29119, que:

* **Complementa a Parte 2 (Processos de Teste)** → adicionando uma forma estruturada e automatizável de escrever casos de teste;
* **Apoia a Parte 4 (Técnicas de Teste)** → permitindo que técnicas como *particionamento de equivalência* ou *valor limite* sejam expressas em formato de palavras-chave reutilizáveis.

---

### ⚙️ **Essência da ISO/IEC/IEEE 29119-5**

O objetivo central é **padronizar a automação baseada em palavras-chave**, garantindo **reutilização, clareza e interoperabilidade** entre ferramentas.

| Conceito                       | Descrição                                                                                                                                                 |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Keyword (Palavra-chave)**    | Representa uma ação ou operação (ex: “Login”, “Adicionar Produto”, “Validar Mensagem”).                                                                   |
| **Test Step (Passo de teste)** | Uma sequência de palavras-chave que descreve o fluxo de um caso de teste.                                                                                 |
| **Data-Driven Layer**          | Complementa as palavras-chave com dados variáveis, permitindo reuso.                                                                                      |
| **Framework KDT**              | Estrutura que contém o executor de palavras-chave, bibliotecas, e interface de integração com ferramentas (como Cypress, Robot Framework, Selenium, etc). |
| **Interoperabilidade**         | Define como ferramentas diferentes podem compartilhar palavras-chave e scripts de automação.                                                              |

---

### 🧠 **Por que ela é importante para o QA moderno**

1. **Abstração e Reutilização:**
   Permite separar a lógica do teste da sua implementação técnica. Assim, um analista pode criar cenários automatizados sem escrever código complexo.

2. **Facilita a colaboração:**
   Testadores manuais, analistas e engenheiros de automação conseguem trabalhar juntos num formato comum (palavras-chave).

3. **Reduz manutenção:**
   Mudou a interface? Só atualiza a palavra-chave base — todos os testes que a usam continuam válidos.

4. **Padroniza a automação:**
   A norma define boas práticas para a criação, nomeação e manutenção de palavras-chave, evitando caos em projetos grandes.

---

### 💡 **Ligação prática com ferramentas atuais**

Mesmo que poucas equipes sigam formalmente a 29119-5, ela **inspirou frameworks modernos**:

* **Robot Framework** → segue o padrão de palavras-chave quase literalmente;
* **Cypress + Custom Commands** → cada comando pode ser visto como uma palavra-chave reutilizável;
* **Selenium + Cucumber (Gherkin)** → os *steps* em linguagem natural funcionam como “palavras-chave semânticas”;
* **Playwright Test + Fixtures** → estrutura modular e reutilizável que reflete o mesmo princípio.

---

### 📘 **Resumo rápido da Parte 5**

| Elemento                | Descrição                                                                  |
| ----------------------- | -------------------------------------------------------------------------- |
| **Nome**                | ISO/IEC/IEEE 29119-5: Keyword-Driven Testing                               |
| **Escopo**              | Padronizar como projetar e manter automação orientada a palavras-chave     |
| **Foco**                | Modularidade, abstração, reutilização e interoperabilidade                 |
| **Público-alvo**        | Engenheiros de automação, analistas de teste e líderes técnicos            |
| **Benefício principal** | Facilita automação sustentável e acessível para equipes multidisciplinares |
