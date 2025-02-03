# Plano de Testes - Preenchimento de Formulário

## 1. História do Usuário  

**Título:** Preenchimento de Formulário de Cadastro  

**Descrição:**  
Como um usuário do site **Way2Automation**, quero preencher e enviar um formulário de cadastro para garantir que os dados sejam submetidos corretamente e visualizar a mensagem de confirmação após a submissão bem-sucedida.  

---

## 2. Critérios de Aceite  

1. O formulário deve permitir a entrada de dados nos seguintes campos:  
   - Nome  
   - Telefone  
   - E-mail  
   - Cidade  
   - Nome de usuário  
   - Senha  
   - Seleção do país  

2. Os campos devem estar visíveis e permitir a digitação.  

3. Após preencher corretamente os dados e clicar no botão de envio, deve aparecer a mensagem de confirmação:  
   - **"This is just a dummy form, you just clicked SUBMIT BUTTON"**  

4. O botão de envio deve estar visível e acionável.  

5. O sistema não deve apresentar erros durante o processo de preenchimento e submissão.  

---

## 3. Casos de Teste  

| ID  | Caso de Teste | Passos | Entrada | Resultado Esperado |
|-----|-------------|--------|---------|--------------------|
| CT01 | Validar se os campos do formulário estão visíveis | Acessar a página e verificar a visibilidade dos campos | - | Todos os campos devem estar visíveis |
| CT02 | Preencher o formulário com dados válidos | Digitar informações válidas nos campos do formulário e clicar no botão de envio | Nome: Rogerio Lopes, Telefone: (48)988329640, Email: rogerio.lord@gmail.com, Cidade: Floripa, Usuário: rogeriol, Senha: 123456, País: Brazil | Mensagem "This is just a dummy form, you just clicked SUBMIT BUTTON" deve aparecer |
| CT03 | Validar se o botão de envio está visível e acionável | Verificar se o botão está visível antes da submissão | - | O botão deve estar visível e clicável |
| CT04 | Testar preenchimento parcial (faltando um campo obrigatório) | Deixar um dos campos obrigatórios em branco e tentar submeter | Deixar o campo "Nome" vazio | O sistema deve exibir erro ou impedir a submissão |
| CT05 | Inserir e-mail inválido | Digitar um e-mail inválido (ex: rogerio.lord.com) | Email: rogerio.lord.com | O sistema deve exibir erro ou impedir a submissão |
| CT06 | Testar submissão com senha fraca | Inserir senha curta (ex: "123") | Senha: "123" | O sistema deve exibir erro se houver validação de senha |
| CT07 | Selecionar país inválido | Escolher uma opção inexistente (se aplicável) | País: Opção inválida | O sistema não deve permitir seleção inválida |
| CT08 | Testar a submissão múltipla | Clicar várias vezes no botão de envio rapidamente | Múltiplos cliques no botão | O sistema deve processar apenas um envio |

---

## 4. Estimativa de Tempo para Testes  

### **Cálculo do Tempo de Teste**  

**Fatores Considerados:**  
1. **Configuração do ambiente:** Acesso ao site e preparação inicial (~5 minutos).  
2. **Execução de cada teste manualmente:**  
   - Testes básicos (~2 a 5 minutos por teste).  
   - Testes que envolvem validação de erro (~3 a 7 minutos cada).  
   - Testes repetitivos, como cliques múltiplos (~3 minutos).  
3. **Registro dos resultados e geração de relatórios (~10 minutos).**  

| Tipo de Teste | Número de Casos | Tempo Estimado por Caso | Tempo Total |
|--------------|---------------|----------------------|------------|
| Testes de preenchimento válido | 2 | 3 min | 6 min |
| Testes de validação de erro | 4 | 5 min | 20 min |
| Testes de usabilidade e UX | 2 | 3 min | 6 min |
| Configuração do ambiente | - | 5 min | 5 min |
| Registro dos resultados | - | 10 min | 10 min |
| **Total Estimado** | **8** | - | **47 min** |

O tempo total estimado para a execução manual completa dos testes é **aproximadamente 47 minutos**.  

---

## 5. Conclusão  

Este plano de testes cobre as validações essenciais do formulário, garantindo que a experiência do usuário seja fluida e sem erros. Os testes contemplam tanto cenários positivos (preenchimento válido) quanto negativos (erros e usabilidade), garantindo a confiabilidade da funcionalidade.  

---
