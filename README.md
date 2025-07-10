# NLW Agents

Projeto desenvolvido para estudos em um curso de TypeScript e React moderno, utilizando tecnologias modernas para criação de uma API robusta e eficiente.

## 🚀 Tecnologias

- **Runtime**: Node.js com TypeScript
- **Framework**: Fastify (API REST)
- **Banco de Dados**: PostgreSQL com pgvector
- **ORM**: Drizzle ORM
- **Validação**: Zod
- **Linter**: Biome
- **Containerização**: Docker

## 📋 Pré-requisitos

- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

## ⚙️ Configuração

1. **Clone o repositório**
```bash
git clone <repository-url>
cd nlw/server
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

4. **Inicie o banco de dados**
```bash
docker-compose up -d
```

5. **Execute as migrações e seed**
```bash
npm run db:seed
```

## 🏃‍♂️ Executando o projeto

**Desenvolvimento:**
```bash
npm run dev
```

**Produção:**
```bash
npm start
```

O servidor estará disponível em `http://localhost:3333`

## 📁 Estrutura do Projeto

```
src/
├── db/           # Configuração do banco de dados
├── http/         # Rotas da API
├── env.ts        # Validação de variáveis de ambiente
└── server.ts     # Configuração do servidor
```

## 🔧 Scripts Disponíveis

- `npm run dev` - Executa em modo desenvolvimento com hot reload
- `npm start` - Executa em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais

## 🛠️ Padrões de Projeto

- **Arquitetura**: API REST com Fastify
- **Validação**: Schema validation com Zod
- **Banco de Dados**: Type-safe com Drizzle ORM
- **Código**: Linting com Biome
- **Containerização**: Docker para desenvolvimento 