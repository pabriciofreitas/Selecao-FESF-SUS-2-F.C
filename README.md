# Desafio

Projeto dividido em duas partes:

- [Backend](./backend/README.md): API desenvolvida com FastAPI e SQLAlchemy.
- [Frontend](./frontend/README.md): aplicacao web desenvolvida com Next.js e React.

## Executar com Docker

1. Certifique-se de ter o Docker instalado e rodando.
2. Na raiz do projeto, execute:

```powershell
docker compose up -d --build
```

3. Aguarde a construção e o start dos containers.

Acesse:

- Frontend: `http://localhost:3000`
- Backend: `http://localhost:8000`
- Documentacao da API: `http://localhost:8000/docs`
- Health check: `http://localhost:8000/health`

Para parar e remover os containers:

```powershell
docker compose down
```

## Executar sem Docker

1. Configure e rode o backend seguindo a documentacao em [backend/README.md](./backend/README.md).
2. Configure e rode o frontend seguindo a documentacao em [frontend/README.md](./frontend/README.md).

Por padrao, os servicos usam as seguintes URLs:

- Backend: `http://localhost:8000`
- Frontend: `http://localhost:3000`

## Solucao de problemas Docker

- Se o comando `docker compose` nao for reconhecido, verifique se o Docker Desktop esta instalado corretamente.
- Se o backend nao iniciar, verifique se a porta `8000` esta livre.
- Se o frontend nao carregar, verifique se o backend esta ativo e se a variavel `NEXT_PUBLIC_API_URL` esta apontando para `http://localhost:8000`.
