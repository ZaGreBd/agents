# NLW Agents

Projeto desenvolvido durante a Next Level Week Agents da [Rocketseat](https://www.rocketseat.com.br/).

## Descrição

Este projeto é um backend desenvolvido em Node.js com TypeScript, utilizando Fastify para o servidor web, Drizzle ORM para interação com o banco de dados PostgreSQL e pgvector para funcionalidades de busca vetorial.

## Tecnologias

- **Node.js**: Ambiente de execução JavaScript no servidor.
- **TypeScript**: Superset do JavaScript que adiciona tipagem estática.
- **Fastify**: Framework web para Node.js, focado em performance.
- **Drizzle ORM**: ORM para TypeScript que oferece uma sintaxe similar a SQL.
- **PostgreSQL**: Banco de dados relacional.
- **pgvector**: Extensão para PostgreSQL que permite o armazenamento e busca de vetores.
- **Docker**: Plataforma de contêineres para facilitar o setup do ambiente de desenvolvimento.

## Arquitetura e Padrões de Projeto

O projeto segue uma arquitetura em camadas, separando as responsabilidades em:

- **`src/http/routes`**: Define as rotas da API e lida com as requisições e respostas HTTP.
- **`src/use-cases`**: Contém a lógica de negócio da aplicação.
- **`src/db`**: Camada de acesso a dados, responsável pela comunicação com o banco de dados utilizando Drizzle ORM.

## Setup e Configuração

### Pré-requisitos

- Node.js (v18 ou superior)
- Docker

### Instalação

1. Clone o repositório:

   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd <NOME_DO_PROJETO>
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Crie um arquivo `.env` na raiz do projeto, baseado no `.env.example` (se houver) ou com as seguintes variáveis:

   ```env
   DATABASE_URL="postgresql://docker:docker@localhost:5432/agents"
   ```

### Execução

1. Inicie o banco de dados com Docker:

   ```bash
   docker-compose up -d
   ```

2. Rode as migrations do banco de dados:

   ```bash
   npx drizzle-kit migrate
   ```

3. Inicie o servidor de desenvolvimento:

   ```bash
   npm run dev
   ```

O servidor estará disponível em `http://localhost:3333`.
