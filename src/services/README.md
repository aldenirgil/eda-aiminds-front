# Services

Este diretório contém os serviços para comunicação com APIs e lógica de negócio.

## Estrutura

```
services/
├── api/             # Configuração e instâncias de API
├── auth/            # Serviços de autenticação
├── storage/         # Serviços de armazenamento local
└── utils/           # Utilitários para serviços
```

## Convenções

- Use camelCase para nomes de arquivos
- Separe lógica de API da lógica de negócio
- Implemente tratamento de erros consistente
- Use TypeScript para tipagem de APIs