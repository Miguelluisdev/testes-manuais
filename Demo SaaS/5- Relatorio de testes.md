# ✅ **Relatório Final de Execução de Testes - Demo SaaS**

**Sistema testado:** Demo SaaS (versão pública demo)
**Responsável:** Miguel Luis
**Data de execução:** 19 de Maio de 2025
**Ambiente:**

* Sistema operacional: Windows 11 / Motorola g75 5g
* Navegador: Microsoft Edge v.136.0 / Google Chrome 124.0 mobile
* URL: [Demo SaaS]( https://demo-saas.bugbug.io/)

---

## 📊 **Resumo da Execução**

| Total de Casos de Teste | Casos Passaram | Casos Falharam | Bugs Registrados |
| ----------------------- | -------------- | -------------- | ---------------- |
| 32                      | 24             | 6              | 6                |

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo                   | Casos Testados | Casos Passaram | Bugs encontrados | Bug(s) Associado(s)       |
| --------- | ------------------------ | -------------- | -------------- | -------------- | ------------------------- |
| RF01      | Autenticação de Usuário                    | 4              | 4              | 2              | BUG-001 |
| RF02      | 	Registro de Usuário               | 	4              | 	4              | 0              | -                         |
| RF03      | Criação de Organização       | 4             | 4             | 0              |                   |
| RF04      | 	Gerenciamento de Conta           | 4              | 3              | 1              | BUG-003, BUG-004, BUG-006                   |
| RF05      |Navegação na Plataforma             | 4              | 3              | 1              | BUG-005                 |
| RF06      | 	Dashboard de Tickets    | 4             | 4              | 0              | -                         |
| RF07      | 	Compartilhamento de Projetos | 4              | 0             | 0              | Testes não realizados                       |
| RF08      | Recuperação de Senha              | 4              | 3           | 1             |  BUG-002                        |


---

## 🐞 **Resumo dos Bugs Reportados**

| ID      | Título                                                                                                              | Severidade | Status |
| ------- | ------------------------------------------------------------------------------------------------------------------- | ---------- | ------ |
| BUG-001 | Campo email no login com mensagem genérica “Invalid email” ao invés de “Campo vazio”                                | Média      | Aberto |
| BUG-002 | Ausência de mensagens claras de erro/sucesso após login ou falha                                                    | Média      | Aberto |
| BUG-003 | Possível criar ticket após encerramento da sessão, mas não visualizar os tickets                                    | Crítico    | Aberto |
| BUG-004 | Persistência do perfil e projeto visível no header após logout                                                      | Crítico    | Aberto |
| BUG-005 | Rota inválida não exibe mensagem 404, somente tela em branco                                                        | Média      | Aberto |
| BUG-006 | Recuperação de senha envia email para endereços não cadastrados                                                     | Crítico    | Aberto |


---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 24
* ❌ Falharam: 6

**Severidade dos bugs:**

* 🟥 Alta: 4
* 🟨 Média: 4
* 🟩 Baixa: 0

---

## 📁 **Evidências e Documentos**

* ✔️ [Plano de Testes (Markdown)]
* ✔️ [Casos de Teste (Planilha ou Markdown)]
* 🐛 [Relatório de Bugs com Evidências em Vídeo]
* 📹 Evidências em vídeo hospedadas no [Jam.dev]

---

## ✅ **Conclusão**

A execução dos testes manuais mostrou um sistema funcional em grande parte, com 24 casos aprovados de um total de 32, porém com falhas críticas em módulos fundamentais, especialmente na gestão de sessão e segurança, afetando diretamente a experiência e a integridade dos dados dos usuários.

🔍 Identificação da Causa Raiz (Root Cause Analysis)
A identificação da causa raiz é uma etapa essencial no processo de garantia de qualidade (QA), pois busca entender por que um defeito ocorreu, indo além dos sintomas visíveis do problema. Essa análise ajuda a evitar recorrência de falhas, melhorando a qualidade do software a longo prazo.

Ao encontrar um bug, o QA não deve apenas registrá-lo, mas também investigar sua origem. A causa raiz pode estar em erros de lógica no código, falhas de validação, má comunicação entre equipes, requisitos mal definidos ou até inconsistências no ambiente de teste. Ferramentas como 5 Porquês, Diagrama de Ishikawa ou análise de logs podem ser utilizadas para essa investigação.

Identificar corretamente a causa raiz permite que os desenvolvedores corrijam o erro de forma precisa e que o time evite retrabalhos, contribuindo para entregas mais estáveis, eficientes e com menor custo.

| ID          | Causa Raiz Provável                                                                                                                                         |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BUG-001** | Falta de tratamento específico para o campo vazio no backend ou frontend. A validação genérica não diferencia um campo vazio de um formato inválido.        |
| **BUG-002** | O sistema parece não implementar feedback visual/textual após ações de login, sugerindo ausência de mensagens de estado no código ou falha no front-end.    |
| **BUG-003** | A sessão do usuário não está sendo devidamente invalidada no backend, permitindo ações após logout por meio de tokens ainda válidos ou cache do navegador.  |
| **BUG-004** | Falha no gerenciamento da UI após logout. Os dados do usuário e do projeto ainda são renderizados por ausência de uma limpeza adequada no estado do app.    |
| **BUG-005** | Não há tratamento de erro ou rota padrão configurada para URLs inválidas. Isso pode ser causado por falta de página 404 ou falha no roteamento global.      |
| **BUG-006** | A verificação de existência do email antes do envio do link de recuperação de senha não está sendo feita corretamente, permitindo envio mesmo sem cadastro. |

