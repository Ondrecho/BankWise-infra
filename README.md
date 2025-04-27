# Bankwise Infrastructure

This repository manages the local development of the BankWise project via Docker Compose. Includes:

- `frontend/` — submodule with Next.js application
- `backend/` — submodule with Spring Boot aplication
- `postgres` — container with DB

## Quick start

1. Clone this repository with submodules:
 ```bash
git clone --recurse-submodules https://github.com/Ondrecho/BankWise-infra.git
```
2. Set the environment variable in frontend/.env.production
```
NEXT_PUBLIC_API_URL=http://localhost:8080/api 
```

3. Build and run with Docker:
```bash
cd BankWise-infra

docker compose up --build
```
frontend will be available on: http://localhost:3000  
backend will be available on: http://localhost:8080/api

## Updating
**In case of changes in submodules**
1. Merge the updates:
```bash
git submodule update --remote --merge
```
2. Rebuild and rerun the compose:
```bash
docker compose up --build --force-recreate
```
