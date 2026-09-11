# Caddy Global

Reverse proxy global para los proyectos alojados en la VPS.

## Responsabilidades

- HTTPS automático mediante Let's Encrypt.
- Enrutamiento por dominio.
- Red Docker compartida para los proyectos.
- Administración centralizada de los puertos 80 y 443.

## Dominios actuales

- `api.precioinbox.com` → `backend:8000`
- `turismo.precioinbox.com/api/*` → `turismo-backend:8000`
- `turismo.precioinbox.com` → `turismo-frontend:80`

## Red compartida

La red utilizada por Caddy y los proyectos es:

```text
proxy_network