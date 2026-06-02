# Backend (FastAPI + SQLAlchemy)

## Requisitos

- Python **3.14.0 ou superior**
- Pip atualizado
- Docker Desktop instalado para uso em containers

Verifique sua versao do Python:

```powershell
python --version
```

## Setup local

1. Copie o arquivo de ambiente:

```powershell
Copy-Item .env.example .env
```

2. Crie e ative o ambiente virtual:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

3. Atualize o pip:

```powershell
python -m pip install --upgrade pip
```

4. Instale as dependencias:

```powershell
pip install -r requirements.txt
```

5. Rode a API:

```powershell
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

6. Acesse:

- `http://localhost:8000`
- `http://localhost:8000/docs`
- `http://localhost:8000/health`

## Variaveis de ambiente

O backend usa a variavel:

```env
FRONTEND_URL=http://localhost:3000
```

Esta variavel e usada para configurar o CORS.

## Docker

### Usando Docker Compose

Na raiz do projeto, execute:

```powershell
docker compose up --build backend
```

Ou inicie toda a aplicacao:

```powershell
docker compose up --build
```

### Alternativa direta no backend

Se preferir iniciar apenas o container do backend:

```powershell
docker build -t desafio-backend .

docker run --rm -p 8000:8000 -e FRONTEND_URL=http://localhost:3000 desafio-backend
```

## Endpoints

- `GET /api/contatos`
- `POST /api/auth/google`
- `GET /health`
- `GET /docs`

## Solucao de problemas Docker

- Se o comando `docker compose` nao for reconhecido, instale ou atualize o Docker Desktop.
- Se a porta `8000` estiver ocupada, pare o servico que estiver usando ela ou altere o mapeamento de portas.
- Se o backend nao conseguir ler variaveis de ambiente, certifique-se de ter criado `.env` a partir de `.env.example`.
