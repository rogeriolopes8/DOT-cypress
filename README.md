# DOT-cypress
Testes automatizados de validação de formulário com Cypress, cobrindo cenários de validação de campos obrigatórios, formato de dados e envio com sucesso.

# Testes Automatizados para Formulário de Solicitação de Informações do Curso de Pediatria

## 📖 História do Usuário

**Título:** Solicitação de Informações do Curso de Pediatria  
**Descrição:**  
Como usuário interessado no curso de Pediatria, desejo preencher o formulário de contato para solicitar mais informações sobre o curso, possibilitando um atendimento personalizado e a obtenção de esclarecimentos necessários antes de me matricular.

---

## ✅ Critérios de Aceitação

1. **Exibição do Formulário:**
   - O formulário deve estar visível e acessível ao usuário ao acessar a página do curso.

2. **Campos Obrigatórios e Validação:**
   - **Nome Completo:** Campo obrigatório.
   - **Email:** Campo obrigatório, com validação de formato (ex.: `usuario@dominio.com`).
   - **Telefone:** Campo obrigatório (com máscara para número válido).
   - **Sua área de atuação:** Campo obrigatório, com opções pré-definidas:
     - Não sou médico(a)
     - Clínico Geral
     - Psiquiatria
     - Cardiologista
     - Ortopedista
     - Cirurgião
     - Médico (Outros)
     - Estudante
     - Pediatria
     - Endoscopia

3. **Feedback Visual:**
   - Mensagens de erro devem ser exibidas ao lado ou abaixo dos campos obrigatórios que estão vazios ou com dados inválidos.
   - Quando o formulário for preenchido corretamente e enviado, deve ser exibida uma mensagem de sucesso ou redirecionamento para uma página de confirmação.

4. **Envio do Formulário:**
   - O botão "Enviar" deve submeter os dados.
   - O sistema deve validar os dados antes do envio e, em caso de sucesso, processar a solicitação (simulação de envio via API ou redirecionamento).

5. **Persistência dos Dados:**
   - Se o envio for bem-sucedido, os dados não devem ser perdidos (caso haja redirecionamento ou recarregamento, a confirmação deve ser apresentada).

---

## 🔍 Casos de Testes

1. **Campos obrigatórios vazios**  
   - **Cenário:** O usuário acessa o formulário e tenta enviá-lo sem preencher os campos.  
   - **Resultado Esperado:** Exibição de mensagens de erro nos campos obrigatórios.

2. **Validação de email**  
   - **Cenário:** O usuário insere um email inválido.  
   - **Resultado Esperado:** O formulário exibe um erro indicando que o email é inválido.

3. **Formato de telefone inválido**  
   - **Cenário:** O usuário insere um número de telefone fora do formato exigido.  
   - **Resultado Esperado:** O formulário exibe um erro indicando o formato correto.

4. **Seleção de área de atuação**  
   - **Cenário:** O usuário não seleciona uma área de atuação.  
   - **Resultado Esperado:** O formulário exibe um erro pedindo que uma área seja selecionada.

5. **Envio de formulário válido**  
   - **Cenário:** O usuário preenche todos os campos corretamente, incluindo a área de atuação.  
   - **Resultado Esperado:** O formulário é enviado com sucesso e uma mensagem de confirmação é exibida.

---


## ⏱️ Estimativa de Tempo de Teste

**Tempo Total:** **4 horas**

1. **Planejamento dos testes:** 30 minutos  
2. **Testes manuais:**
   - Validação de campos: 30 minutos  
   - Funcionalidade de envio: 30 minutos  
3. **Desenvolvimento dos testes automatizados:** 2 horas  
4. **Documentação dos resultados:** 30 minutos  

---

## 🛠️ Ferramentas Utilizadas

- **Cypress** para desenvolvimento de testes automatizados.
- **Visual Studio Code (VS Code)** como IDE para desenvolvimento.
- **JavaScript** para implementação dos casos de testes.

---

## 💡 Como Executar os Testes

1. Clone este repositório:
   ```bash
   git clone <https://github.com/rogeriolopes8/DOT-cypress>

