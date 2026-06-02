# Frontend (Next.js + React)

## Requisitos

- Node.js **20 ou superior**
- NPM instalado

Verifique sua versao do Node.js:

```powershell
node --version
```

Verifique sua versao do NPM:

```powershell
npm --version
```

Caso a versao do Node.js seja inferior a 20, atualize o Node antes de prosseguir.

## Setup local

1. Instalar dependencias:

```powershell
npm install
```

2. Criar o arquivo de variaveis de ambiente:

```powershell
Copy-Item .env.example .env
```

3. Conferir a URL da API no arquivo `.env`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

4. Rodar o frontend:

```powershell
npm run dev
```

5. Acessar a aplicacao:

```text
http://localhost:3000
```

## Docker

Na raiz do projeto, execute:

```powershell
docker compose up --build frontend
```

Ou suba toda a aplicacao:

```powershell
docker compose up --build
```

## Scripts

- `npm run dev`: inicia o servidor de desenvolvimento
- `npm run build`: gera a build de producao
- `npm run start`: inicia a aplicacao em modo producao apos o build
- `npm run lint`: executa o ESLint

## Rotas

- `/`
- `/produto`

> **Importante:** Antes de usar o frontend, rode o backend em `http://localhost:8000`.
