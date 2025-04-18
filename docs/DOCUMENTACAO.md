
---

## 📋 Etapas Realizadas
# 📑 Documentação do Projeto de QA Automation - Cypress

## 🎯 Objetivo do Projeto

Criar um portfólio profissional de automação de testes utilizando **Cypress**, para demonstrar habilidades práticas em automação web, organização de testes, boas práticas e estrutura de projetos em QA.

---

## 👨‍💻 Responsável pelo Projeto

- Nome: **Rodrigo Dantas**
- GitHub: [Devrodd](https://github.com/Devrodd)
- E-mail: rodrigodeveloperios@gmail.com

---

## 📚 Tecnologias Utilizadas

- Node.js
- Cypress
- Git & GitHub

---

## 🛠 Estrutura do Projeto


### 1. Criação do Projeto

- [x] Criar repositório público no GitHub
- [x] Inicializar projeto Node.js com `npm init`
- [x] Instalar Cypress com `npm install cypress --save-dev`
- [x] Configurar a estrutura padrão do Cypress

### 2. Primeiro Teste Automatizado - Login Válido

- [x] Criar teste `login.cy.js` na pasta `e2e`
- [x] Testar login bem-sucedido no site [Sauce Demo](https://www.saucedemo.com/)
- [x] Verificar sucesso do login validando a URL `/inventory.html`

**Cenário implementado:**
| Cenário | Resultado Esperado |
|:--|:--|
| Login com usuário e senha válidos | Acesso à página de inventário |

**Código utilizado:**

```javascript
describe('Login Sauce Demo', () => {
  it('Deve logar com sucesso', () => {
    cy.visit('https://www.saucedemo.com/');
    cy.get('[data-test="username"]').type('standard_user');
    cy.get('[data-test="password"]').type('secret_sauce');
    cy.get('[data-test="login-button"]').click();
    cy.url().should('include', '/inventory.html');
  });
});
