# ✅ **Definition of Ready (DoR)**

> **Quando uma tarefa/funcionalidade está pronta para ser iniciada pelo time de QA.**

| Critério                          | Descrição                                                                                                                  |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| 🎯 Objetivo definido              | O escopo e objetivo do teste estão claramente definidos (ex: testar funcionalidades do front-end do PrestaShop Demo).      |
| 📄 Requisitos acessíveis          | Requisitos funcionais e não funcionais disponíveis (ou serão levantados durante o teste exploratório).                     |
| 🔗 Ambiente de teste disponível   | Ambiente de testes acessível e funcional: [https://demo.prestashop.com/#/en/front](https://demo.prestashop.com/#/en/front) |
| 👥 Responsável definido           | Responsável pela execução do teste está designado (ex: Miguel Luis - QA).                                                  |
| 🛠 Ferramentas definidas          | Ferramentas de apoio e documentação estabelecidas (Ex: navegador Edge, editor Markdown, vídeo ou print para evidência).    |
| ⏱ Tempo estimado                  | Estimativa de tempo para realização do teste definida.                                                                     |
| 💬 Critérios de aceite combinados | Critérios que definem sucesso para essa entrega foram validados com o time.                                                |

---

# 🏁 **Definition of Done (DoD)**

> **Quando consideramos o mini projeto finalizado e pronto para ser entregue/documentado.**

| Critério                        | Descrição                                                                                           |
| ------------------------------- | --------------------------------------------------------------------------------------------------- |
| 🔍 Teste exploratório executado | Teste foi realizado em diferentes áreas do site, cobrindo funcionalidades principais.               |
| 🧪 Funcionalidades mapeadas     | Funcionalidades foram listadas e categorizadas como funcionais ou com falhas.                       |
| 🐞 Bugs documentados            | Erros encontrados foram descritos com passos, evidência, severidade e comportamento esperado.       |
| 📋 Análise de requisitos feita  | Requisitos funcionais e de usabilidade foram mapeados com base no comportamento observado.          |
| 📁 Documentação gerada          | README.md com documentação do teste exploratório foi criado com: URL, data, observações, sugestões. |
| 📌 Conclusão escrita            | Resultado geral do teste, sugestões de melhoria e próximos passos foram registrados.                |
| 🔁 Revisado e validado          | Documento foi revisado para clareza e completude antes de entrega/publicação.                       |

# 🎯 Priorização dos Testes Manuais – PHPTRAVELS.NET

Esta priorização orienta a **ordem de execução** dos testes manuais com base nos **requisitos funcionais** e **regras de negócio** analisados na plataforma de demonstração [phptravels.net](https://phptravels.net).

---

## 🧠 Critérios de Priorização

| Nível     | Definição                                                                 |
|-----------|---------------------------------------------------------------------------|
| 🔴 Alta   | Funcionalidade crítica, usada com frequência ou que impacta o negócio.    |
| 🟡 Média  | Funcionalidade importante, mas não bloqueadora.                           |
| 🟢 Baixa  | Funcionalidade complementar, com pouco impacto se falhar.                |

---

## 🔴 PRIORIDADE ALTA

Esses testes devem ser executados **primeiro**, pois validam fluxos essenciais, bloqueadores e regras críticas.

| ID         | Item a ser testado                                       | Requisitos / Regras Relacionadas |
|------------|-----------------------------------------------------------|----------------------------------|
| TST-001    | Busca de hotéis com todos os campos obrigatórios          | RF-01.3, RN-BUSCA-01, RN-BUSCA-02, RN-BUSCA-05, RN-BUSCA-08 |
| TST-002    | Cadastro com e-mail único e senha válida                  | RF-02.2, RN-CONTA-01, RN-CONTA-02, RN-CONTA-03 |
| TST-003    | Login com credenciais válidas e inválidas                 | RF-02.1 |
| TST-004    | Fluxo completo de reserva de hotel                        | RF-05, RN-RESERVA-01 a 07 |
| TST-005    | Alteração de moeda e verificação da persistência          | RF-06.2, RN-GL-01 |
| TST-006    | Alteração de idioma e verificação da interface            | RF-06.1, RN-GL-02 |
| TST-007    | Validação de campos obrigatórios nos formulários de busca| RN-BUSCA-08 |
| TST-008    | Confirmação de reserva com e sem aceite de termos         | RF-05.5, RN-RESERVA-04 |
| TST-009    | Acesso ao painel do cliente (autenticado vs não autenticado) | RF-02.3, RN-GL-03 |
| TST-010    | Visualização da reserva em "Bookings" após finalização    | RF-02.3, RF-05.9, RN-RESERVA-05 |

---

## 🟡 PRIORIDADE MÉDIA

Esses testes devem ser realizados após os de alta prioridade. Impactam a experiência do usuário, mas não bloqueiam o uso do sistema em geral.

| ID         | Item a ser testado                                       | Requisitos / Regras Relacionadas |
|------------|-----------------------------------------------------------|----------------------------------|
| TST-011    | Busca de voos com validações de datas e locais            | RF-01.4, RN-BUSCA-01, RN-BUSCA-03, RN-BUSCA-06 |
| TST-012    | Busca de carros com validação de datas e horários         | RF-01.6, RN-BUSCA-04 |
| TST-013    | Visualização de resultados com filtros e ordenação        | RF-03.2 a RF-03.4 |
| TST-014    | Página de detalhes de hotel com galeria e avaliações      | RF-04.1 e RF-04.2 |
| TST-015    | Persistência dos dados do perfil após edição              | RF-02.3, RN-CONTA-05 |
| TST-016    | Geração e visualização da fatura de reserva               | RN-RESERVA-06 |
| TST-017    | Simulação de pagamento sem transação real                 | RF-05.4, RN-RESERVA-07 |
| TST-018    | Troca de idioma com conteúdo dinâmico                     | RN-GL-02 |
| TST-019    | Teste de logout e redirecionamento correto                | RF-02.3 |
| TST-020    | Tentativa de login com senha incorreta                    | RF-02.1 |

---

## 🟢 PRIORIDADE BAIXA

Esses testes validam aspectos complementares, comportamentos alternativos e consistência visual.

| ID         | Item a ser testado                                       | Requisitos / Regras Relacionadas |
|------------|-----------------------------------------------------------|----------------------------------|
| TST-021    | Validação visual de mensagens de erro em formulários     | RNF-01.2 |
| TST-022    | Verificação de hover e feedbacks visuais nos botões      | RNF-01.3 |
| TST-023    | Responsividade em diferentes dispositivos (mobile/tablet)| RNF-02.2 |
| TST-024    | Navegação pelo cabeçalho e rodapé                         | RF-06.3 |
| TST-025    | Página de resultados com "No results found"              | RF-03.6 |
| TST-026    | Alternância entre visualização em lista e em grade       | RF-03.5 |
| TST-027    | Busca por passeios com validação de data e quantidade    | RF-01.5, RN-BUSCA-05 |
| TST-028    | Busca por visto com países diferentes                    | RF-01.7, RN-BUSCA-07 |

---

## ✅ Observações

- A execução dos testes deve seguir esta ordem de prioridade em ciclos curtos (ex: sprints ou sessões).
- Bugs encontrados nos testes de prioridade **Alta** devem ser tratados com **urgência**, pois bloqueiam fluxos principais.
- Testes de **baixa prioridade** podem ser agendados para ciclos posteriores ou automatizados futuramente.

---

🎯 *"Testar o que mais impacta primeiro é a base da eficiência em QA manual."*

