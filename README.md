# Bankwise Infrastructure

This repository manages the local development of the BankWise project via Docker Compose. Includes:

- `frontend/` — submodule with Next.js application
- `backend/` — submodule with Spring Boot aplication
- `postgres` — container with DB

## Quick start

```bash
git clone --recurse-submodules https://github.com/Ondrecho/BankWise-infra.git
cd BankWise-infra

docker compose up --build
```
frontend will be available on: http://localhost:3000  
backend will be available on: http://localhost:8080/api

## Updating

```bash
git submodule update --remote --merge

docker compose up --build --force-recreate
```
