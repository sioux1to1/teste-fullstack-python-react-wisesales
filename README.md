# Teste Técnico — Fullstack Python + React

## Setup

### Pré-requisitos

- Docker e Docker Compose
- Python 3.11+
- Node.js 18+

### Subindo o banco

```bash
cp .env.example .env
docker compose up -d
```

O PostgreSQL sobe na porta 5432 com os dados de seed já carregados (produtos e cupons).

### Verificando

```bash
docker compose exec db psql -U wisesales -c "SELECT name, stock FROM products;"
```

## O que tem aqui

| Arquivo | Descrição |
|---------|-----------|
| `docker-compose.yml` | PostgreSQL 16 |
| `seed.sql` | Tabelas e dados iniciais (products, coupons, cart_items) |
| `.env.example` | Variáveis de ambiente pro banco |

## O que você precisa criar

- **Backend**: API Python com psycopg2 (raw SQL, sem ORM), arquitetura N-layered, Alembic
- **Frontend**: React + Vite, JavaScript, Tailwind CSS, Context API

Leia o enunciado completo no documento do teste técnico que você recebeu.

## Estrutura sugerida

```
/
├── backend/
│   ├── src/
│   │   ├── routes/
│   │   ├── services/
│   │   └── repositories/
│   ├── tests/
│   ├── alembic/
│   └── requirements.txt
├── frontend/
│   ├── src/
│   └── package.json
├── docker-compose.yml
├── seed.sql
└── .env
```

Essa estrutura é uma sugestão. Organize como preferir, desde que esteja claro no README.
