# Desafio

Projeto dividido em duas partes:

- [Backend](./backend/README.md): API desenvolvida com FastAPI e SQLAlchemy.
- [Frontend](./frontend/README.md): aplicacao web desenvolvida com Next.js e React.

## Executar com Docker

Na raiz do projeto, execute:

```powershell
docker compose up --build
```

Depois acesse:

- Frontend: `http://localhost:3000`
- Backend: `http://localhost:8000`
- Documentacao da API: `http://localhost:8000/docs`
- Health check: `http://localhost:8000/health`

Para parar os containers:

```powershell
docker compose down
```

## Executar sem Docker

1. Configure e rode o backend seguindo a documentacao em [backend/README.md](./backend/README.md).
2. Configure e rode o frontend seguindo a documentacao em [frontend/README.md](./frontend/README.md).

Por padrao, os servicos usam as seguintes URLs:

- Backend: `http://localhost:8000`
- Frontend: `http://localhost:3000`
