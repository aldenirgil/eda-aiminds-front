# Guia de Configuração do Projeto

Este documento fornece instruções detalhadas para configurar o ambiente de desenvolvimento do EDA AI Minds Frontend.

## 📋 Pré-requisitos

### Ferramentas Necessárias

- **Node.js** (versão 18.0.0 ou superior)
- **npm** (versão 8.0.0 ou superior) ou **yarn**
- **Git** (versão 2.30.0 ou superior)
- **Editor de Código** (VS Code recomendado)

### Verificando Versões

```bash
node --version    # Deve ser >= 18.0.0
npm --version     # Deve ser >= 8.0.0
git --version     # Deve ser >= 2.30.0
```

## 🚀 Configuração Inicial

### 1. Clone do Repositório

```bash
# Clone o repositório
git clone https://github.com/aldenirgil/eda-aiminds-front.git

# Entre no diretório
cd eda-aiminds-front
```

### 2. Instalação de Dependências

```bash
# Usando npm
npm install

# Ou usando yarn
yarn install
```

### 3. Configuração de Variáveis de Ambiente

```bash
# Copie o arquivo de exemplo
cp .env.example .env.local

# Edite as variáveis conforme necessário
vim .env.local
```

### 4. Configuração do Editor

#### VS Code

Instale as seguintes extensões:

- **ESLint** (dbaeumer.vscode-eslint)
- **Prettier** (esbenp.prettier-vscode)
- **Auto Rename Tag** (formulahendry.auto-rename-tag)
- **Bracket Pair Colorizer** (coenraads.bracket-pair-colorizer)
- **GitLens** (eamodio.gitlens)

#### Configurações do VS Code

Crie `.vscode/settings.json`:

```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ]
}
```

## 🔧 Scripts Disponíveis

```bash
# Desenvolvimento
npm run dev          # Inicia servidor de desenvolvimento

# Build
npm run build        # Build para produção
npm run preview      # Preview da build de produção

# Qualidade de Código
npm run lint         # Executa ESLint
npm run lint:fix     # Corrige problemas de lint automaticamente
npm run format       # Formata código com Prettier

# Testes
npm run test         # Executa testes
npm run test:watch   # Executa testes em modo watch
npm run test:coverage # Gera relatório de cobertura
```

## 🌐 URLs de Desenvolvimento

- **Aplicação Local**: http://localhost:3000
- **Storybook**: http://localhost:6006 (se configurado)
- **Documentação**: http://localhost:8080/docs (se configurado)

## 🔒 Configuração de Segurança

### 1. Configuração de Git Hooks

```bash
# Instalar husky para git hooks
npm install --save-dev husky

# Configurar pre-commit hooks
npx husky install
npx husky add .husky/pre-commit "npm run lint"
npx husky add .husky/pre-push "npm run test"
```

### 2. Configuração de Commitizen

```bash
# Instalar commitizen
npm install --save-dev commitizen cz-conventional-changelog

# Configurar commitizen
echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc
```

## 🐛 Solução de Problemas

### Problemas Comuns

#### Erro de permissão no npm

```bash
# Configurar npm para usar diretório diferente
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.profile
source ~/.profile
```

#### Porta já em uso

```bash
# Verificar processos na porta 3000
lsof -ti:3000

# Parar processo
kill -9 $(lsof -ti:3000)
```

#### Cache corrompido

```bash
# Limpar cache do npm
npm cache clean --force

# Deletar node_modules e reinstalar
rm -rf node_modules package-lock.json
npm install
```

### Logs de Debug

```bash
# Executar com logs detalhados
DEBUG=* npm run dev

# Verificar configuração do npm
npm config list
```

## 📚 Recursos Adicionais

- [Documentação do Node.js](https://nodejs.org/docs/)
- [Documentação do npm](https://docs.npmjs.com/)
- [Guia do Git](https://git-scm.com/docs)
- [VS Code Tips](https://code.visualstudio.com/docs)

## 🆘 Precisa de Ajuda?

- **Issues**: [GitHub Issues](https://github.com/aldenirgil/eda-aiminds-front/issues)
- **Discussions**: [GitHub Discussions](https://github.com/aldenirgil/eda-aiminds-front/discussions)
- **Email**: aldenirgil@example.com

---

**Pronto para começar! 🎉**