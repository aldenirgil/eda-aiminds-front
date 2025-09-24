# Guia de Contribuição

Obrigado por considerar contribuir para o EDA AI Minds Frontend! Este documento fornece diretrizes para contribuições.

## 🚀 Como Contribuir

### 1. Fork e Clone

1. Faça um fork do repositório
2. Clone seu fork localmente:
   ```bash
   git clone https://github.com/seu-usuario/eda-aiminds-front.git
   cd eda-aiminds-front
   ```

### 2. Configuração do Ambiente

```bash
# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

### 3. Criando uma Branch

```bash
# Crie uma branch para sua feature/fix
git checkout -b feature/nome-da-feature
# ou
git checkout -b fix/nome-do-bug
```

## 📝 Padrões de Código

### Convenções de Nomenclatura

- **Componentes**: PascalCase (`Button`, `UserProfile`)
- **Arquivos**: camelCase (`userService.js`, `apiHelpers.js`)
- **Constantes**: UPPER_SNAKE_CASE (`API_BASE_URL`)
- **Variáveis/Funções**: camelCase (`userName`, `fetchUserData`)

### Estrutura de Commits

Use o padrão [Conventional Commits](https://www.conventionalcommits.org/):

```
tipo(escopo): descrição

tipos: feat, fix, docs, style, refactor, test, chore
```

Exemplos:
```
feat(auth): add login functionality
fix(ui): correct button alignment issue
docs(readme): update installation guide
```

### Linting e Formatação

```bash
# Executar linting
npm run lint

# Corrigir problemas automaticamente
npm run lint:fix

# Formatação de código
npm run format
```

## 🧪 Testes

- Escreva testes para novas funcionalidades
- Mantenha cobertura acima de 80%
- Execute testes antes de submeter PR:

```bash
npm run test
npm run test:coverage
```

## 🔄 Pull Requests

### Antes de Submeter

1. ✅ Código segue os padrões estabelecidos
2. ✅ Testes passam localmente
3. ✅ Documentação atualizada (se necessário)
4. ✅ Commit messages seguem o padrão
5. ✅ Branch está atualizada com a main

### Template de PR

- **Descrição**: O que foi alterado e por quê
- **Tipo**: Feature, Bug Fix, Documentation, etc.
- **Screenshots**: Se aplicável
- **Testes**: Como testar as mudanças
- **Checklist**: Todos os itens verificados

## 🐛 Reportando Bugs

Use o template de issue para bugs:

1. **Descrição clara** do problema
2. **Passos para reproduzir** o bug
3. **Comportamento esperado** vs **atual**
4. **Screenshots** ou **logs** se aplicável
5. **Ambiente** (OS, browser, versão)

## 💡 Sugerindo Features

Para novas funcionalidades:

1. **Descreva o problema** que a feature resolve
2. **Proponha uma solução** detalhada
3. **Considere alternativas** se houver
4. **Adicione contexto** adicional se necessário

## 📋 Checklist para Contribuições

- [ ] Branch criada a partir da `main`
- [ ] Código segue os padrões do projeto
- [ ] Testes adicionados/atualizados
- [ ] Documentação atualizada
- [ ] Commits seguem o padrão
- [ ] PR tem título descritivo
- [ ] Todas as verificações passam

## 🤝 Processo de Review

1. **Automated Checks**: CI/CD deve passar
2. **Code Review**: Pelo menos 1 aprovação
3. **Testing**: Funcionalidade testada
4. **Documentation**: Se necessário, docs atualizadas

## 📞 Contato

- **Issues**: Para bugs e features
- **Discussions**: Para perguntas gerais
- **Email**: Para questões sensíveis

## 📄 Código de Conduta

Este projeto segue o [Contributor Covenant](https://www.contributor-covenant.org/). Esperamos que todos os participantes sigam estas diretrizes para manter um ambiente acolhedor e inclusivo.

---

**Obrigado por contribuir! 🎉**