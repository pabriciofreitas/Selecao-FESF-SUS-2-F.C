# Frontend (Next.js + React)

## Requisitos

- Node.js **20 ou superior**
- NPM instalado
- Docker Desktop instalado para uso em containers

Verifique sua versao do Node.js:

```powershell
node --version
```

Verifique sua versao do NPM:

```powershell
npm --version
```

## Setup local

1. Instale as dependencias:

```powershell
npm install
```

2. Copie o arquivo de ambiente:

```powershell
Copy-Item .env.example .env
```

3. Verifique a URL da API no arquivo `.env`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

4. Rode o frontend:

```powershell
npm run dev
```

5. Acesse a aplicacao:

```text
http://localhost:3000
```

## Docker

### Usando Docker Compose

Na raiz do projeto, execute:

```powershell
docker compose up --build frontend
```

Ou inicie toda a aplicacao:

```powershell
docker compose up --build
```

### Alternativa direta no frontend

Se quiser construir apenas o container do frontend:

```powershell
docker build -t desafio-frontend .

docker run --rm -p 3000:3000 -e NEXT_PUBLIC_API_URL=http://localhost:8000 desafio-frontend
```

## Scripts

- `npm run dev`: inicia o servidor de desenvolvimento
- `npm run build`: gera a build de producao
- `npm run start`: inicia a aplicacao em modo producao apos o build
- `npm run lint`: executa o ESLint

## Rotas

- `/`
- `/produto`

## Solucao de problemas Docker

- Se o frontend nao abrir, verifique se o backend esta rodando em `http://localhost:8000`.
- Se o comando `docker compose` nao for reconhecido, instale Docker Desktop ou use o alias `docker compose` correto.
- Se a aplicacao falhar na build, confirme se `NEXT_PUBLIC_API_URL` esta definido como `http://localhost:8000`.

> **Importante:** Antes de usar o frontend, rode o backend em `http://localhost:8000`.
