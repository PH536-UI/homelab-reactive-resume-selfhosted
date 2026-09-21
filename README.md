# Homelab - Reactive Resume Self-Hosted

Self-host de builder de curriculos para fugir de paywall e estudar infra real na Dell Latitude 3400.

## O que aprendi
- Debug de env vars obrigatorias na v5: APP_URL, DATABASE_URL, AUTH_SECRET
- Docker Compose com healthcheck do Postgres
- Persistencia com volumes docker + backup com pg_dump
- Acesso externo seguro via Tailscale sem abrir porta
- Redes: ss -tulpn, tcpdump, bind 0.0.0.0 vs localhost

## Arquitetura
Dell Latitude 3400 (Piracicaba) -> Docker -> Postgres 16 + Reactive Resume + Tailscale VPN

## Como rodar
openssl rand -hex 32
cp .env.example .env
docker compose up -d
docker compose logs -f reactive-resume

## Backup
docker compose exec postgres pg_dump -U postgres postgres > backup_$(date +%F).sql

Stack: Docker, Postgres, Linux, Tailscale
