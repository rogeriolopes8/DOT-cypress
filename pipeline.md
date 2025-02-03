name: Cypress Tests

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      # 1. Configura o repositório
      - name: Check out the repository
        uses: actions/checkout@v3

      # 2. Configura o Node.js
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: 18

      # 3. Instala as dependências
      - name: Install dependencies
        run: npm install

      # 4. Instala o Cypress
      - name: Install Cypress
        run: npx cypress install

      # 5. Executa os testes
      - name: Run Cypress tests
        run: npx cypress run

      # 6. Upload de vídeos e screenshots (se falhar)
      - name: Upload Cypress artifacts
        if: failure()
        uses: actions/upload-artifact@v3
        with:
          name: cypress-artifacts
          path: |
            cypress/screenshots
            cypress/videos
