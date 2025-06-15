# ✅ Relatório de Testes - Requisito Funcional RF01: Login e Cadastro

📌 **Prioridade:** ALTA  
📅 **Data de Execução:** 11 de Junho de 2025  
🔍 **Funcionalidade Testada:** Login, Cadastro, Logout, Recuperação de Senha  
🌐 **Sistema:** PrestaShop Demo  
🔧 **Método de Teste:** Manual  

---

## 📚 Cenários e Resultados

### 🔐 Cenário 01: Login com sucesso
- **CT01 - Login com credenciais válidas**  
  ✅ Resultado: **Passou**

---

### ❌ Cenário 01.2: Login com credenciais inválidas
- **CT02 - Login com senha incorreta**  
  ✅ Resultado: **Passou**

---

### 🧾 Cenário 01.3: Tentativa de login com e-mail não cadastrado
- **CT03 - Login com e-mail inexistente**  
  ✅ Resultado: **Passou**

---

### 📝 Cenário 01.4: Validação de campos obrigatórios no login
- **CT04 - Tentativa de login com campos vazios**  
  ✅ Resultado: **Passou**

---

### 👤 Cenário 01.5: Registro de novo usuário com sucesso
- **CT05 - Registro com dados válidos**  
  ✅ Resultado: **Passou**

---

### 🔁 Cenário 01.6: Tentativa de registro com e-mail já existente
- **CT06 - Registro com e-mail duplicado**  
  ✅ Resultado: **Passou**  
  📌 *Mensagem apresentada:*  
  `The email is already used, please choose another one or sign in`

---

### 🔒 Cenário 01.7: Validação de força de senha no registro
- **CT07 - Registro com senha fraca**  
  ✅ Resultado: **Passou**

---

### 🔓 Cenário 01.8: Recuperação de senha
- **CT08 - Recuperação de senha com e-mail válido**  
  ❌ Resultado: **Falhou**  
  📌 *Mensagem de erro exibida:*  
  `An error occurred while sending the email.`  
  Mesmo com e-mails válidos e cadastrados, o sistema retorna erro ao tentar recuperar senha.  
  🎥 **Evidência:** [Jam.dev Vídeo da Falha](https://jam.dev/c/7e3dc316-ab39-402e-b69c-f5cba3583f95)

---

### 🔚 Cenário 01.9: Logout
- **CT09 - Logout com sessão ativa**  
  ✅ Resultado: **Passou**  
  ⚠️ *Observação:* Após logout, o usuário é redirecionado para a **última página acessada antes do login**, o que pode causar confusão em fluxos como "Forgot Password".

---

## 🐞 Bugs Encontrados

| ID   | Descrição                                                                                   | Severidade | Prioridade | Evidência |
|------|---------------------------------------------------------------------------------------------|------------|------------|-----------|
| B01  | Recuperação de senha falha mesmo com e-mails válidos                                        | Alta       | Alta       | [Jam.dev](https://jam.dev/c/7e3dc316-ab39-402e-b69c-f5cba3583f95) |
| B02  | Após logout, usuário é redirecionado para a página anterior ao login (ex: Forgot Password)  | Média      | Média      | Vídeo acima |
| B03  | Sessão expira rapidamente: ao atualizar a página, o usuário perde a sessão e é desconectado | Alta       | Alta       | N/A       |

---

## 📌 Conclusão

A maioria dos casos de teste para login e cadastro foi bem-sucedida, validando os fluxos principais. No entanto, falhas críticas foram encontradas no processo de **recuperação de senha** e na **gestão de sessão** do usuário, que devem ser corrigidas para garantir a confiabilidade da autenticação.

---

👤 **Autor dos Testes:** Miguel Luis
🧪 **Tipo de Teste:** Manual  
📂 **Arquivo Original dos Testes:** `CT_RF01: Login e Cadastro (Prioridade: ALTA).md`  

