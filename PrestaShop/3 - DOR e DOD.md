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

## 📊 Tabela de Priorização de Módulos para Teste

### 🔍 Testes Funcionais

| Nº | Módulo/Funcionalidade             | Prioridade  | Justificativa                                                                 |
|----|-----------------------------------|-------------|-------------------------------------------------------------------------------|
| 1  | Processo de Checkout              | ALTÍSSIMA   | Crítico para o negócio. Falhas resultam em perda de vendas diretas.         |
| 2  | Carrinho de Compras               | ALTÍSSIMA   | Precede o checkout. Erros impedem o avanço da compra.                       |
| 3  | Página de Detalhes do Produto     | ALTA        | Decisão de compra ocorre aqui. Falhas afetam diretamente as vendas.        |
| 4  | Busca de Produto                  | ALTA        | Principal método de encontrar produtos. Sem ela, o usuário não encontra.    |
| 5  | Listagem de Produtos (PLP)        | ALTA        | Navegação e visualização por categorias. Filtros e ordenação são cruciais.  |
| 6  | Login/Cadastro                    | ALTA        | Essencial para histórico e dados, mas há alternativa via guest checkout.    |
| 7  | Gerenciamento de Conta de Usuário | MÉDIA       | Importante para alterações e pedidos, mas não impede compras iniciais.      |

### 🛡️ Testes Não Funcionais

| Nº | Módulo/Funcionalidade  | Prioridade  | Justificativa                                                                 |
|----|------------------------|-------------|-------------------------------------------------------------------------------|
| 1  | Usabilidade            | ALTÍSSIMA   | Site deve ser intuitivo e responsivo. Caso contrário, a taxa de abandono é alta. |
| 2  | Performance (Manual)   | ALTA        | Lentidão compromete experiência e conversão.                                 |
| 3  | Segurança (Manual)     | ALTA        | Essencial para gerar confiança: HTTPS, dados sensíveis, etc.                |
| 4  | Acessibilidade (Básica com DevTools) | MÉDIA | Inclusão e boas práticas: uso de tags semânticas e atributos básicos.        |
