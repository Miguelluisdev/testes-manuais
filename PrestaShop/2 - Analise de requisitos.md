# Análise de Requisitos para Testes Manuais de QA - PrestaShop Demo Front-End

**Site Alvo:** [https://demo.prestashop.com/#/en/front](https://demo.prestashop.com/#/en/front)

## Objetivo da Análise

Identificar os requisitos funcionais e não funcionais do front-end do site demo do PrestaShop para embasar a criação de casos de teste manuais de Garantia de Qualidade (QA). A análise visa cobrir:

1.  **O que** o sistema deve fazer (requisitos funcionais).
2.  **Como** o sistema deve se comportar em termos de usabilidade, performance, etc. (requisitos não funcionais).
3.  **Quais dados** são manipulados.

---

## 1. Requisitos Gerais e de Navegação (Interface do Usuário - UI)

### **R1.1 - Consistência Visual**
O site deve apresentar um design consistente em todas as páginas (cores, fontes, espaçamento, ícones).

### **R1.2 - Responsividade**
O layout do site deve se adaptar corretamente a diferentes tamanhos de tela (desktop, tablet, mobile).

### **R1.3 - Navegação Principal**
- O menu principal deve ser claramente visível e funcional.
- Links do menu devem redirecionar para as seções corretas.
- Submenus (dropdowns) devem aparecer ao passar o mouse (ou clicar, dependendo do design) e seus links devem ser funcionais.

### **R1.4 - Logotipo**
O logotipo da loja deve ser clicável e redirecionar para a página inicial.

### **R1.5 - Rodapé (Footer)**
- Deve conter links úteis (Informações, Minha Conta, Contato, etc.).
- Links do rodapé devem ser funcionais.
- Informações de copyright e redes sociais (se houver) devem estar corretas e funcionais.

### **R1.6 - Breadcrumbs (Migalhas de Pão)**
Devem indicar corretamente a localização do usuário dentro da hierarquia do site e permitir navegação para níveis anteriores.

### **R1.7 - Internacionalização (`i18n`) e Localização (`l10n`)**
- **R1.7.1 - Seletor de Idioma:** Deve permitir ao usuário trocar o idioma do site. A troca deve refletir em todo o conteúdo textual da interface.
- **R1.7.2 - Seletor de Moeda:** Deve permitir ao usuário trocar a moeda. A troca deve refletir nos preços dos produtos, carrinho e checkout.

### **R1.8 - Mensagens de Erro e Sucesso**
Devem ser claras, informativas e contextuais.

### **R1.9 - Ícones**
Ícones utilizados devem ser intuitivos e consistentes.

---

## 2. Página Inicial (Homepage)

### **R2.1 - Carregamento**
A página inicial deve carregar dentro de um tempo aceitável.

### **R2.2 - Banners Promocionais/Slideshow**
- Devem ser exibidos corretamente.
- Se forem clicáveis, devem redirecionar para a página/produto correto.
- Controles de navegação do slideshow (se houver) devem funcionar.

### **R2.3 - Seções de Produtos**
- Produtos em destaque (`Featured Products`), novos produtos (`New Products`), mais vendidos (`Best Sellers`) devem ser exibidos corretamente.
- Links dos produtos ("Ver Produto", imagem, nome) devem levar à Página de Detalhes do Produto (`PDP`).
- Botão "Adicionar ao Carrinho" (se presente na homepage) deve funcionar.

### **R2.4 - Blocos de Conteúdo Customizado**
(Ex: "Custom Text Block") Devem exibir o conteúdo esperado.

### **R2.5 - Inscrição em Newsletter**
- Campo para inserção de e-mail deve aceitar formatos válidos.
- Validação para e-mails inválidos.
- Mensagem de sucesso após inscrição.
- Prevenção contra múltiplas inscrições com o mesmo e-mail (se aplicável).

---

## 3. Busca de Produtos

### **R3.1 - Campo de Busca**
Deve estar visível (geralmente no cabeçalho).

### **R3.2 - Funcionalidade de Busca**
- Resultados relevantes devem ser exibidos ao buscar por nome do produto, `SKU` (se visível), ou palavras-chave da descrição.
- Busca com termos parciais deve funcionar.
- Busca por termos inexistentes deve retornar uma mensagem "Nenhum resultado encontrado" amigável.
- A página de resultados da busca deve ser paginada se houver muitos resultados.
- Opções de ordenação e filtro na página de resultados da busca (se disponíveis).

### **R3.3 - Sugestões de Busca (Autocomplete)**
Se implementado, deve sugerir produtos à medida que o usuário digita.

---

## 4. Listagem de Produtos (PLP - Product Listing Page) / Páginas de Categoria

### **R4.1 - Exibição de Produtos**
- A lista de produtos da categoria selecionada deve ser exibida corretamente (imagem, nome, preço).
- Paginação deve funcionar corretamente (navegar entre páginas, exibir número correto de itens por página).

### **R4.2 - Filtros**
- Filtros disponíveis (por preço, marca, atributos como cor, tamanho, etc.) devem funcionar individualmente e combinados.
- A lista de produtos deve ser atualizada dinamicamente (ou após clicar em "Aplicar") conforme os filtros são selecionados/removidos.
- Opção de limpar/resetar filtros.

### **R4.3 - Ordenação**
- Opções de ordenação (por preço crescente/decrescente, nome, relevância, mais recentes) devem funcionar e atualizar a lista de produtos.

### **R4.4 - Visualização (Grid/List)**
Se houver opção de alternar entre visualização em grade e lista, deve funcionar.

### **R4.5 - Botão "Adicionar ao Carrinho" (Quick Add)**
Se presente na `PLP`, deve adicionar o produto ao carrinho (para produtos simples, sem variações obrigatórias).

### **R4.6 - Indicador de Estoque/Promoção**
Informações como "Em estoque", "Fora de estoque", "Promoção" devem ser visíveis e corretas.

---

## 5. Página de Detalhes do Produto (PDP - Product Detail Page)

### **R5.1 - Informações do Produto**
- Nome do produto, descrição curta e longa, preço, `SKU` (se visível), marca devem ser exibidos corretamente.
- Imagens do produto: galeria de imagens, zoom na imagem principal, miniaturas clicáveis.

### **R5.2 - Variações do Produto (se aplicável)**
- Seletores de variações (cor, tamanho, etc.) devem estar funcionais.
- A seleção de uma variação pode atualizar a imagem do produto, preço e disponibilidade de estoque.

### **R5.3 - Preço**
- Preço original e preço com desconto (se em promoção) devem ser exibidos corretamente.
- Cálculo do percentual de desconto (se exibido).

### **R5.4 - Disponibilidade de Estoque**
Deve indicar claramente se o produto está em estoque ou não.

### **R5.5 - Seletor de Quantidade**
- Deve permitir ao usuário aumentar/diminuir a quantidade desejada.
- Validação para quantidades inválidas (ex: zero, letras).

### **R5.6 - Botão "Adicionar ao Carrinho"**
- Deve adicionar a quantidade selecionada do produto (e suas variações) ao carrinho.
- Mensagem de confirmação (pop-up ou notificação) deve aparecer.
- O ícone do carrinho no cabeçalho deve ser atualizado.

### **R5.7 - Informações Adicionais**
Abas como "Data sheet", "Attachments", "Reviews" devem exibir o conteúdo correto.

### **R5.8 - Compartilhamento em Redes Sociais**
Se houver botões de compartilhamento, devem funcionar.

### **R5.9 - Produtos Relacionados/Sugeridos**
Seção deve exibir produtos relevantes e clicáveis.

### **R5.10 - Avaliações e Comentários (Reviews)**
- Exibição de avaliações existentes.
- Funcionalidade de escrever uma nova avaliação (se habilitada para visitantes ou apenas logados). Formulário com validações.

---

## 6. Carrinho de Compras (Shopping Cart)

### **R6.1 - Exibição dos Itens**
- Todos os produtos adicionados devem ser listados com imagem, nome, variações selecionadas, preço unitário, quantidade e subtotal.

### **R6.2 - Atualização de Quantidade**
Permitir alterar a quantidade de cada item no carrinho; o subtotal e o total geral devem ser recalculados.

### **R6.3 - Remoção de Itens**
Permitir remover itens do carrinho; o total geral deve ser recalculado.

### **R6.4 - Resumo do Pedido**
Exibição clara de subtotal, descontos (se aplicados), impostos (se configurados), custos de envio (se calculados nesta etapa) e total geral.

### **R6.5 - Cupom de Desconto**
- Campo para inserir código de cupom.
- Aplicação de cupons válidos, com o desconto refletido no total.
- Mensagem de erro para cupons inválidos ou expirados.

### **R6.6 - Botões de Ação**
- "Continuar Comprando" (redireciona para a loja, geralmente homepage ou última categoria visitada).
- "Proceder para o Checkout".

### **R6.7 - Carrinho Vazio**
Mensagem apropriada quando o carrinho está vazio, com sugestão para continuar comprando.

---

## 7. Processo de Checkout

### **R7.1 - Checkout como Convidado vs. Login/Registro**
Opções devem estar claras.

### **R7.2 - Etapa de Endereços (Addresses)**
- Formulário para inserir endereço de cobrança e entrega.
- Validação de campos obrigatórios (nome, sobrenome, endereço, cidade, CEP, país, estado/província, telefone).
- Opção para "Usar este endereço para cobrança" se o endereço de entrega for o mesmo.
- Para usuários logados: opção de selecionar endereços salvos ou adicionar novo.

### **R7.3 - Etapa de Método de Envio (Shipping Method)**
- Exibição das opções de envio disponíveis com seus respectivos custos.
- Seleção de um método de envio deve atualizar o total do pedido.
- Possibilidade de adicionar comentários sobre o pedido.
- Concordância com Termos de Serviço (se obrigatório).

### **R7.4 - Etapa de Pagamento (Payment)**
- Exibição dos métodos de pagamento disponíveis (ex: "Pay by Check", "Pay by Bank Wire" - comuns em demos).
- Seleção de um método de pagamento.
- Entrada de dados de pagamento (para métodos que exigem, ex: cartão de crédito - geralmente simulado em demos).

### **R7.5 - Revisão do Pedido (Order Summary/Confirmation before payment)**
- Exibição de um resumo completo do pedido antes da finalização (produtos, quantidades, preços, endereços, método de envio, método de pagamento, total).

### **R7.6 - Finalização do Pedido**
- Botão "Place Order" (ou similar).
- Após finalização, redirecionamento para uma página de confirmação de pedido.
- A página de confirmação deve exibir o número do pedido e detalhes.
- E-mail de confirmação de pedido deve ser enviado (verificar se o demo envia e-mails reais ou simulados).

### **R7.7 - Tratamento de Erros no Checkout**
Mensagens claras para falhas de pagamento, problemas de endereço, etc.

---

## 8. Gerenciamento de Conta de Usuário (My Account)

### **R8.1 - Login**
- Campos para e-mail e senha.
- Validação para credenciais incorretas.
- Link "Esqueceu sua senha?".

### **R8.2 - Registro de Novo Usuário**
- Formulário com campos (nome, sobrenome, e-mail, senha, etc.).
- Validação de campos (e-mail único, força da senha, campos obrigatórios).
- Mensagem de sucesso após registro.
- E-mail de boas-vindas/confirmação (se configurado).

### **R8.3 - Recuperação de Senha**
- Campo para e-mail.
- Envio de instruções/link para redefinição de senha para o e-mail fornecido (se válido e existente).
- Processo de redefinição de senha (inserir nova senha, confirmação).

### **R8.4 - Painel da Conta (Dashboard)**
Visão geral da conta com links para outras seções.

### **R8.5 - Histórico de Pedidos (Order History and Details)**
- Lista de pedidos anteriores com status, data, total.
- Visualização dos detalhes de um pedido específico.
- Opção de "Reordenar" (se disponível).

### **R8.6 - Meus Endereços (My Addresses)**
- Visualizar, adicionar, editar e excluir endereços de cobrança/entrega.

### **R8.7 - Minhas Informações Pessoais (My Personal Information)**
- Visualizar e editar dados pessoais (nome, e-mail, opção de mudar senha).
- Opções de consentimento `GDPR` (se aplicável).

### **R8.8 - Meus Vouchers/Cupons (My Vouchers)**
Exibição de cupons de desconto disponíveis para o usuário.

### **R8.9 - Logout**
Deve encerrar a sessão do usuário e redirecionar para uma página apropriada (ex: homepage ou página de login).

---

## 9. Páginas Estáticas (CMS Pages)

### **R9.1 - Acesso**
Links para páginas como "Sobre Nós", "Termos e Condições", "Política de Privacidade", "Contato" devem estar acessíveis (geralmente no rodapé ou menu de informações).

### **R9.2 - Conteúdo**
O conteúdo dessas páginas deve ser exibido corretamente.

### **R9.3 - Formulário de Contato (Contact Us page)**
- Campos para nome, e-mail, assunto, mensagem, anexos (se houver).
- Validação de campos.
- Envio da mensagem e confirmação.

---

## 10. Requisitos Não Funcionais (para Testes Manuais)

### **R-NF10.1 - Usabilidade**
- Facilidade de navegação e intuitividade.
- Clareza das informações e chamadas para ação (`CTAs`).
- Feedback visual para ações do usuário (ex: item adicionado ao carrinho).

### **R-NF10.2 - Performance Percebida**
- Páginas devem carregar em tempo razoável (sem atrasos excessivos perceptíveis).
- Ações como adicionar ao carrinho, aplicar filtros devem responder rapidamente.

### **R-NF10.3 - Compatibilidade entre Navegadores (Cross-Browser Testing)**
- O site deve funcionar e ser exibido corretamente nos principais navegadores (Chrome, Firefox, Edge, Safari - definir escopo).

### **R-NF10.4 - Acessibilidade (Básica)**
- Contraste de cores adequado.
- Navegação por teclado (uso do TAB para navegar entre elementos interativos).
- Textos alternativos (alt text) para imagens importantes (pode ser verificado inspecionando o elemento).

### **R-NF10.5 - Segurança (Perspectiva do Usuário)**
- Uso de `HTTPS` em todas as páginas, especialmente no checkout e login.
- Senhas mascaradas nos campos de entrada.
- Nenhuma informação sensível exposta em URLs.

---

## Considerações Específicas para o Ambiente de Demonstração

-   **Reset de Dados:** Verificar se o ambiente de demonstração reseta os dados periodicamente. Isso afeta a persistência dos testes.
-   **Dados de Teste:** Pode ser necessário criar contas de usuário, adicionar produtos ao carrinho, etc., para cada ciclo de teste se os dados forem resetados.
-   **Limitações do Demo:** Alguns recursos podem estar desabilitados ou simplificados (ex: métodos de pagamento reais, envio de e-mails para fora do sistema).

---

## Como Usar Esta Análise para Criar Casos de Teste

1.  **Para cada requisito (R...), crie um ou mais casos de teste.**
    *   **Exemplo para R5.6 (Botão "Adicionar ao Carrinho" na `PDP`):**
        > **CT_PDP_001:** **Dado que** o usuário está na `PDP` de um produto simples em estoque, **Quando** ele seleciona a quantidade "1" e clica em "Adicionar ao Carrinho", **Então** o produto deve ser adicionado ao carrinho, uma mensagem de sucesso deve ser exibida, e o ícone do carrinho deve ser atualizado com "1" item.
        >
        > **CT_PDP_002:** **Dado que** o usuário está na `PDP` de um produto com variações obrigatórias, **Quando** ele NÃO seleciona uma variação e clica em "Adicionar ao Carrinho", **Então** uma mensagem de erro deve ser exibida solicitando a seleção da variação e o produto NÃO deve ser adicionado ao carrinho.
        >
        > **CT_PDP_003:** **Dado que** o usuário está na `PDP` de um produto fora de estoque, **Então** o botão "Adicionar ao Carrinho" deve estar desabilitado ou exibir uma mensagem indicando indisponibilidade.

2.  **Pense em cenários positivos e negativos.**
    *   **Positivo:** O usuário faz tudo corretamente.
    *   **Negativo:** O usuário insere dados inválidos, tenta ações não permitidas, etc.

3.  **Considere diferentes tipos de dados de entrada.**
    *   Valores limite, dados válidos, dados inválidos, campos vazios.

4.  **Priorize os casos de teste** com base na criticidade da funcionalidade (ex: checkout é mais crítico que uma página estática).
